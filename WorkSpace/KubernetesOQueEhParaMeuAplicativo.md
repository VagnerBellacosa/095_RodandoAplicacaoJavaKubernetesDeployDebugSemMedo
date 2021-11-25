# Kubernetes: o que é e o que ele faz na prática para meu aplicativo?

![Veja aqui como levar o kubernetes para sua software house](https://blog.tecnospeed.com.br/wp-content/uploads/2020/03/23183949/kubernets.jpg)

Tempo de Leitura: 8 minutos

*Este superpost detalha todas as informações necessárias para quem quer aprender mais sobre Kubernetes. Confira!*

------

Todas as empresas que lidam com o desenvolvimento de aplicações robustas como ERPs ou CRMs, por exemplo, vivem o mesmo problema.

Os projetos que foram iniciados de forma simples acabam virando grandes blocos de [programação difíceis de alterar ou programar](https://blog.tecnospeed.com.br/livros-de-programacao/). 

E toda vez que é necessário mexer nestes blocos, é aquela dor de cabeça de sempre para os desenvolvedores.

Foi tentando corrigir estes problemas que um grupo de engenheiros criou uma nova abordagem de redimensionamento: Kubernetes. 

**Se você está se perguntando o que é Kubernetes e por que eles são importantes, acompanhe este superpost e aprenda tudo sobre o assunto!**

## O que é Kubernetes? 

Kubernetes é uma plataforma de código aberto que **automatiza a implantação, dimensiona e gerencia aplicativos em contêineres.** 

Um dos objetivos de criação do kubernetes e o gerenciamento de contêineres é **levar mais eficiência para o time de desenvolvimento.**

Já que o transporte de aplicações inteiras é complexo e improdutivo, a opção foi dividi-la em diversos contêineres com os códigos e recursos encapsulados. 

Assim, cada um deles pode ser facilmente acessado de onde quer que o desenvolvedor esteja. Sem maiores dores de cabeça e complicações.

### O que é a tecnologia dos contêineres

Se você ainda está se perguntando **o que é um contêiner e para que serve**, vamos explicar agora.

Voltemos alguns anos na História. Como era feito o transporte de carga nos porões dos navios sem o uso de tecnologia?

Com as ferramentas rudimentares da época, todo este processo era lento. Cada tipo de carga era transportado uma por uma. Isso acarretava riscos de avaria e roubo.

O tempo passou e, hoje em dia, já existem contêineres e tecnologia de automação que facilitam a logística de todo este processo.  

**Os contêineres são abastecidos, transportados por guindastes e depositados de forma a ocupar a menor quantidade de espaço possível.** 

O mesmo acontece no Kubernetes, com os contêineres de aplicação. 

Cada um contém um fragmento completo da infraestrutura de programação. Ou seja, código, biblioteca ou recursos, entre outros. 

Para ter acesso a um destes fragmentos, basta acessá-lo de onde estiver e trabalhar naquele bloco de aplicação específico.

Mas que outros benefícios os desenvolvedores encontram ao utilizar este tipo de sistema?

A **produtividade** é o número um deles. Quando o seu time desenvolve aplicações em microsserviços, não precisa de testes ou versões no bloco monolítico inteiro.

Só será necessário alterar aquele código-fonte específico que, aliás, nem precisa ter a mesma linguagem de programação dos demais contêineres. 

A **escalabilidade** é muito maior também, já que é possível excluir ou adicionar recursos com facilidade. 

E, por último, a **disponibilidade**. Quando se fizer alterações somente em parte da aplicação, o restante dos contêineres permanecem ativos e livres de falhas. 

### Como o Kubernetes foi criado? 

Os idealizadores originais do Kubernetes foram Joe Beda, Brendan Burns e Craig McLuckie, em 2014. 

Mas logo os três se juntaram a Brian Grant e Tim Hockin, engenheiros do [Google](https://www.google.com/), e a empresa o lançou no mesmo ano.

O **Kubernetes**, hoje em dia, é mantido pela [Cloud Native Computing Foundation](https://www.cncf.io/).

O desenvolvimento e **design original do Kubernetes foi baseado no sistema Borg,** o gerenciador de cluster usado pelo Google.

O motivo disto é que os principais desenvolvedores trabalharam no Borg anteriormente.

Porém, enquanto o Borg foi escrito inteiramente em C++, o Kubernetes foi implementado em Go.

A primeira versão oficial do Kubernetes foi lançada em 21 de julho de 2015.

Em 06 de março de 2018, o projeto alcançou o nono lugar GitHub e o segundo lugar no núcleo Linux.

Achou interessante entender mais sobre Kubernetes e sua história? **Mas como será que ele funciona?** Continue lendo o superpost e descubra!

## O que faz o Kubernetes na prática?

Bom, até agora já deve ter dado para entender a praticidade e a agilidade que o uso de contêineres leva para o desenvolvimento, não é mesmo? 

Mas e quanto aos Kubernetes? Onde eles entram nessa história? 

Imagine que uma empresa escolheu praticar a abordagem de contêineres no seu dia a dia. Quando menos esperarem, eles estarão multiplicados em milhares. 

E cada unidade de contêiner deve ser implantada num host do servidor. É muita mão de obra para administrar tudo isso!

Para resolver este problema, a plataforma de código aberto chamada **Kubernetes** foi criada como forma de orquestração e gerenciamento de clusters de contêineres.

Ao implantar um cluster num contêiner da Linux, armazenado na [nuvem pública, privada ou híbrida](https://blog.tecnospeed.com.br/migrar-meu-software-para-a-nuvem/), o **Kubernetes** entrará em ação e fará o agrupamento em pods.

Além disso, o **Kubernetes** tem a capacidade de gerenciar todos os contêineres e garantir que todos eles estejam em funcionamento. 

Ou seja, ele não apenas garante o dimensionamento de todos os contêineres como também aciona determinado contêiner se algum deles ficar inativo. 

Mas se você acha que as vantagens do **Kubernetes** terminam aí, está muito enganado. Confira todas as outras agora:

### Descoberta de Serviços e Balanceamento da Capacidade

O Kubernetes pode expor um contêiner usando o nome DNS ou usando seu próprio endereço de IP. 

Se o tráfego para um contêiner for alto, a plataforma poderá equilibrar a carga e distribuir o tráfego da rede para estabilizar toda a implantação.

### Orquestração de armazenamento

Com o **Kubernetes** **é possível montar um sistema de armazenamento de sua escolha**, sejam locais, provedores de nuvens públicas ou privadas.

### Rollout e Rollback automático

Com o uso da plataforma Kubernetes, o seu time pode determinar o estado desejado para seus contêineres implantados. 

Afinal, ela tem a capacidade de alterar o estado real para o estado desejado. 

Por exemplo, seu time pode automatizar o Kubernetes para criar novos contêineres para sua implantação. 

Também é possível remover os contêineres existentes e adotar seus recursos para o novo contêiner.

### Bin Packing automático

Por meio do Kubernetes, você pode **determinar que um cluster de nodes execute tarefas em contêiner.** 

Por exemplo, é possível dizer ao Kubernetes quanta CPU e memória RAM cada contêiner precisa. 

Logo em seguida, a plataforma ajustará os contêineres nos nodes para fazer o melhor uso dos recursos.

### Self-healing (gerenciamento de contêineres funcionais) 

O Kubernetes reinicia/substitui os contêineres que falham e exclui aqueles que não respondem à verificação de integridade definida pelo usuário. 

Além disso, só os libera para os clientes quando eles estão totalmente adequados. 

### Gestão de configuração e segredos (dos usuários) 

A plataforma Kubernetes é **capaz de** **armazenar e gerenciar informações confidenciais, como senhas, tokens e chaves SSH.** 

Ainda implanta e atualiza segredos e configurações de aplicativos sem reconstruir suas imagens de contêiner e sem expor segredos em sua configuração de pilha. 

## Quais são os componentes do Kubernetes?

Até agora nós já demos um panorama geral sobre **para que serve o Kubernetes** e mostramos um pouco da história que envolveu sua criação.

Também abordamos algumas palavras como cluster e node, por exemplo, que, para alguém pouco introduzido no contexto, pode ser um pouco difícil de entender. 

Para tornar tudo mais claro, definiremos cada uma destas palavras. Veremos os componentes essenciais para que a plataforma Kubernetes funcione corretamente. 

Digamos que, se está executando o Kubernetes, se executa um cluster.

Em outras palavras, **o cluster é o conjunto de máquinas de nodes necessários para executar aplicativos em contêiner.** 

O cluster deve conter, pelo menos, um *work node*, ou node de trabalho, e um *master node*, que é o node pr**incipal.** 

**O \*master node\*** **é o responsável por manter o estado desejado do cluster**. 

Ele gerencia os aplicativos em execução e as imagens de contêineres que devem ser usadas.

**Os \*work nodes\* executam os aplicativos e as cargas de trabalho.**

Veja agora cada um dos componentes do cluster e dos nodes, responsáveis pelo funcionamento adequado de suas funções.

## Componentes do painel de controle

### Kube-apiserver

Este componente valida e configura dados para os objetos da API, que incluem pods, serviços, controladores de replicação e outros. 

Esta API server executa operações [REST ](https://blog.tecnospeed.com.br/rest-x-soap/)e fornece o *front-end* ao estado compartilhado do cluster por meio do qual todos os outros componentes interagem.

### Etcd

O etcd é o componente de armazenamento de valores-chave de alta disponibilidade usado como repositório do **Kubernetes** para todos os dados do cluster.

### Kube-scheduler

O kube-scheduler é também chamado de agendador. Sua função é definir cargas de trabalho para nodes específicos. 

Para definir os trabalhos, o kube-scheduler leva em consideração fatores como:

- Recursos individuais e coletivos
- Requisitos de qualidade de serviço
- Restrições de hardware e software
- Localidade dos dados
- Interferência entre cargas de trabalho
- Prazos, entre outros. 

Os requisitos específicos da carga de trabalho serão expostos por meio da API, conforme necessário.

### Kube-controller-manager

Este componente é um *daemon* que incorpora os loops de controle principais enviados pelo Kubernetes.

No Kubernetes, é um controlador de loop de controle que observa o estado compartilhado do cluster pelo apiserver. 

Ele faz alterações tentando mover o estado atual para o estado desejado. 

Como exemplos, temos o controlador de replicação, o controlador de endpoints, o controlador de namespace e o controlador service accounts. 

### Cloud-controller-manager

O controlador de nuvem é um *daemon* que incorpora os loops de controle específicos da nuvem enviados com o Kubernetes.

## Componentes do node

### Kubelet

Este componente é responsável pelo estado de execução de cada node, garantindo que todos os contêineres presentes nele estejam íntegros. 

Ou seja, o Kubelet é responsável por iniciar, pausar e manter os contêineres de aplicativos organizados em pods, conforme indicado pelo plano de controle.

### Kube-proxy

O kube-proxy é **um proxy de rede executado em cada node do cluster**, implementando o conceito de serviço do Kubernetes.

Além disso, este componente mantém regras de rede nos nodes, permitindo a comunicação com seus pods a partir de sessões de rede dentro ou fora do cluster.

O kube-proxy usa a camada de filtragem de pacotes do sistema operacional, se houver uma disponível. Caso contrário, encaminha o próprio tráfego.

### Container Runtime

Este é o software responsável pela execução dos contêineres.

No caso do Kubernetes, eles suporta vários software de execução, como Docker, containerd, CRI-O, entre outros. 

## Adicionais ao sistema Kubernetes

Além de todos estes componentes citados acima, a plataforma Kubernetes ainda precisa de recursos adicionais para desenvolver suas funcionalidades plenamente.

Entre eles:

### Informação de DNS para serviços Kubernetes

DNS significa *Domain Name System*. Em português, Sistema de Nomes de Domínio. 

**A função principal deste sistema é alterar os nomes de computadores ou serviços conectados à internet para seus números de IP.**

Assim, fica muito mais fácil localizar e identificar serviços e dispositivos de computador com os protocolos de rede subjacentes.

No Kubernetes**,** o DNS agenda um pod e serviço no cluster e configura os kubelets para instruir os contêineres individuais a usar o serviço de IP do DNS. 

### Dashboard para gestão de Aplicações

O Dashboard é a interface do usuário Kubernetes. Ele pode ser usado para inúmeras funções como:

- Implantação de aplicativos em contêiner no Kubernetes
- Solução de problemas em um aplicativo em contêiner 
- Gerenciamento de recursos do cluster
- Visão geral dos aplicativos em execução no cluster
- Criação ou alteração de recursos individuais do Kubernetes (como implantações, trabalhos, DaemonSets, entre outros).

Além disso, o dashboard ainda é capaz de fornecer informações sobre o estado dos recursos do Kubernetes no cluster e quaisquer erros que possam ter ocorrido. 

### Monitoramento de recurso dos contêineres

Existem duas soluções capazes de monitorar os recursos dos contêineres: **pipeline de métrica de recursos ou pipeline de métricas completo.**

O pipeline de métrica de recursos fornece um conjunto limitado de métricas relacionadas a determinados componentes do cluster. 

Por exemplo, Horizontal Pod Autoscaler controller ou kubectl top. 

Estas métricas são coletadas pelo lightweight, short-term, in-memory metrics-server e expostos por meio da API metrics.k8s.io.

Já o pipeline de métricas completo, como diz o nome, fornece acesso a métricas mais ricas. 

O Kubernetes pode responder a essas métricas adaptando automaticamente o cluster com base em seu estado atual, usando o Horizontal Pod Autoscaler. 

Este pipeline de monitoramento busca métricas do kubelet. 

Depois, as expõe ao Kubernetes por meio de um adaptador implementando tanto a API custom.metrics.k8s.io quanto a external.metrics.k8s.io.

### Log de Atividades no Nível do Cluster

Nós já dissemos acima que, em geral, **um cluster Kubernetes terá um grande volume de pods para serem gerenciados.**

Como consultar os logs de aplicativo se ele é composto por muitos pods que podem ser reiniciados ou gerados automaticamente pelo sistema Kubernetes?

A maneira mais eficiente de executar estas tarefas é por meio do log de atividades.

O log de atividades no nível do cluster permite coletar registros que persistem além do tempo de vida das imagens do contêiner do pod, do próprio pod ou do cluster. 

Estes logs, por sua vez, serão salvos em um armazenamento de log central com interface de pesquisa e navegação.

## Entendendo e trabalhando com os componentes do Kubernetes

**Os componentes Kubernetes são entidades persistentes no sistema.** Ele as usa para representar o estado do seu cluster, e eles podem descrever: 

- Quais aplicativos em contêiner estão em execução (e em quais nodes)
- Os recursos disponíveis para esses aplicativos
- As políticas sobre como esses aplicativos se comportam, como políticas de reinicialização, atualização, falhas, entre outros.

Agora vamos mostrar as funções de cada um dos componentes Kubernetes. 

### Replica sets

O objetivo de um ReplicaSet **é manter um conjunto estável de pods de réplica em execução.** 

Além disso, ele é frequentemente usado para garantir a disponibilidade de determinado número de pods idênticos.

O ReplicaSet possui inúmeros campos com informações para identificar:

- Os pods que ele pode obter
- O número de réplicas que indica quantos pods ele deve manter 
- O modelo de pod que determina os dados dos novos pods que ele deve criar para atender ao número de critérios de réplicas. 

A partir de então o ReplicaSet cria e exclui pods conforme necessário para atingir o número desejado. 

### Services

Services são uma abstração que expõe uma aplicação em execução em um conjunto de pods. 

### Volumes

Os volumes são um diretório que contém dados acessíveis aos contêineres em um pod. Um volume Kubernetes tem a mesma vida útil que o pod que o encapsula. 

Ele sobrevive a todos os contêineres executados no pod e os dados são preservados quando um contêiner é reiniciado.

O Kubernetes suporta muitos tipos de volumes e um pod pode usar todos eles simultaneamente.

### Namespaces

O Kubernetes pode gerenciar vários clusters virtuais (para equipes ou projetos diferentes) suportados pelo mesmo cluster físico. 

Esses clusters virtuais são chamados de namespaces.

### ConfigMaps and Secrets

O **Kubernetes** possui dois tipos de objetos que podem injetar dados de configuração em um contêiner ao iniciá-lo: Secrets e ConfigMaps. 

Ambos os componentes se comportam de maneira semelhante. Não apenas na forma como são criados. 

Mas também podem ser expostos em um contêiner como arquivos montados, volumes ou variáveis de ambiente.

### Stateful Sets

StatefulSet é o objeto da API de carga de trabalho usado para gerenciar aplicações stateful. 

Como uma implantação, um StatefulSet gerencia pods com base em uma especificação de contêiner idêntica. 

Ao contrário de uma implantação, um StatefulSet mantém uma identidade persistente para cada um de seus pods. 

Esses pods são criados com a mesma especificação, mas não são intercambiáveis: cada um tem um identificador persistente, mantido em qualquer reagendamento.

### Daemon Sets

Um DaemonSet garante que os nodes executem uma cópia de um pod. **À medida que os nodes são adicionados ao cluster, os pods são adicionados a eles.** 

Porém, sempre que os nodes forem removidos do cluster, esses pods são coletados como lixo. A exclusão de um DaemonSet limpará os pods criados.

Entre os diversos usos de um DaemonSet, podemos citar: 

- Daemon de armazenamento em cluster em cada node, como glusterd e ceph, por exemplo. 
- Daemon de coleta de logs em todos os nodes, como fluentd ou filebeat.
- Daemon de monitoramento de node em cada node, como Prometheus Node Exporter, Flowmill, Sysdig Agent, collectd, Dynatrace OneAgent, AppDynamics Agent, entre outros. 

Em um caso simples, um DaemonSet, cobrindo todos os nodes, seria usado para cada tipo de daemon. 

Uma configuração mais complexa pode usar vários DaemonSets para um único tipo de daemon. 

No entanto, com diferentes sinalizadores e/ou diferentes solicitações de memória e CPU para cada tipo de hardware.

## Conclusão

Este superpost mostrou bem os motivos que tornaram o Kubernetes a plataforma de orquestração de contêineres mais utilizada no mundo. 

Afinal, **nada melhor do que aproveitar a própria tecnologia para beneficiar o cotidiano de quem vive imerso em desenvolvimento de tecnologia.** 