---
description: 'Principais comandos do Linux, divididos por categoria'
---

# Comandos Linux

## Manipulação de arquivos

* `tr` - substitui ou delete caracteres. a entrada de caracteres deve vir via pipe.
* `cut` - recorta caracteres de uma entrada de texto.
* `sed` - substituir ou deletar caracteres de uma entrada de texto.
* `grep` - fazer busca por padrões de expressão regular dentro de um arquivo ou stream de texto.
* `egrep` - fazer busca por padrões de expressão regular estendida dentro de um arquivo ou stream de texto \(entende os caracteres especiais\).
* `touch [nome.ext]` - cria um arquivo vazio com o nome.ext informado.

## Comandos do ambiente bash

* `type [cmd]` - este comando informa se o argumento "cmd" é um comando interno do bash ou se é um programa externo.
* `rmdir` - remove diretórios vazios.
* `set` - comando built-in do bash que mostra todas as variáveis declaradas no shell.
* `env` - comando que mostra todas as variáveis de sistema que foram exportadas.
* `$$` - variável pid do processo atual.
* `history` - comando built-in do shell bash que mostra o histórico de todos os comandos enviados pelo usuário.
* `tee` - mostra na tela o que está sendo redirecionado para um arquivo de saída.
* `xargs -n 1` - recebe argumentos a partir do pipe e executa um comando para cada linha.
* `tmux` - gerencia múltiplos terminais.

## Comandos de gerenciamento de processos

* `ppid [id]` - parent id do “id”.
* `kill` - envia um signal para um processo.
* `killall` - mata um processo a partir do nome do mesmo.
* `pregrep [nome]` - busca o pid de um processo a partir do nome do mesmo.
* `pidof` - busca o pid de um processo a partir do nome do mesmo.
* `watch` - executa um processo periodicamente, deixando-o travado na tela.
* `nohup` - evitar que o sinal hup não seja aceito pelo processo em execução, ou seja, quando estivermos em uma conexão remota, aquele processo não será derrubado.
* `top` - mostra todas as informações dos processos em execução no Linux.
* `nice` - rodar um programa com uma prioridade de scheduling modificada.
* `renice` - alterando o nice de um processo em execução.

## Meta comandos

Comandos que dão informação a respeito dos comandos que estão disponíveis na bash.

* `man [cmd]` - mostra o manual de referência do comando "cmd".
* `info [cmd]` - é um “man” reduzido.
* `apropos [palavra]` - lista todos os comandos que tenham “palavra” na sua descrição.
* `man -k [palavra]` - funciona como o apropos.
* `whatis [cmd]` - descreve um comando.
* `which [cmd]` - caminho do executável do comando externo.

## Compactação de arquivos

* `file [arquivo]` - mostra o tipo do “arquivo”.
* `xz` - compactar e descompactar arquivos .xz.
* `bzip2` - compacta com o algoritmo bzip2.
* `gzip` - compacta ou descompacta arquivos.
* `tar cpv` - agrupa arquivos mas não compacta.
* `cpio` - compacta uma lista de arquivos, a entrada é via pipe e a saída precisa ser redirecionada com ‘&gt;’.
* `dd`- criar imagem a partir de uma partição.

## Discos e partições

* `blkid`- mostra um resumo as informações de todas as partições, tais como UUID, LABEL, e tipo.
* `cfisk [partição]`- comando para visualizar, criar ou editar partições através de uma interface interativa.
* `df -h`- mostra detalhes das partições montadas.
* `du -h [diretório]`- mostra informações do tamanho do diretório informado.
* `dumpe2fs [filesystem]` - mostra informações adicionais do filesystem, como o seu UUID.
* `fdisk -l`- comando utilizado para checar as partições de um disco. Este comando mostra as partições e alguns detalhes do sistema de arquivo. No entanto, ele não mostra o tamanho de cada partição.
* `lsblk`- lista todos os discos existentes na máquina, assim como as partições existentes em cada disco.
* `mount`- monta uma partição temporariamente, esta partição será esquecida quando o sistema for reiniciado, para que esta partição seja montada de forma permanente, deve ser inserido um novo registro no arquivo `/etc/fstab`.
* `mount -a` - monta tudo que estiver presente no arquivo `/etc/fstab`.
* `mount --bind [diretório] [diretório]`- montar um diretório dentro de outro diretório.
* `mount [partição] [diretório]`- monta o diretório informado dentro da partição que foi passada como primeiro parâmetro.
* `parted`- mais um utilitário que lista e permite realizar modificação de partições.
* `sdisk -l -uM`- comando parecido com o `fdisk -l` mas com funções extras, como por exemplo mostrar o tamanho de cada partição.
* `systemctl list-units --type=mount`- lista todas as unidades do tipo mount.
* `umount [partição || diretório]`- pode ser passado como parâmetro a partição que você deseja desmontar, ou o nome do diretório que está servindo de ponto de montagem.
* `umount -a` - desmonta tudo que está presente no arquivo `/etc/fstab`.

