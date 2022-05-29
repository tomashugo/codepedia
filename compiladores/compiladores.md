# Estrutura de um compilador

Um compilador é constituído de **duas fases**, uma fase de _análise_ e uma fase de _síntese_. A fase de análise também é chamada frequentemente de _front end_ do compilador enquanto a fase de síntese é chamada de _backend_.

A fase de análise quebra o código fonte em suas peças constituintes, validando uma gramática que o representa. Esta fase também é responsável pela criação de uma estrutura intermediária de representação do programa. Caso o programa tenha alguma mal formação sintática ou semântica, a fase de análise é responsável por disponibilizar mensagens que sejam informativas, para que o usuário possa tomar medidas de correção do código.

Na fase de síntese, são criadas várias representações independentes a partir da representação de código intermediária, gerada na fase anterior. 

Antes de gerar a versão final do código, para a arquitetura de destino, a fase de *backend* realiza várias otimizações de código, visando uma melhor utilização dos recursos da máquina.

## Fases de um compilador

| Entrada | Transformação realizada | Saída |
|--------|--------|--------|
| Código fonte | Análise Léxica | Fluxo de tokens |
| Fluxo de tokens | Análise sintática | Árvore sintática |
| Árvore sintática | Análise semântica | Árvore sintática |
| Árvore sintática | Geração intermediária de código | Representação intermediária | 
| Representação intermediária | Otimização de código independente de máquina | Representação intermediária |
| Representação intermediária | Geração de código | Código para a máquina destino |
| Código para a máquina destino | Otimização dependente de máquina | Código para a máquina destino |