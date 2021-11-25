# O que é Kubernetes? Tudo que você precisa saber sobre!

- março 8, 2021
- [1 Comment](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#disqus_thread)

Quer saber qual é uma das principais tecnologias do momento? **Kubernetes (K8s)**.

A adoção dessa tecnologia por empresas de todos os tamanhos tem se espalhado como fogo, levando o número de oportunidades para profissionais que manjam dessa tecnologia a crescer rapidamente.

Que tal aprender um pouco mais sobre K8s e garantir aquela próxima vaga?

“*…no Google nós temos gerenciado contêineres Linux em larga escala por mais de 10 anos…*“

Esse é um trecho de um artigo publicado em 2016 pelo Google chamado **[Borg, Omega, and Kubernetes](https://queue.acm.org/detail.cfm?id=2898444)**.

O projeto foi desenvolvido com base nos desafios e aprendizados de engenheiros do ***Google\*** enquanto eles tentavam desenvolver uma plataforma que fosse capaz de suportar diversas aplicações e times dentro da empresa.

**Conteúdo** [ocultar](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#) 

[1 O que é Kubernetes?](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#O_que_e_Kubernetes)

[2 Como funciona o Kubernetes: Containers](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#Como_funciona_o_Kubernetes_Containers)

[3 Como funciona o Kubernetes: Aplicações cloud-native](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#Como_funciona_o_Kubernetes_Aplicacoes_cloud-native)

[3.1 Características das aplicações cloud-native](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#Caracteristicas_das_aplicacoes_cloud-native)

[4 Funcionalidades do Kubernetes](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#Funcionalidades_do_Kubernetes)

[5 A arquitetura Kubernetes: Como funciona?](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#A_arquitetura_Kubernetes_Como_funciona)

[5.1 Node](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#Node)

[5.2 etcd](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#etcd)

[5.3 Master](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#Master)

[5.4 Control Plane](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#Control_Plane)

[6 Aprendendo kubernetes: como criar aplicações?](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#Aprendendo_kubernetes_como_criar_aplicacoes)

[6.1 Configuração declarativa](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#Configuracao_declarativa)

[6.2 Entendendo a API do Kubernetes](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#Entendendo_a_API_do_Kubernetes)

[7 Um resumo das vantagens do kubernetes](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#Um_resumo_das_vantagens_do_kubernetes)

[8 O que é um cluster Kubernetes e como construir um?](https://blog.geekhunter.com.br/kubernetes-a-arquitetura-de-um-cluster/#O_que_e_um_cluster_Kubernetes_e_como_construir_um)

## O que é Kubernetes?

![kubernetes é mantido pelo Cloud Native Computing Foundation](https://blog.geekhunter.com.br/wp-content/uploads/2019/04/logo-kubernetes-arquitetura-de-cluster-3.png)

**O K8s é um projeto de código aberto que tem como objetivo orquestrar containers e automatizar a implantação de aplicações.**

Atualmente mantido pela **[Cloud Native Computing Foundation](https://www.cncf.io/)**, o Kubernetes gerencia os clusters que contêm os hosts que executam as aplicações Linux.

Esses clusters podem incluir hosts em nuvem, por isso, o Kubernetes é a plataforma ideal para hospedar aplicações *cloud-native* que exigem escalabilidade rápida, como a transmissão de dados em tempo real por meio do [Apache Kafka](https://blog.geekhunter.com.br/apache-kafka/).

Fazer o *deploy* de uma nova versão de uma aplicação é sempre um processo arriscado. Existem uma série de passos manuais ou semi-automatizados e, caso algo dê errado, fazer o *rollback* para a versão anterior é super complicado.

Agora imagine isso com uma aplicação composta por dezenas de microsserviços, cada um com um ciclo de vida diferente, datas de *release* diferentes, tecnologías diferentes.

Esse seria o pesadelo de qualquer time de desenvolvimento.

Por isso, ele elimina muitos processos manuais que uma aplicação em containers exige, facilitando e dando agilidade a projetos de microsserviços, por exemplo.

Recomendo esse vídeo do canal Código Fonte, é muito didático e explica de uma forma simples e clara!

<iframe title="Kubernetes // Dicionário do Programador" width="820" height="461" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="" data-src="https://www.youtube.com/embed/mVL0nOM3AGo?feature=oembed&amp;enablejsapi=1&amp;origin=https://blog.geekhunter.com.br" class=" lazyloading" data-gtm-yt-inspected-1_19="true" style="box-sizing: border-box; max-width: 100%; position: absolute; inset: 0px; width: 620px; height: 348.75px; border: 0px;"></iframe>

## Como funciona o Kubernetes: Containers

![conteineres na programaçãio ](https://blog.geekhunter.com.br/wp-content/uploads/2019/08/Entendendo-um-pouco-sobre-cont%C3%AAineres.jpg)

Não tem muito mistério! Containers seguem basicamente a mesma lógica da sua contraparte literal.

Da mesma forma que agrupamos objetos que precisam ser enviados de um local para o outro em containers, também agrupamos nossos códigos em um container, que pode ser executado em diversos locais.

Dessa forma, podemos trabalhar com componentes menores, utilizando a arquitetura de microsserviços que, assim como o **Kubernetes**, está em alta.

Utilizar *microservices* e *containers* simplifica a vida do programador, pois dissipa codificações enormes em outras menores, impedindo que seu código vire um monstro.

> **[Tudo sobre DevOps, para iniciantes.](https://blog.geekhunter.com.br/tudo-sobre-devops-iniciantes/)**

## Como funciona o Kubernetes: Aplicações *cloud-native*

![Aplicações cloud-native ](https://blog.geekhunter.com.br/wp-content/uploads/2019/08/photo-1509803874385-db7c23652552-min.jpg)

C*loud-native* é o termo utilizado para classificar aplicações projetadas para tirar máximo proveito de ambientes em nuvem, seja ela privada ou pública.

Essas aplicações se baseiam na **[arquitetura de microsserviços](https://blog.geekhunter.com.br/microservices-e-o-perigo-das-modinhas/)** e incorporam práticas que possibilitam a automação de todo o ciclo de vida da aplicação.

Existem aplicações conhecidas como **[monolíticas](https://blog.geekhunter.com.br/arquitetura-de-microsservicos-x-arquitetura-monolitica/)**, onde todas as partes da aplicação vivem juntas (causando forte acoplamento).

A arquitetura de microsserviços sugere a ideia de que aplicações devem ser compostas por partes menores e independentes chamadas de serviços (resultando em fraco acoplamento).

A ideia é que cada serviço seja especializado e ofereça uma API para se comunicar com outros serviços.

Essa característica possibilita, por exemplo, que diferentes times assumam diferentes partes de uma mesma aplicação.

Outra vantagem é que um mesmo serviço pode ser utilizado por múltiplas aplicações sem nenhum esforço extra.

[![img](https://blog-geek-midia.s3.amazonaws.com/wp-content/uploads/2021/03/08130032/cta1-kubernetes.png)](https://www.geekhunter.com.br/vagas?utm_source=blog&utm_medium=banner&utm_campaign=o_que_e_kubernetes)

### Características das aplicações cloud-native

![Aplicação cloud-native composta por contêineres ](https://lh6.googleusercontent.com/xYwp01TS-OIA7LwfhjVaz3MJYo3I9znj_i3pU4j3uq85wYZGxCUdorP4zJqch-FsDBlfrv_tlHjarpBxqKpZtXsvYO-xF9NLyHp0H_n0bkpZiwfBxfgIRnxpSfBxne68e-EhybAw)

No caso de aplicações *cloud-native*, uma das principais características é que elas utilizam contêineres para encapsular cada microsserviço.

Como esses contêineres possuem o serviço e todas as suas dependências, eles se tornam independentes da infraestrutura, podendo ser facilmente migrados de uma *cloud* para outra, por exemplo.

Outro ponto importante é que a **[utilização de contêineres](https://blog.geekhunter.com.br/orquestracao-de-conteineres-docker-swarm-portainer/)** facilita muito questões como escalabilidade e *deploy* de novas versões.

No exemplo da imagem acima, se 3 contêineres da interface web não forem suficientes, basta iniciar mais um.

Saiu uma nova versão? Basta substituir os contêineres pela nova versão. A nova versão tem um bug crítico? Só substituir de volta pelo contêiner da versão anterior.

Esse tipo de flexibilidade traz diversas vantagens, mas também cria novos desafios. Quando uma aplicação é composta por diversas partes pequenas, gerenciar tudo isso de forma manual pode se tornar bem complexo.

**E é para ajudar nessa parte que existem orquestradores como o Kubernetes.**

> [**Microservices**](https://blog.geekhunter.com.br/microservices-e-o-perigo-das-modinhas/) e o perigo das “modinhas”

## Funcionalidades do Kubernetes

![funcionalidades do kubernetes ](https://blog.geekhunter.com.br/wp-content/uploads/2019/08/funcionalidades-do-kubernetes.jpg)

Para ajudar a resolver o problema citado no começo do texto, o **Kubernetes** oferece uma série de funcionalidades. No entanto, antes de entrarmos em detalhes, é importante entendermos um conceito central do K8s: **o estado da aplicação**.

A ideia por trás desse conceito é que existem dois tipos de estado de uma aplicação: **o atual e o desejado.**

O estado atual da aplicação descreve a realidade. Por exemplo, quantas réplicas de um determinado serviço estão em execução, qual a versão em produção de cada serviço e por aí vai.

Já o estado desejado descreve como o time ou a pessoa responsável pela aplicação deseja que ela esteja naquele momento.

O Kubernetes implementa uma série de *loops* que ficam constantemente verificando se o estado atual é igual ao estado desejado. Esse papel é desempenhado pelos chamados *Controllers*.

Quando um *controller* identifica que o estado atual é diferente do estado desejado, ele aciona outros componentes do sistema para fazer novamente com que o estado atual se iguale ao estado desejado.

Todo esse processo de monitoramento e gestão do estado da aplicação, sem contar a execução da aplicação em si, exige uma série de componentes. É por isso que a arquitetura de um ambiente Kubernetes é baseada em um cluster de máquinas.

> Usando o [**MediatR com ASP.NET Core**](https://blog.geekhunter.com.br/utilizando-a-biblioteca-mediatr-com-asp-net-core/)

## A arquitetura Kubernetes: Como funciona?

![infraestrutura de um cluster](https://blog.geekhunter.com.br/wp-content/uploads/2019/04/arquitetura-de-cluster-kubernetes.png)

O Kubernetes é composto por uma série de componentes, cada um com um propósito diferente. Para garantir que exista uma separação de responsabilidades e que o sistema seja resiliente, o **K8s** utiliza um cluster de máquinas para ser executado.

As máquinas de um cluster são separadas em três tipos:

### Node

O primeiro tipo é chamado de *Node*. O papel de um *Node* é executar os contêineres que encapsulam as aplicações sendo gerenciadas pelo K8s.

Quando você faz o *deploy* de uma aplicação em um cluster K8s, essa aplicação vai ser executada em um dos *Nodes* do cluster. O conjunto de *Nodes* forma o que chamamos de *Workers*.

### *etcd*

O segundo tipo de nó é o *etcd*. O *etcd* é, na verdade, o nome da **[base de dados distribuída](https://github.com/etcd-io/etcd)** que é utilizada para armazenar tudo o que está acontecendo dentro do cluster, incluindo o estado da aplicação.

Em ambientes de produção, um bom gerenciamento desses nós é essencial para garantir que o *cluster* esteja sempre disponível.

### Master

Finalmente, o último tipo de nó é o que chamamos de *Master*. É nesse tipo de nó que os principais componentes do Kubernetes são executados, como o *Scheduler*, o qual tem a responsabilidade de controlar a alocação de recursos no cluster.

O conjunto de nós *Master* forma o que pode ser considerado o cérebro de um cluster Kubernetes: o *Control Plane*.

### Control Plane

O *Control Plane* do Kubernetes pode ser considerado o cérebro de um cluster. Ele é responsável por gerenciar os principais componentes do sistema e garantir que tudo está funcionando de acordo com o estado desejado da aplicação.

Para facilitar a representação desse estado, o K8s trabalha com uma abstração chamada de *Object*. Um *Object* representa parte do estado da aplicação e quando o seu estado atual não é o estado desejado, mudanças são aplicadas para que os dois estados se igualem novamente.

Existem diversos tipos de *Objects* em um ambiente Kubernetes, mas alguns deles são essenciais para entendermos como um cluster funciona.

#### Pod

Na seção sobre aplicações *cloud-native*, uma das principais características é que essas aplicações utilizam contêineres para encapsular seus microsserviços. No entanto, quando falamos sobre aplicações sendo executadas em um cluster Kubernetes, não falamos sobre contêineres diretamente, mas sim sobre *Pods*.

*Pods* são a unidade básica de um um cluster **K8s**. Elas encapsulam um ou mais contêineres de uma aplicação e representam um processo dentro do cluster. Quando fazemos o *deploy* de uma aplicação no K8s, estamos criando uma ou mais *Pods*.

No entanto, *Pods* são efêmeras, ou seja, elas são criadas e destruídas de acordo com as necessidades do cluster.

Para garantir que o acesso a um microsserviço esteja sempre disponível, existe um *Object* chamado *Service* que encapsula uma ou mais *Pods* e é capaz de encontrá-las dinamicamente em qualquer *Node* do cluster.

#### Deployment

Esse tipo de *Object* oferece uma série de funcionalidades que automatizam todos aqueles passos que descrevemos de um cenário típico de desenvolvimento de software, com *deploys* manuais ou semi-automatizados de uma aplicação.

Utilizando *Deployments*, nós podemos descrever qual o estado desejado da nossa aplicação e um *Deployment controller* vai se encarregar de transformar o estado atual no estado desejado, caso eles sejam diferentes.

E por falar em descrever o estado desejado da nossa aplicação, é hora de entendermos como isso é feito em um ambiente **Kubernetes**.

[![img](https://blog-geek-midia.s3.amazonaws.com/wp-content/uploads/2021/03/08130012/cta2-kubernetes.png)](https://www.geekhunter.com.br/criar-perfil-gratis?utm_source=blog&utm_medium=banner&utm_campaign=o_que_e_kubernetes)

## Aprendendo kubernetes: como criar aplicações?

![fluxo de uma aplicação](https://blog.geekhunter.com.br/wp-content/uploads/2019/04/configuracao-declarativa-cloud-native-para-criar-aplicacoes.png)

Quando estamos utilizando um cluster Kubernetes, existem duas formas de aplicarmos mudanças ao estado atual de uma aplicação, ou seja, de mudarmos sua configuração.

A abordagem tradicional e que talvez você esteja mais acostumado é o chamada de **Configuração Imperativa**, onde dizemos como cada mudança deve ser feita.

Por exemplo, imagine que você queira mudar o número de réplicas de uma determinada *Pod* de 3 para 4.

Na abordagem imperativa, você enviaria comandos diretamente para a **API** do K8s dizendo que você quer alterar o número de réplicas de 3 para 4. Mas como fazer isso em uma aplicação com dezenas de microsserviços?

E se, enquanto você estava alterando cada um deles, algo aconteceu e você só teve tempo de aplicar as mudanças em metade das *Pods*. Quais são as implicações que uma mudança como essa poderia causar? Se algo começar a dar errado, como os membros do seu time vão saber o que já foi alterado e o que ainda não foi?

Talvez você tenha passado um parâmetro errado em um dos comandos e agora a aplicação está fora do ar.

### Configuração declarativa

É para evitar esse tipo de problema que o Kubernetes suporta o que é chamado de **Configuração Declarativa**.

Em uma abordagem declarativa, nós não dizemos como uma mudança deve ser feita, mas apenas qual mudança deve ser feita.

O sistema, no nosso caso o *Control Plane* do K8s, vai decidir qual é a melhor forma de aplicar aquela mudança e tornar o estado atual da aplicação igual ao estado desejado.

Se nós fossemos fazer a mesma mudança do exemplo anterior, alterar o número de réplicas de uma *Pod* de 3 para 4 de uma forma declarativa, bastaria alterarmos o valor do campo “replicas” no exemplo abaixo e enviarmos esse arquivo YAML para a API do K8s.

```
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: frontend
  labels:
    app: guestbook
    tier: frontend
spec:
  # só precisamos alterar o valor do campo abaixo
  replicas: 3
  selector:
    matchLabels:
      tier: frontend
  template:
    metadata:
      labels:
        tier: frontend
    spec:
      containers:
      - name: php-redis
        image: gcr.io/google_samples/gb-frontend:v3
```

Por falar na API do Kubernetes, vamos entender melhor como ela funciona?

### Entendendo a API do Kubernetes

![API no  Control Plane ](https://blog.geekhunter.com.br/wp-content/uploads/2019/04/api-do-kubernetes-clusters.png)

A API do Kubernetes é um dos principais elementos do *Control Plane*. É através dela que conseguimos interagir com todos componentes de um cluster K8s, seja pela linha de comando ou pela interface web.

Além disso, é a API quem define os diferentes *Objects* que fazem parte do ecossistema do K8s.

Quando enviamos uma alteração de estado, seja de forma imperativa ou declarativa, a API cria o que é chamado de *Record of Intent* (Registro de Intenção). Dependendo do *Object* que está sendo alterado nesse *Record of Intent*, um *Controller* específico vai detectar que o estado desejado foi alterado e vai reagir para aplicar as mudanças necessárias.

Como existem diversos tipos de *Objects* no contexto do Kubernetes, a API pode parecer complexa quando vista pela primeira vez. Para facilitar a gestão e evolução da API, os *Objects* foram agrupados em diferentes categorias, como *Core*, *Apps* e *Storage*.

Esse grupos são compostos por desenvolvedores da comunidade Kubernetes e são eles quem decidem como cada categoria vai evoluir. Isso mostra a natureza open source do projeto e como os usuários do sistema tem influência direta na sua evolução.

## Um resumo das vantagens do kubernetes

![vantagens do kubernetes ](https://blog.geekhunter.com.br/wp-content/uploads/2019/08/checklist-2077020_960_720-min.jpg)

O Kubernetes é uma ferramenta super poderosa, mas que pode parecer bem complexa em um primeiro momento.

Existem diversos conceitos e componentes envolvidos no funcionamento de um cluster, mas são eles que fazem com o que o K8s seja o orquestrador mais utilizado no momento.

Para recapitularmos os principais pontos que vimos sobre o Kubernetes e organizar o nosso raciocínio, aqui vai um resumo:

- O K8s oferece uma plataforma completa para aplicações conhecidas como *cloud-native*;
- Os seus componentes são executados em um cluster composto por três tipos de nós: *Node*, *etcd* e *Master*;
- O conjunto de todos os nós *Master* forma o chamado *Control Plane*, o qual é responsável por controlar tudo o que acontece dentro do cluster e monitorar o estado da aplicação;
- Ele utiliza abstrações, como *Pods* e *Deployments*, chamadas de *Objects* para representar diferentes aspectos do estado de uma aplicação;
- Esse estado pode ser alterado de duas formas: imperativa ou declarativa. A forma declarativa é considerada a mais ideal e utiliza arquivos no formato YAML que são enviados para a API;
- A API do Kubernetes é a porta de entrada de um cluster, sendo utilizada tanto pela linha de comando quando pela interface web.

Agora que você já tem uma noção do que é o Kubernetes e da sua arquitetura, é hora de começar a aprender da melhor forma possível: colocando a mão na massa!

## O que é um cluster Kubernetes e como construir um?

![como construir um cluster Kubernetes](https://blog.geekhunter.com.br/wp-content/uploads/2019/08/tools-864983_960_720-min.jpg)

Como bônus, vou agora dar algumas dicas para você construir o seu primeiro cluster Kubernetes. Prontos?

A melhor forma de aprender como o Kubernetes funciona é usando ele na prática. Para isso, existem 3 formas rápidas de você criar o seu primeiro cluster.

A primeira, e mais fácil, é utilizando o site: **[Play With Kubernetes](https://labs.play-with-k8s.com/)**.

O *Play with K8s* oferece um cluster Kubernetes que você pode acessar através do seu browser. A ideia é que você tenha um ambiente de laboratório para brincar por até 4 horas. Depois disso, o ambiente é destruído, mas você sempre pode criar um novo.

Outra opção é utilizar a função Kubernetes disponível no **[Docker](https://www.docker.com/)**.

Caso você não conheça, o Docker é principal **[plataforma para contêineres](https://blog.geekhunter.com.br/orquestracao-de-conteineres-docker-swarm-portainer/)** no momento. Graças a ele, o uso de contêineres ganhou popularidade nos últimos anos, gerando uma série de novas tecnologias e práticas, como é o caso das aplicações *cloud-native*.

Com o avanço do Kubernetes, o Docker criou uma opção que possibilita a criação de um cluster K8s na sua máquina.

Para isso, basta instalar o Docker seguindo as **[instruções para o seu sistema operacional](https://docs.docker.com/install/#supported-platforms)**, clicar com o botão direito no ícone do Docker e selecionar Preferências.

Nesse menu você deve achar a opção chamada Kubernetes, como na imagem abaixo.

![menu da plataforma de conteineres docker](https://blog.geekhunter.com.br/wp-content/uploads/2019/04/menu-do-docker-kubernetes.png)

Finalmente, a terceira opção é utilizar os serviços oferecidos pelos provedores de nuvem pública.

Com a adoção do Kubernetes crescendo a cada dia, era natural que eles não ficariam de fora.

Atualmente, os principais serviços são:

- **[Amazon EKS](https://aws.amazon.com/pt/eks/?nc1=h_ls)** da AWS;
- **[Kubernetes Engine](https://cloud.google.com/kubernetes-engine/)** do Google Cloud Platform; e
- **[AKS](https://azure.microsoft.com/pt-br/services/kubernetes-service/)** da Azure (Microsoft).

Essas três opções oferecem um cluster gerenciado, livrando você de se preocupar com diversos aspectos, como quantidade de nós *etcd* e *Master*.

E aí estão, três formas de você criar o seu primeiro cluster e começar a aprender Kubernetes na prática.

Espero que esse artigo tenha ajudado a clarear um pouco mais o por que tantas empresas estão interessadas em utilizar o K8s e tenha te inspirado a querer aprender mais. O mercado está cheio de oportunidades sensacionais para aqueles que se empenharem.

Como sempre, caso tenha dúvidas, não pense duas vezes, é só me mandar uma mensagem que eu estarei aqui para te responder.