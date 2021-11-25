CONTAINERS

# O que é Kubernetes?

Kubernetes, ou “k8s”, é uma plataforma open source que automatiza as operações dos [containers Linux](https://www.redhat.com/pt-br/topics/containers/whats-a-linux-container). O Kubernetes elimina grande parte dos processos manuais necessários para implantar e escalar as aplicações em containers. Em outras palavras, se você desejar agrupar em clusters os hosts executados nos containers Linux, o Kubernetes ajudará a gerenciar esses clusters com facilidade e eficiência. Esses clusters podem incluir hosts em [nuvem pública](https://www.redhat.com/pt-br/topics/cloud-computing/what-is-public-cloud), [nuvem privada](https://www.redhat.com/pt-br/topics/cloud-computing/what-is-private-cloud) ou [nuvem híbrida](https://www.redhat.com/pt-br/topics/cloud-computing/what-is-hybrid-cloud). Por isso, o Kubernetes é a plataforma ideal para hospedar [aplicações nativas em nuvem](https://www.redhat.com/pt-br/topics/cloud-native-apps) que exigem escalabilidade rápida, como a transmissão de dados em tempo real por meio do[ Apache Kafka](https://www.redhat.com/pt-br/topics/integration/what-is-apache-kafka).

Originalmente, o Kubernetes foi criado e desenvolvido por engenheiros do Google. O Google foi um dos [pioneiros no desenvolvimento da tecnologia de containers Linux](https://en.wikipedia.org/wiki/Cgroups). Além disso, a empresa já revelou publicamente que [tudo no Google é executado em containers](https://speakerdeck.com/jbeda/containers-at-scale) (inclusive, essa é a tecnologia por trás dos serviços em cloud da empresa). O Google gera mais de 2 bilhões de implantações de containers por semana, viabilizadas por uma plataforma interna: [Borg](http://blog.kubernetes.io/2015/04/borg-predecessor-to-kubernetes.html). O Borg foi o antecessor do Kubernetes. As lições aprendidas ao longo dos anos de desenvolvimento do Borg foram a principal influência para o desenvolvimento da tecnologia do Kubernetes.

*Uma curiosidade sobre o Kubernetes é que os sete raios do logotipo fazem referência ao nome original do projeto, “[Project Seven of Nine](https://cloudplatform.googleblog.com/2016/07/from-Google-to-the-world-the-Kubernetes-origin-story.html)” (Projeto Sete de Nove).*

A Red Hat foi uma das primeiras empresas a trabalhar com o Google no desenvolvimento do Kubernetes, antes mesmo do lançamento da plataforma. Foi assim que nos tornamos o [segundo maior colaborador](https://www.stackalytics.com/cncf?module=kubernetes) com o projeto upstream dessa tecnologia. Em 2015, o Google [doou o projeto Kubernetes](https://techcrunch.com/2015/07/21/as-kubernetes-hits-1-0-google-donates-technology-to-newly-formed-cloud-native-computing-foundation-with-ibm-intel-twitter-and-others/) à [Cloud Native Computing Foundation](https://www.cncf.io/), recém-formada na época.

------

## Kubernetes: entenda por que ele é essencial

Aplicações de produção abrangem múltiplos containers. Eles devem ser implantados em vários hosts do servidor. A [segurança dos containers](https://www.redhat.com/pt-br/topics/security/container-security) tem várias camadas e pode ser complexa. É aí que o Kubernetes entra em cena. Ele oferece os recursos de orquestração e gerenciamento necessários para implantar containers em escala para essas cargas de trabalho. Com a orquestração do Kubernetes, é possível criar serviços de aplicações que abrangem múltiplos containers, programar o uso deles no cluster, escalá-los e gerenciar a integridade deles com o passar do tempo. Com o Kubernetes, você toma medidas reais para aprimorar a [segurança da TI](https://www.redhat.com/pt-br/topics/security).

Também é necessário integrar o Kubernetes com os serviços de rede, [armazenamento](https://www.redhat.com/pt-br/topics/data-storage), segurança, telemetria e outros para oferecer uma infraestrutura de containers global.

![diagrama Kubernetes](https://www.redhat.com/cms/managed-files/kubernetes-diagram-902x416.png)

No entanto, isso obviamente depende do uso que cada empresa faz dos containers em seus próprios ambientes. Uma aplicação rudimentar dos containers Linux os trata como máquinas virtuais rápidas e eficientes. Quando escalado para um ambiente de produção e diversas aplicações, fica claro que é necessário ter vários containers alocados funcionando em conjunto para disponibilizar serviços individuais. Isso multiplica substancialmente o número de containers no ambiente. À medida que eles se acumulam, a complexidade também aumenta.

O Kubernetes corrige vários problemas comuns que ocorrem com a proliferação de containers, organizando-os em "pods". Os pods adicionam uma camada de abstração aos containers agrupados. Assim, é mais fácil programar as cargas de trabalho e fornecer os serviços necessários a esses containers, como rede e armazenamento. Outros componentes do Kubernetes são úteis no balanceamento de carga entre os pods. Com isso, é possível garantir que o número de containers em execução seja suficiente para oferecer suporte às cargas de trabalho.

Com a implementação correta do Kubernetes (e a ajuda de outros projetos open source, como [Open vSwitch](http://openvswitch.org/), [OAuth](https://oauth.net/) e [SELinux](https://selinuxproject.org/page/Main_Page)), as empresas podem orquestrar todas as partes da infraestrutura de containers.

------

## Como o Kubernetes funciona e para que serve?

A principal vantagem que as empresas garantem ao usar o Kubernetes, especialmente se estiverem [otimizando o desenvolvimento de aplicações para a cloud](https://www.redhat.com/pt-br/topics/cloud-native-apps), é que elas terão uma plataforma para programar e executar containers em clusters de máquinas físicas ou virtuais. Em termos mais abrangentes, com o Kubernetes, é mais fácil implementar e confiar totalmente em uma infraestrutura baseada em containers para os ambientes de produção. Como o propósito do Kubernetes é automatizar completamente as tarefas operacionais, ele permite que os containers realizem muitas das tarefas possibilitadas por outros sistemas de gerenciamento ou plataformas de aplicações.

O Kubernetes possibilita:

- Orquestrar containers em vários hosts.
- Aproveitar melhor o hardware para maximizar os recursos necessários na execução das aplicações corporativas.
- Controlar e automatizar as implantações e atualizações de aplicações.
- Montar e adicionar armazenamento para executar aplicações com monitoração de estado.
- Escalar rapidamente as aplicações em containers e recursos relacionados.
- Gerenciar serviços de forma declarativa, garantindo que as aplicações sejam executadas sempre da mesma maneira como foram implantadas.
- Verificar a integridade e autorrecuperação das aplicações com posicionamento, reinício, replicação e escalonamento automáticos.

No entanto, o Kubernetes depende de outros projetos para oferecer plenamente esses serviços orquestrados. Com a inclusão de outros projetos open source, é possível atingir a capacidade total do Kubernetes. Dentre esses projetos necessários, incluem-se:

- Registro, como o Atomic Registry ou o Docker Registry.
- Rede, como o OpenvSwitch e roteamento de borda inteligente.
- Telemetria, como o heapster, o kibana, o hawkular e o elastic.
- Segurança, como o LDAP, o SELinux, o RBAC e o OAUTH com camadas de multilocação.
- Automação, com a adição de playbooks do Ansible para a instalação e o gerenciamento do ciclo de vida do cluster.
- Serviços, oferecidos em um catálogo variado de conteúdos previamente criados de padrões de aplicações populares.

[Faça uma avaliação gratuita do Red Hat OpenShift](https://www.redhat.com/pt-br/technologies/cloud-computing/openshift2)

------

## Aprenda a linguagem do Kubernetes

Assim como qualquer tecnologia, há vários termos específicos que podem representar uma barreira inicial. Vamos explicar alguns dos termos mais comuns para ajudar você a entender melhor o Kubernetes.

**Master:** a máquina que controla os nós do Kubernetes. É nela que todas as atribuições de tarefas se originam.

**Nó:** são máquinas que realizam as tarefas solicitadas e atribuídas. A máquina mestre do Kubernetes controla os nós.

**Pod:** um grupo de um ou mais containers implantados em um único nó. Todos os containers em um [pod](https://www.redhat.com/pt-br/topics/containers/what-is-kubernetes-pod) compartilham o mesmo endereço IP, IPC, nome do host e outros recursos. Os pods separam a rede e o armazenamento do container subjacente. Isso facilita a movimentação dos containers pelo cluster.

**Controlador de replicações:** controla quantas cópias idênticas de um pod devem ser executadas em um determinado local do cluster.

**Serviço:** desacopla as definições de trabalho dos pods. Os proxies de serviço do Kubernetes automaticamente levam as solicitações de serviço para o pod correto, independentemente do local do pod no cluster ou se foi substituído.

**Kubelet:** um serviço executado nos nós que lê os manifestos do container e garante que os containers definidos foram iniciados e estão em execução.

**kubectl:** a ferramenta de configuração da linha de comando do Kubernetes.

[Aprenda mais. Consulte o glossário completo do Kubernetes.](https://kubernetes.io/docs/reference/)

------

## Uso do Kubernetes em produção

O Kubernetes é uma tecnologia open source. Por isso, ele não conta com uma estrutura de suporte formal em que as empresas podem confiar totalmente. Problemas com a implantação do Kubernetes durante a execução no ambiente de produção podem representar uma grande dor de cabeça para você e os seus clientes.

Para isso, existe o [Red Hat OpenShift](https://www.redhat.com/pt-br/technologies/cloud-computing/openshift2). Essa é uma solução de nível corporativo que oferece o Kubernetes e muito mais. O OpenShift vem com todos os elementos extras que tornam o Kubernetes potente e viável para as empresas, incluindo componentes de registro, rede, telemetria, segurança, automação e serviços. Com o Red Hat OpenShift, os desenvolvedores da sua empresa poderão criar novas aplicações em containers, hospedá-las e implantá-las na cloud. Tudo isso com a escalabilidade, o controle e a orquestração necessários para transformar boas ideias em negócios valiosos de forma rápida e fácil.

Além disso, a maior vantagem dessa solução é que essa plataforma foi desenvolvida e conta com o suporte da Red Hat, a empresa líder global em tecnologia open source.

------

## Veja como o Kubernetes se encaixa na sua infraestrutura

![diagrama do Kubernetes na infraestrutura](https://www.redhat.com/cms/managed-files/kubernetes-diagram-2-824x437.png)

O Kubernetes é executado em um sistema operacional (por exemplo, no [Red Hat Enterprise Linux Container Host](https://www.redhat.com/pt-br/technologies/linux-platforms/old-enterprise-linux)) e interage com pods de containers executados em nós. A máquina mestre do Kubernetes aceita os comandos de um administrador (ou equipe de DevOps) e retransmite essas instruções aos nós subservientes. Essa retransmissão é realizada em conjunto com vários serviços para automaticamente decidir qual nó é o mais adequado para a tarefa. Depois, são alocados os recursos e atribuídos os pods do nó para cumprir a tarefa solicitada.

Portanto, do ponto de vista da infraestrutura, são poucas as mudanças em comparação com a forma como você já gerencia os containers. O controle sobre os containers acontece em um nível superior, tornando-o mais refinado, sem a necessidade de microgerenciar cada container ou nó separadamente. Será necessário realizar algum trabalho, mas em sua maioria trata-se somente de uma questão de atribuir um master do Kubernetes e definir os nós e pods.

### Kubernetes x Docker

A tecnologia do [docker](https://www.redhat.com/pt-br/topics/containers/what-is-docker) ainda realiza as mesmas tarefas do seu objetivo original. Quando o Kubernetes programa um pod para um nó, o kubelet no nó instruirá o docker a iniciar os containers especificados. O kubelet, então, continuamente coleta do docker os status desses containers e agrega as informações no master. O docker insere os containers nesse nó e os inicia e interrompe normalmente. A diferença é que um sistema automatizado solicita que o Docker realize essas tarefas em todos os nós de todos os containers, em vez do administrador fazer essas solicitações manualmente.



### Leia o whitepaper:

- [Uma introdução ao Kubernetes corporativo](https://www.openshift.com/introduction-enterprise-kubernetes?intcmp=701f2000001OMH6AAO)

### Aprenda também:

- [O que é Kubernetes cluster?](https://www.redhat.com/pt-br/topics/containers/what-is-a-kubernetes-cluster)
- [Introdução aos containers Linux](https://www.redhat.com/pt-br/topics/containers)
- [O que é um container Linux?](https://www.redhat.com/pt-br/topics/containers/whats-a-linux-container)
- [Por que escolher a Red Hat para adoção de containers?](https://www.redhat.com/pt-br/topics/containers/why-choose-red-hat-containers)
- [O que é DOCKER?](https://www.redhat.com/pt-br/topics/containers/what-is-docker)
- [Plataforma de aplicações em containers da Red Hat](https://www.redhat.com/pt-br/technologies/cloud-computing/openshift2)
- [Segurança de containers](https://www.redhat.com/pt-br/topics/security/container-security)
- [Red Hat OpenShift X Kubernetes](https://www.redhat.com/pt-br/topics/containers/red-hat-openshift-kubernetes)

## Descubra todas as vantagens dos containers Linux

[Experimente grátis](https://www.openshift.com/container-platform/trial.html)

[Aprenda mais](https://www.redhat.com/pt-br/topics/containers)

[Fale com nossa equipe](https://www.redhat.com/pt-br/contact)

### SOBRE A RED HAT

A Red Hat é líder mundial no fornecimento de soluções empresariais open source. Utilizando uma abordagem de parceria com as comunidades, a Red Hat oferece tecnologias confiáveis e de alto desempenho em Linux, nuvem, containers e Kubernetes. Com serviços premiados de consultoria, treinamento e suporte, ajudamos nossos clientes a definir padrões entre diferentes ambientes, desenvolver aplicações nativas em nuvem, além de integrar, automatizar, proteger e gerenciar ambientes complexos.

- [Informações institucionais](https://www.redhat.com/pt-br/about/company)
- [Oportunidades de emprego](https://www.redhat.com/pt-br/jobs-overview)
- [Escritórios](https://www.redhat.com/pt-br/about/office-locations)
- [Modelo de desenvolvimento](https://www.redhat.com/pt-br/about/development-model)
- [Eventos](https://www.redhat.com/pt-br/events)
- [Sala de imprensa](https://www.redhat.com/pt-br/about/newsroom)
- [Blog](https://www.redhat.com/pt-br/blog)
- [Cool Stuff Store](https://coolstuff.redhat.com/)
- [Diversidade, equidade e inclusão](https://www.redhat.com/pt-br/about/our-culture/diversity-equity-inclusion/statement)
- 

### PRODUTOS

- [Red Hat Ansible Automation Platform](https://www.redhat.com/pt-br/technologies/management/ansible)
- [Red Hat Enterprise Linux](https://www.redhat.com/pt-br/technologies/linux-platforms/enterprise-linux)
- [Red Hat OpenShift](https://www.redhat.com/pt-br/technologies/cloud-computing/openshift)
- [Red Hat OpenShift Data Foundation](https://www.redhat.com/pt-br/technologies/cloud-computing/openshift-container-storage)
- [Red Hat OpenStack Platform](https://www.redhat.com/pt-br/technologies/linux-platforms/openstack-platform)
- [Veja todos os produtos](https://www.redhat.com/pt-br/technologies/all-products)

### FERRAMENTAS

- [Minha conta](https://sso.redhat.com/)
- [Suporte ao cliente](https://access.redhat.com/)
- [Recursos para parceiros](https://connect.redhat.com/)
- [Recursos para desenvolvedores](https://developers.redhat.com/)
- [Treinamento e certificação](https://www.redhat.com/pt-br/services/training-and-certification)
- [Comunidade de aprendizagem](https://learn.redhat.com/)
- [Red Hat Ecosystem Catalog](https://catalog.redhat.com/)
- [Biblioteca de recursos](https://www.redhat.com/pt-br/resources)

### EXPERIMENTE, COMPRE, VENDA

- [Central de avaliação de produtos](https://www.redhat.com/pt-br/products/trials)
- [Red Hat Store](https://www.redhat.com/en/store)
- [Red Hat Marketplace](https://marketplace.redhat.com/)
- [Comprar online (Japão)](https://www.redhat.com/pt-br/about/japan-buy)
- [Encontre um parceiro](http://redhat.force.com/finder/)
- [Contate o setor de vendas](https://www.redhat.com/pt-br/contact)
- [Contate o setor de treinamento](https://www.redhat.com/pt-br/services/training-and-certification/contact-us)
- [Contate a Red Hat Consulting](https://www.redhat.com/pt-br/services/consulting-overview#contact-form)

### COMUNICAÇÃO

- [Entre em contato](https://www.redhat.com/pt-br/contact)
- [Comentários e feedback](https://www.redhat.com/pt-br/feedback-sobre-o-site)
- [Redes sociais](https://www.redhat.com/pt-br/about/social)
- [Newsletter](https://engage.redhat.com/Global-Preference-Center?newsletter=RH-Shares&intcmp=7016000000154xCAAQ)

[![Red Hat](https://www.redhat.com/profiles/rh/themes/redhatdotcom/img/logo.svg)](https://www.redhat.com/pt-br)

© 2021 Red Hat, Inc.

- [Declaração de Privacidade](https://www.redhat.com/pt-br/about/privacy-policy)
- [Termos de uso](https://www.redhat.com/pt-br/about/terms-use)
- [Todas as políticas e diretrizes](https://www.redhat.com/pt-br/about/all-policies-guidelines)
- [Acessibilidade digital](https://www.redhat.com/pt-br/about/digital-accessibility)
- |Preferências de Cookies

[![Red Hat Summit](https://www.redhat.com/cms/managed-files/Logo-Red_Hat-Summit-A-Standard-RGB-02_0.svg)](http://www.redhat.com/summit/)

<iframe class="drift-frame-chat" scrolling="no" title="Drift Widget Chat Window" allow="autoplay; encrypted-media; fullscreen;" frameborder="0" src="https://js.driftt.com/core/chat?region=US&amp;driftEnableLog=false&amp;pageLoadStartTime=1638912872284" style="box-sizing: border-box; display: block; min-width: 0px; max-width: 100%; min-height: 0px; max-height: none; border: none; background: transparent; width: 400px !important; height: 0px;"></iframe>

<iframe class="drift-frame-controller" scrolling="no" title="Drift Widget Icon" allow="autoplay; encrypted-media; fullscreen;" frameborder="0" src="https://js.driftt.com/core?embedId=vtgnfrnufv54&amp;region=US&amp;forceShow=false&amp;skipCampaigns=false&amp;sessionId=db19435f-b376-422d-829c-3b302a00710c&amp;sessionStarted=1638911244.669&amp;campaignRefreshToken=51335e65-b5f5-4a9c-a7ba-3e1f860e4fbc&amp;hideController=false&amp;pageLoadStartTime=1638912872284&amp;mode=CHAT&amp;driftEnableLog=false" style="box-sizing: border-box; display: block; min-width: 0px; max-width: 100%; min-height: 0px; max-height: none; border: none; background: transparent; width: 76px; height: 0px;"></iframe>