# AWS-Workflw
Serviços Intermediários e Avançados 
Amazon Lambda – AWS Lambda
O AWS Lambda é um serviço de computação que executa seu código em resposta a eventos e gerencia automaticamente os recursos de computação, tornando-se a maneira mais rápida de transformar uma ideia em aplicações de produção modernas e com tecnologia sem servidor.
Serveless não tem servidor por trás.
O Lambda executa seu código em uma infraestrutura de computação de alta disponibilidade e executa toda a administração dos recursos computacionais, incluindo manutenção do servidor e do sistema operacional, provisionamento e escalabilidade automática da capacidade e registro em log do código. 
Não temos aesso ao servidor porque ele não existe, e ele executa o codigo em uma infraestrutuura de computação de alta disponibilidade. Ele tem o inuito de receber informação e passar pra  frente. 
Serverless: sem servidor é a arquitetura nativa da nuvem que permite transferir mais das suas responsabilidades operacionais à AWS, aumentando a agilidade e a inovação. 
Custo: 0,20 USD por 1 milhão de solicitações
AWS Lambda oferece vários benefícios, incluindo:
Execução sob demanda: o Lambda executa seu código somente quando necessário e é cobrado apenas pelo tempo de computação usado.
Escalonamento automático: o Lambda é dimensionado automaticamente com base no número de eventos recebidos, eliminando a necessidade de gerenciamento manual do servidor.
AWS Lambda oferece vários benefícios, incluindo:
Execução sob demanda: o Lambda executa seu código somente quando necessário e é cobrado apenas pelo tempo de computação usado.
Escalonamento automático: o Lambda é dimensionado automaticamente com base no número de eventos recebidos, eliminando a necessidade de gerenciamento manual do servidor.

Amazon ECS e EKS - Serviços de contêineres gerenciados
Microservices - Antes de tudo, falar em serviços como ECS e EKS que são serviços de containers e trabalham com microserviços, temos que entender o que vem a ser microserviços!
ECS - Amazon Elastic Container Service
O ECS é um serviço gerenciado de orquestração de contêineres que permite executar, interromper e gerenciar facilmente contêineres em um cluster. (orquestrador de conteiner).

O ECS permite executar aplicações em contêineres em uma arquitetura de microservices, utilizando a escalabilidade, segurança e o desempenho da infraestrutura da AWS.

As principais características do ECS são:
- Simples Gerenciamento: podemos automatizar o gerenciamento de clusters de contêineres.
- Escalabilidade: permite escalar de forma automática com base na demanda.
- Facil Integração: permite integrar facilmente com outros serviços da AWS, como IAM, VPC, CloudWatch, entre outros.
- Segurança: podemos aplicar políticas de segurança para controlar o acesso aos contêineres.

Use Case:
Vamos pensar agora sobre um exemplo de implementação.
Veja este desenho de arquitetura de microserviços.

Microserviços em Contêineres: cada componente do aplicativo (catálogo, carrinho, pagamentos, etc.) é empacotado em um contêiner Docker.

Definição de Tarefas e Serviços no ECS: definimos uma tarefa para cada contêiner e configuramos os serviços no ECS para manter a disponibilidade desejada para cada contêiner.

Escalabilidade Automática: configuramos as políticas de escalabilidade automática para aumentar ou diminuir o número de contêineres com base na carga de trabalho (por exemplo, aumentar contêineres durante promoções).
Monitoramento e Logging: utilizamos o Amazon CloudWatch para monitorar a performance e logs dos contêineres para troubleshooting e análise de desempenho.

ECS: serviço de orquestração de contêineres que ajuda a gerenciar contêineres do Docker em um cluster.
Elastic Container Registry (ECR): serviço de registro de contêiner gerenciado para armazenar, 
gerenciar e implantar imagens do Docker. (repositório de container).

Porquê usar ECS?
O Amazon ECS é ideal para tarefas em execução por mais de 15 minutos ou se precisar executar código fora das regiões da AWS. 

O Amazon ECS oferece experiências opinativas sobre coisas como redes e observabilidade, mas pode ser personalizado de acordo com suas necessidades.

EKS - Elastic Kubernetes Service (EKS)
O AWS Elastic Kubernetes Service (EKS) é um serviço gerenciado que facilita a execução do Kubernetes na AWS sem a necessidade de instalar e operar seu próprio cluster Kubernetes. 

O EKS oferece uma forma segura, confiável e escalável de gerenciar contêineres usando Kubernetes, uma das plataformas de orquestração de contêineres mais populares.
O que é o Kubernetes Service?
O Kubernetes auxilia no ajuste do tamanho de um cluster necessário para executar um serviço. (POD).

Permitindo escalonar automaticamente seus aplicativos, para mais e para menos, com base na demanda e executá-los com eficiência.

O AWS EKS é mais adequado para organizações que já utilizam o Kubernetes ou estão considerando implementar essa tecnologia para aproveitar a força da infraestrutura da AWS e, ao mesmo tempo, reduzir os esforços vinculados à manutenção do ambiente Kubernetes.

