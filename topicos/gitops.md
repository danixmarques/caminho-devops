# GitOps 

"Fala sério, além de DevOps tem GitOps também?! Daqui a pouco vamos ter OpsOps."

Eeeeeeh pois é, a industria cria esses termos e temos que correr para entender o que são, e como nos afetam como profissionais e estudantes de tecnologia. Mas felizmente esse temos já está totalmente integrado nas práticas DevOps, mas ao mesmo tempo possuem definições diferentes.

Mas antes de de matar tua curiosidade sobre mais um "Ops", vou separar alguns parágrafos a seguir para explicar o que é Git. Porque o tal do GitOps simplesmente não pode existir sem o Git.

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExaGZoNzJxdTFkanEwOHJ2OTNrdzdwbnRxbm9ndGZrejgwYWs5Z29vZiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/75ZaxapnyMp2w/giphy.gif)

## Breve história do Git
Git é um sistema de controle de versão distribuído onde vários colaboradores podem contribuir no mesmo repositório de código ao mesmo tempo. Foi criado em 7 de abril de 2005 por [Linus Torvalds](https://twitter.com/Linus__Torvalds), o mesmo criador do Linux (Te amo tio Totô <3). Quando Torvalds e a comunidade estavam desenvolvendo o [Kernel do Linux](https://github.com/torvalds/linux), o [BitKeeper](http://www.bitkeeper.org/) era a ferramenta usada para registrar e manter todas as contribuições da comunidade. 

Tudo estava indo muito bem entre Torvalds e BitKeeper, até que a lincença da BitKeeper mudou, e Torvalds teria que pagar a licença para continuar o desenvolviment do Kernel Linux.

Torvalds não ficou muito feliz com a ideia, e falou "Quer saber?! Vou criar meu próprio versionador de código". Então foi aí que Torvalds começou a desenvolver o Git. A ferramenta é tão popular atualmente que é usada por 89.04% do mercado devido à sua velocidade, eficiência e capacidade de lidar com projetos de grande escala. Ele permite que várias pessoas trabalhem no mesmo projeto simultaneamente, mantendo um histórico detalhado de todas as alterações feitas ao longo do tempo. 

Além disso, o Git oferece recursos poderosos, como ramificação e mesclagem de código, que facilitam o trabalho colaborativo e a experimentação com diferentes versões do código. Essas características tornaram o Git uma ferramenta indispensável para desenvolvedores de software em todo o mundo, contribuindo para sua popularidade atual.

O próprio GitHub é uma ferramenta feita para armazenar e compartilhar projetos de desenvolvimento de software através do Git 😉

<img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbnpoOGpvcXJ2bzYxZWh3d3RveWY3MnY4YnpxcjllbGptZGg5amk1YSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/KzJkzjggfGN5Py6nkT/giphy.gif" width="250" height="250" />

## Agora vamos adicionar o "Ops"
GitOps é uma abordagem para gerenciar infraestrutura e aplicativos de software usando o Git como fonte de verdade. Na prática, isso significa que todas as alterações na infraestrutura ou no código são versionadas e controladas pelo Git. Por exemplo, em um ambiente GitOps, se um desenvolvedor deseja implantar uma nova versão de um aplicativo, ele simplesmente faz um commit e um push para um repositório Git específico, e as ferramentas de automação (como o Flux ou ArgoCD) detectam essa alteração e automaticamente aplicam as mudanças no ambiente de produção. Isso traz benefícios significativos, como maior rastreabilidade, consistência e segurança. Uma empresa pode se beneficiar do GitOps ao ter uma visão clara do estado da infraestrutura em todos os momentos, permitindo atualizações rápidas e consistentes, além de facilitar a colaboração entre equipes de desenvolvimento e operações.

Embora GitOps compartilhe semelhanças com DevOps, há diferenças importantes entre os dois conceitos. Ambos visam melhorar a colaboração entre desenvolvimento e operações, automatizar processos e promover uma cultura de entrega contínua. No entanto, enquanto DevOps se concentra mais nas práticas e cultura organizacional para alcançar esses objetivos, GitOps adiciona uma camada de automação mais específica, utilizando o Git como a fonte única de verdade para a infraestrutura e o código da aplicação. Em resumo, enquanto o DevOps é mais amplo e aborda a cultura e os processos, o GitOps é uma implementação específica de DevOps que se baseia no controle de versão do Git para gerenciar a infraestrutura e as aplicações.
