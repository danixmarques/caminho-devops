# Caminho DevOps (Work in progress)
Um guia objetivo de estudo, em sua maioria com conteúdos gratuítos, para que você se torne um Engenheiro Devops supimpa. 

Indicado para quem está:
- Iniciando seus estudos em DevOps
- Em transição de carreira para T.I para atuar como DevOps
- Profissionais de outras áreas de T.I que querem se familiarizar com DevOps

Beleza, agora você sabe pra quem é esse material de estudo, mas antes de começarmos a estudar as ferramentas e habilidades que um profissional Devops precisa saber, vamos entender um pouco dos conceitos que abrangem essa função supimpa dentro da engenharia de software.


## O que é esse tal de DevOps
A princípio, vamos focar no básico. 

DevOps é a fusão das palavras **"Desenvolvimento" + "Operações"**, é uma abordagem colaborativa cujo objetivo é aumentar a eficiência e a agilidade no desenvolvimentos de sistemas.

O conceito surgiu no início dos anos 2000 como uma resposta à crescente necessidade de superar as lacunas (e muitas tretas) entre times de desenvolvimento e operações. Embora não tenha um único criador, [Patrick Debois](https://twitter.com/patrickdebois) se destaca como um figura que fomentou o movimento Devops desde do início. Ele organizou a primeira conferência, chamada 'DevOpsDays', na cidade de Gante, Bélgica, em 2009 proporcionando um fórum para a comunidade discutir e disseminar práticas colaborativas. Foi nesse mesmo em que o termo DevOps foi cunhado.

Como nada se cria do nada. DevOps se apoia fortemente em outras metodologias como: Lean, Teoria da Restrições, O Sistema de Produção Toyota, e muitos outros.

Quando comecei a trabalhar como DevOps em 2018, eu não entendia muito bem o conceito de DevOps. Era um movimento? Uma cultura? Um conjunto de práticas?

Depois de alguns meses criando pipelines de deployment, criando servidores na nuvem e no VMWare, gerenciando clusters de Kubernetes e muitas outras tarefas que englobam a tecnologia da informação, eu passei a acreditar que "aquilo" que eu estava fazendo era ser um "DevOps".

Embora o termo "DevOps" tenha sido cunhado por Patrick Debois, o mercado sempre dá um jeitinho de alterar o significado e papel relacionado a esse termo dependendo da época e do momento. DevOps passou a ser um profissional que faz tudo isso que mencionei (e muito mais) no parágrafo anterior.

Mas será que é só isso mesmo? Então todo esse hype de DevOps foi só para criar um novo papel dentro de um time e fazer essa pessoa sair criando toda a infraestrutura necessária (em especial, na nuvem) que um sistema precisa para chegar até o ambiente produtivo?

Essas são algumas daquelas "perguntas da alma" que buscam trazer à luz verdades que ficam esquecidas por um tempo até um ser corajoso começar a "cavucar" em todos os terrenos possíveis por uma resposta mais eficaz.

Dito isso, onde melhor encontrar a resposta para o que é DevOps do que nas palavras do homem que cunhou o termo?

Em 2021, Patrick Debois fez um breve post aqui no LinkedIn explicando o que é "DevOps":

"Minha definição atual de Dev*Ops: tudo o que você faz para superar o atrito criado pelos silos... Todo o resto é engenharia simples." - Patrick Debois

É isso, claro como água. Até mesmo o meu eu de 2018 entenderia essa definição se lhe fosse apresentada.

"Ah, mas isso foi em 2021, T.I. está em constante mudança, essa definição nem deve ser a mesma hoje em dia."

Ou será que não? 😏

Em uma entrevista no final de 2023, Patrick foi questionado sobre o que realmente seria "DevOps" e ele lançou a braba novamente:

"Tentei resumir isso uma vez em um tweet: DevOps trata de remover o atrito entre silos. Todo o resto é engenharia." - Patrick Debois

Interessante, não? Perceba que ele fala em "remover atrito entre silos". Os silos (Dev, Ops, Data, Sec, etc.) sempre irão existir. No entanto, todos podemos remover atritos, todos podemos ser facilitadores, todos podemos remover barreiras e obstruções sejam físicas ou comportamentais que podem impedir que entregas sejam feitas. Não importando o time em que estamos e o papel que exercemos.

Isso é DevOps na sua mais pura essência.

Além disso, DevOps está estabecido sobre 4 princípios e práticas essencias:
- Comunicação não violenta
- Colaboração
- Automação
- Monitoramento & Telemetria

Interessante, não? Caso queria expandir um pouco mais a tua visão sobre DevOps eu recomendo esses dois vídeos abaixo.
- [O que é DevOps em Menos de 7 min](https://www.youtube.com/watch?v=5fQJC9iLCbE) (7 minutos)
- [O que é DevOps?](https://www.youtube.com/watch?v=HzX6ZhmUjoE) (25 minutos) - Esse vídeo é um pouco antigo, mas é muito esclarecedor. O [Jefferson](https://twitter.com/badtux_) manja demais.
- [What is DevOps? REALLY understand it | DevOps vs SRE](https://www.youtube.com/watch?v=0yWAtQ6wYNM) (35 minutos - Inglês)

> [!NOTE]
> **Aproveita e se inscreve no meu também :point_down:. De nada :).**

<figure>
<a href="https://www.youtube.com/@DualBootTech?sub_confirmation=1" target="_blank"><img src="imgs/subscribe.jpg" width="300"></a>
<br>
<figcaption>Créditos da imagem: <a href="https://br.freepik.com/vetores-gratis/botao-inscreva-se-e-siga-me-para-o-seu-canal-do-youtube-vetor_66612348.htm#query=png%20subscribe&position=4&from_view=search&track=ais&uuid=fb1ab6b5-1e87-48df-b433-45a321f1e006">Imagem de starline</a> no Freepik</figcaption size="10">
</figure>

## Supimpa! Assisti os vídeos, e agora?
Parabéns por ter assistido os vídeos introdutórios. Estou torcendo para que não desista, a parte boa ainda nem começou hehe

![](https://www.reactiongifs.com/r/cheering_minions.gif)


Para facilitar tua navegação nesse guia, eu vou separar cada tópico em um arquivo .md diferente nesse mesmo repositório. Segue a sequência que eu sugiro que você siga:
> [!NOTE]
> **Caso você já tenha conhecimento suficiente em algum tópico, sinta-se a vontade para avançar para os próximos.**

1 - [Linux](topicos/linux.md)

2 - [Bash Script](topicos/bash.md)

3 - [Redes](topicos/redes.md)

4 - [GitOps](topicos/gitops.md)

5 - [Contêineres](topicos/container.md)

6 - [Kubernetes](topicos/k8s.md)

7 - [Ansible](topicos/ansible.md)

8 - [Cloud Provider (AWS)](topicos/aws.md)