Pois a gestão de um cluster Kubernetes é muito complexa.
Amazon ECS VS Amazon EKS
Vamos agora ver a diferença entre os dois serviços.
À medida que as arquiteturas baseadas em micro serviços se tornaram mais populares, houve um aumento significativo nos workloads e serviços de contêiner em nuvem.
Por isto escolher entre um serviço e outro depende muito do tipo de serviço e arquitetura escolhida.
Elastic Container Service (ECS), serviço proprietário de orquestração de contêineres gerenciados da AWS para execução de aplicativos em contêineres em escala.
No back-end usa a tecnologia sem servidor (Fargate), que elimina a carga de gerenciamento. 
Elastic Kubernetes Service (EKS), utiliza o Kubernetes, serviço desenvolvido pela Google. É uma das plataformas de orquestração de contêineres mais populares disponíveis.
O EKS é o serviço Kubernetes gerenciado da AWS, que atende aos clientes que preferem o K8s para orquestração de contêineres. 
Conclusão:
O ECS e o EKS oferecem muitos dos mesmos recursos necessários para implantar e gerenciar contêineres no AWS, mas há diferenças sutis que podem ajudá-lo a escolher qual é o melhor para a sua empresa.
O ECS é adequado para organizações que estão começando a usar contêineres com arquiteturas de baixa ou média complexidade.
O EKS é voltado para casos de uso corporativo, atendendo a aplicativos complexos baseados em microsserviços distribuídos.
Embora ambos os serviços ofereçam flexibilidade em suas cargas de trabalho em contêineres, a melhor opção depende do caso de uso-alvo da sua organização, da maturidade em contêineres, do tamanho da equipe e da importância da facilidade de uso.
Amazon SNS (Simple Notification Service)
Serviço de mensagens assíncronas, disponível e seguro para notificações de mensagens entre aplicativos distribuídos e microserviços.
Ele permite o envio de notificações push para dispositivos móveis, mensagens de texto, e-mails ou integrações com outros serviços da AWS, como o Amazon SQS ou o AWS Lambda.
O SNS é dividido em tópicos e assinaturas, na imagem temos uma visão macro com 3 subscribers no mesmo Pubisher (publicador) Serviço de mensagens assíncronas, disponível e seguro para notificação de eventos.

Tópicos: são pontos de acesso entre o Publisher (publicador) e o Subscriber (inscrito). 
EX: Tópico = carteiro / Publisher = correio / Subscriber = casa.
Um tópico pode ser dividido em 2 tipos.
Tipo Fifo ou tipo Padrão e isto é configurado no Subscriber que é onde recebe a mensagem.
Tipo Fifo (first in/first out), possui o limite de 300 publicações por segundo. Garantindo a entrega da primeira mensagem que entra, primeira mensagem que sai.
Tipo Padrão, utilizado na maioria dos casos e é muito mais flexível e menos rigoroso como o Fifo.
Ele não visa ordenar por ordem de chegada, o throughput de publicações. 
Desta forma ele não garante a ordem exata das mensagens, podendo ser entregues mais de uma vez.
EX: Entra A – B – C – D SAI  A – B – C – D
Amazon SQS (Simple Queue Service)
Não muito diferente do SNS o Amazon SQS também é um sistema de entrega de mensagens.
Muito utilizado para integração entre sistemas ou seja, o SQS desacopla os componentes de um aplicativo, permitindo que interajam de forma assíncrona.
O SQS oferece suporte a várias filas, incluindo os tipos Padrão e FIFO (First-In-First-Out).
Trabalha com os consumidores e quando uma mensagem é recebida, ela se torna invisível para outros consumidores por um período de tempo limite especificado.
O SQS suaviza o tráfego de rajadas e garante um processamento consistente.
EX: Entra A – B – C – D SAI  C – A – D – B
Amazon SQS X Amazon SNS
A escolha entre o Amazon SNS e o SQS exige que você tome uma decisão em relação ao gerenciamento das suas mensagens.
O Amazon SNS funciona como um sistema de transmissão, o que o torna ideal para alertar rapidamente os usuários de um determinado produto.

O Amazon SQS funciona como uma fila de mensagens, fornecendo dados a vários componentes de aplicativos de forma ordenada e independente.
Para comunicação com clientes, de forma instantânea, o melhor é utilizar o Amazon SNS.
Para comunicação entre sistemas de diferentes áreas do seu aplicativo e de forma organizada, o melhor sera o Amazon SQS.
AWS Step Functions 
Orquestrador de serviço, low code.
Nada mais é do que um contrutor viisual para criar fluxos de trabalho.
Auxlia você a contruir rotinas. Chamar recursos, dfinir times entre outros.
Não reciso colocar a mão no código, tem pouco.
Criar do jeitoo que quero e fazer funcinar de acordo com o que preciso.
Posso ter recursos criador ou não (workflow).
Para a implantação utiliza o cloudformation que é um serviço de provisionamento da nuvem.
GitHub Quick Start - Repositório com Link para Aulas de Git e GitHub  
GitBook: Formação GitHub Certification - Material textual sobre GitHub 
Documentação do GitHub - Guia completo para uso do GitHub  
GitHub Markdown - Guia específico para Markdown no GitHub  
