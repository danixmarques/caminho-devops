# Kubernetes

> [!NOTE]
> Um pré-requisito para ingressar nesse tópico é ter conhecimento teórico e prático sobre [containers](./container.md), além de entender seus fundamentos e aplicações. Sem esse conhecimento você não vai entender *bulhufas* desse tópico :).

> [!CAUTION]
> Outra observação importante: [O Kubernetes anunciou em dezembro de 2020](https://kubernetes.io/blog/2020/12/02/dont-panic-kubernetes-and-docker/) que iria descontinuar o Docker Runtime porque o Docker não foi projetado para ser o Runtime do Kubernetes.

O Docker não faz download e nem inicia contêineres. Em vez disso, é um componente chamado Containerd (Container Runtime do Docker) que faz essas coisas.

Mas "carma" que isso não é o fim do mundo. Ainda é possível usar imagens de container construídas pelo Docker, porque ele segue o padrão de imagem chamado Container Runtime Interface (CRI). Então qualquer imagem que for construída por um Container Engine que segue o padrão (CRI) vai executar no Kubernetes sem problemas.

"Pow! Então se eu não posso mais usar o Docker como Runtime do Kubernetes, o que eu uso então?"
Bom, nem só de Docker vivem os runtimes. Vou deixar algumas alternativas muito boas:
- [CRI-O](https://cri-o.io/)
- [Containerd](https://containerd.io/)


Alguns outros Container Engine que também seguem o padrão (CRI):
- [Buildah](https://github.com/containers/buildah)
- [Podman](https://docs.podman.io/en/latest/)
- [LXC](https://linuxcontainers.org/lxc/introduction/)

###
Observações feitas, vamos adiante.

Aaaaaaah o [Kubernetes](https://kubernetes.io/pt-br/), ou k8s (o 8 representa o número de letras entre o "K" e o "s". Lê-se "queits") para os mais intímos, é a ferramenta de orquestração de containeres mais popular atualmente.

Com a ampla adoção de containeres entre as organizações, sejam elas startups ou big techs, o Kubernetes, se tornou o padrão de fato, para implantar e operar aplicativos em container.  

Originalmente desenvolvido no Google e lançado como código aberto em 2014, a versão v1.0 (versão estável) do Kubernetes foi lançado em 21 de julho de 2015. Juntamente com o lançamento, o [Google](https://cloud.google.com/learn/what-is-kubernetes?hl=pt-br) fez uma parceria com a Linux Foundation para formar a Cloud Native Computing Foundation (CNCF) e ofereceu Kubernetes como uma tecnologia de base.

Diferente de 7 anos atrás, saber Kubernetes hoje em dia já não é mais um diferencial para um Engenheiro Devops, seja qual for a senioridade. Dito isso aprender e dominar essa ferramenta é uma obrigação. É praticamente impossível encontrar vagas de emprego na área de DevOps que não exijam conhecimento sobre containeres e pelo menos uma ferramenta de orquestração de containeres, que quase sempre será o Kubernetes.

Alguns outros orquestradores de containeres são Docker Swarm, Hashicorp Nomad, Apache Mesos, e Rancher. E é claro que provedores de nuvem como [AWS](https://aws.amazon.com/pt/eks/), [Azure](https://azure.microsoft.com/pt-br/products/kubernetes-service), e [Google Cloud](https://cloud.google.com/kubernetes-engine?hl=pt-BR) também oferecem o Kubernetes de forma gerenciada que acaba simplificando a criação e operação dos clusteres de forma escalável e com alta disponibilidade.

> [!NOTE]
> Aprender Kubernetes pode ser um desafio, pois é uma ferramenta com muitos componentes diferentes que performam papeis bem específicos dentro um cluster do Kubernetes. O conselho que te dou é, primeiro, antes de tudo, aprender o papel de cada componente do Kubernetes, se possível até decore, porque isso vai te ajudar demais ao administrar os clusteres, especialmente no processo de dubugging. O que com certeza você vai fazer bastante :).


## **Recursos de estudo:**
- [O que é Kubernetes](https://www.youtube.com/watch?v=1qmaMaOygjU&ab_channel=FullCycle)<sup>YOUTUBE - PORTUGUÊS</sup>
- [Curso de Introdução ao Kubernetes](https://www.youtube.com/watch?v=RuNTvYejG90&list=PLXzx948cNtr8XI5JBemHT9OWuYSPNUtXs&index=1&ab_channel=InsightLab)<sup>YOUTUBE - PORTUGUÊS</sup>
- [PRIMEIRA LIVE - MÊS DO KUBERNETES](https://www.youtube.com/watch?v=-i0rgPdpc2A&t=6101s&ab_channel=LINUXtips)<sup>YOUTUBE - PORTUGUÊS</sup>
- [ÚLTIMA LIVE - MÊS DO KUBERNETES](https://www.youtube.com/watch?v=BJmKaf7w_eQ&t=1219s&ab_channel=LINUXtips)<sup>YOUTUBE - PORTUGUÊS</sup>
- [Kubernetes for the Absolute Beginners](https://www.youtube.com/watch?v=QJ4fODH6DXI&list=PL2We04F3Y_43dAehLMT5GxJhtk3mJtkl5&ab_channel=KodeKloud)<sup>YOUTUBE - INGLÊS</sup>
- [Descomplicando o Kubernetes](https://livro.descomplicandokubernetes.com.br/pt/)<sup>HTML BOOK - PORTUGUÊS</sup>

###
Eu fiz esse curso em 2019, mas tem muito conteúdo atualizado, se você não tem problema com inglês, eu super recomendo. Porque é excelente.
- [Certified Kubernetes Administrator (CKA) with Practice Tests](https://www.udemy.com/course/certified-kubernetes-administrator-with-practice-tests/)<sup>UDEMY - INGLÊS</sup> 
