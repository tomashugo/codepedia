# O que é Cloud Computing

Cloud Computing é um modelo de computação que disponibiliza recursos de máquinas e rede sob demanda, estes recursos podem ser de *armazenamento* ou *computação* e não estão sob gerenciamento direto dos usuários deste modelo de computação. A ideia é compartilhar os recursos das máquinas disponíveis, diminuindo a ociosidade das mesmas ao mesmo tempo em que propicia a implementação de um modelo de pagamento "_pay as you go_", em que o pagamento é feito a medida que os recursos são utilizados. Desta forma, o usuário pode descartar os recursos utilizados assim que os mesmos não forem mais necessários, disponibilizando-os para os demais usuários da nuvem.

No modelo tradicional de computação *on premises*, as organizações precisam criar e manter os seus *datacenters*, e a cada novo projeto ela precisa comprar novos servidores e equipamentos de rede como (_switches_ e roteadores) para suportar este projeto, o que leva as organizações a dispender uma grande soma de capital no início dos projetos, aumentando também o tempo de implantação dos mesmos uma vez que o processo de espeficicação + compra + chegada + configuração e *deploy* dos novos recursos pode demorar de meses a anos.

Além deste problema econômico e de tempo para os projetos, os recursos computacionais não são utilizados em sua totalidade no início dos projetos, gerando uma grande ociosidade de recursos. No modelo de nuvem, estes recursos podem ser solicitados a medida que cada usuário ou organização necessite dos mesmos, dando agilidade aos projetos e menor necessidade de grandes somas de capitais no início dos projetos.

## Nuvem pública, privada ou híbrida

Existem três modelos de implantação da computação em nuvem. São eles: nuvem pública, nuvem privada e híbrida.

### Nuvem pública

Neste modelo, a nuvem é implementada e operada por um *provedor* (_Cloud Provider_) que disponibiliza o acesso a mesma na internet a qualquer usuário ou organização que precise utilizar os seus recursos, mediante um pagamento que dependerá da forma de uso do recurso.

Como exemplo de nuvens públicas, temos:

* [AWS - que é operada pela Amazon](https://aws.amazon.com/);
* [Azure - operada pela Microsoft](https://azure.microsoft.com/en-us/);
* [Google Cloud - do Google](https://cloud.google.com/?hl=pt-br);
* [OCI - da Oracle](https://www.oracle.com/br/cloud/);

O nome público se refere ao fato de que os mesmos recursos computacionais (servidores e/ou datacenters) podem ser compartilhados por várias organizações diferentes. No entanto, o provedor de nuvem garante o isolamento do recursos por questões de segurança e desempenho. 

A forma como os recursos são administrados pelo provedor é totalmente transparente para o usuário e não afeta em nada a sua utilização. 

### Nuvem privada

Na nuvem privada, os recursos da nuvem são utilizados por somente uma organização. O datacenter onde residem os recursos computacionais podem ou não ser gerenciados pela organização que utiliza os seus recursos, o nome privado refere-se ao fato da utilização dos recursos estar restrita a somente a uma organização.

Este modelo de implantação não obtém todas as vantagens da nuvem uma vez que são necessários altos custos para compra de máquinas e gerenciamento das mesmas. No entanto, este modelo pode ser utilizado como um forma de transição pois ele já utiliza algumas tecnologias presentes na nuvem como: virtualização e containers.

Além disso, existem tipos de aplicações que precisam de uma latência baixa ou que por questões regulatórias não podem estar em uma nuvem pública.

### Nuvem híbrida

Na nuvem híbrida nos temos um misto de nuvem pública e privada. Os recursos de ambas as nuvens estão unidos por uma _VPN_ de modo que os recursos podem ser acessados como se estivessem em uma mesma rede.

Neste modelo, as aplicações que precisam de baixa latência ou por questões regulatórias tem dados sensíveis que precisam estar em posse o utilizador, e as demais aplicações podem estar hospedadas em uma ou mais nuvens públicas.

## Modelos de Serviço

A ideia da Computação em Nuvem é transformar toda a necessidade de TI do usuário em serviço. Estes serviços podem ser classificados dependendo do nível de abstração dos recursos de TI que o provedor propicia. Os três tipos principais estão descritos abaixo, todos os outros modelos são derivações ou combinações destes três modelos:

1. Infraestrutura como serviço (IaaS - Infrastructure as a service)
2. Plataforma como serviço (PaaS - Platform as a service)
3. Software como serviço (SaaS - Software as a service)

### Infrastructure as a service (IaaS)

Neste modelo de serviço, a nuvem disponibiliza ao usuário uma API de alto nível que permite que ele crie máquinas virtuais de forma fácil e sob demanda, abstraindo do usuário, os detalhes de infra-estrutura de rede, particionamento de dados, backup e etc.

Neste modelo o usuário é responsável por manter atualizado o sistema operacional da sua Máquina Virtual, e instalar e implantar todo o _software_ necessário para as suas necessidades organizacionais.

Temos como exemplo deste tipo de nuvem, a [Digital Ocean](https://digitalocean.com), o serviço [EC2 da AWS](https://aws.amazon.com/ec2/), e as [VM da Azure](https://azure.microsoft.com/pt-br/products/virtual-machines/).

### Platform as a service (PaaS)

Caso o usuário necessite de um nível maior de abstração dos recursos, dele pode partir para uma opção de Plataforma como serviço. Neste modelo, o provedor de nuvem disponibiliza um serviço que é uma plataforma para execução de aplicações, onde o usuário precisa somente enviar o código da sua aplicação e todo o restante é gerenciado pela nuvem.

Complexidades como criação e gerenciamento de máquinas virtuais, balanceamento de carga, escalabilidade e alta disponibilidade são feitos pelo provedor de nuvem.

Exemplos: [Heroku](https://heroku.com), [Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/)

### Software as a service (SaaS)

Neste modelo, o acesso ao software é vendido como serviço, temos como exemplos deste tipo de serviço:

* Plataformas de Webmail
* Softwares de produtividade como o [Slack](https://slack.com)
* Ferramentas de low-code ou no-code como o [IFTTT](https://ifttt.com)