# Contêineres

Contêineres são como caixas universais para transporte de mercadorias, mas em T.I eles são um tipo de tecnologia que permite empacotar e executar aplicativos e seus componentes, como bibliotecas e dependências, de maneira rápida e confiável em diferentes ambientes, como computadores desktop, laptops, servidores on premise e nuvem (sim, o negócio é supimpa mesmo). É como se fosse uma caixa que contém tudo o que um aplicativo precisa para funcionar, o que simplifica a distribuição de software e garante que ele funcione da mesma forma em qualquer lugar, facilitando o trabalho dos desenvolvedores e tornando os processos de implantação mais eficientes e escaláveis, vai por mim é muito mais fácil escalar (aumentar e diminuir a quantidade) de contêineres do que máquinas virtuais.

Se você é uma pessoa que entende as coisas de forma visual, eu recomendo [esse vídeo aqui](https://www.youtube.com/watch?v=jv4_sLlGOS0&ab_channel=Alura) para entender o que são contêineres.

Antes de mais nada, é importante você conhecer as diferenças entre Container Engine e Container Runtime. Isso vai fazer toda a diferença no teu aprendizado sobre contêineres daqui em diante.

- **Container Engine**

Software que dispõe de uma interface de linha de comando para criar e deletar imagens de conteiner, fazer upload e download de imagens em registries (repositórios para imagens de contêineres), enviar comando de execução de um conteiner, etc.
Docker é um conteiner engine. Se você tiver ele instalado na sua máquina ou em algum servidor, experimente executar o comando `docker --help`. Um output semelhante a esse, com várias opções de comandos, deve aparecer em seu terminal:
```
$ docker --help

Usage:  docker [OPTIONS] COMMAND

A self-sufficient runtime for containers

Common Commands:
  run         Create and run a new container from an image
  exec        Execute a command in a running container
  ps          List containers
  build       Build an image from a Dockerfile
  pull        Download an image from a registry
  push        Upload an image to a registry
  images      List images
  login       Log in to a registry
  logout      Log out from a registry
  search      Search Docker Hub for images
  version     Show the Docker version information
  info        Display system-wide information

Management Commands:
  builder     Manage builds
  buildx*     Docker Buildx (Docker Inc., v0.11.2)
  checkpoint  Manage checkpoints
  compose*    Docker Compose (Docker Inc., v2.21.0)
  container   Manage containers
  context     Manage contexts
  image       Manage images
  manifest    Manage Docker image manifests and manifest lists
  network     Manage networks
  plugin      Manage plugins
  system      Manage Docker
  trust       Manage trust on Docker images
  volume      Manage volumes

Swarm Commands:
  config      Manage Swarm configs
  node        Manage Swarm nodes
  secret      Manage Swarm secrets
  service     Manage Swarm services
  stack       Manage Swarm stacks
  swarm       Manage Swarm

Commands:
  attach      Attach local standard input, output, and error streams to a running container
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  events      Get real time events from the server
  export      Export a container's filesystem as a tar archive
  history     Show the history of an image
  import      Import the contents from a tarball to create a filesystem image
  inspect     Return low-level information on Docker objects
  kill        Kill one or more running containers
  load        Load an image from a tar archive or STDIN
  logs        Fetch the logs of a container
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  rmi         Remove one or more images
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  wait        Block until one or more containers stop, then print their exit codes

Global Options:
      --config string      Location of client config files (default "/home/daniel/.docker")
  -c, --context string     Name of the context to use to connect to the daemon (overrides DOCKER_HOST env var and
                           default context set with "docker context use")
  -D, --debug              Enable debug mode
  -H, --host list          Daemon socket to connect to
  -l, --log-level string   Set the logging level ("debug", "info", "warn", "error", "fatal") (default "info")
      --tls                Use TLS; implied by --tlsverify
      --tlscacert string   Trust certs signed only by this CA (default "/home/daniel/.docker/ca.pem")
      --tlscert string     Path to TLS certificate file (default "/home/daniel/.docker/cert.pem")
      --tlskey string      Path to TLS key file (default "/home/daniel/.docker/key.pem")
      --tlsverify          Use TLS and verify the remote
  -v, --version            Print version information and quit

Run 'docker COMMAND --help' for more information on a command.

For more help on how to use Docker, head to https://docs.docker.com/go/guides/
```

Além do Docker, existem outros Container Engine: [Buildah](https://github.com/containers/buildah), [Podman](https://docs.podman.io/en/latest/), e [LXC](https://linuxcontainers.org/lxc/introduction/).

- **Container Runtime**

Ok, mas se eu já tenho um Container Engine que faz tudo o que eu quero, porque preciso de Container Runtime?

Ótima pergunta :). Diferente do engine, o Container Runtime é um daemon (processo que fica em execução em background no S.O) que, de fato, faz o trabalho duro de manter os contêineres em execução (e para-los quando receber ocorrer algum erro ou comando), atribui um ID único para cada conteiner, valida a configuração da imagem para criar o conteiner, isola o conteiner do host através da namespace do kernel, configura o filesystem para cada conteiner, etc.

Você percebe que o runtime basicamente executa as ordens do engine, que por sua vez são dadas através da linha de comando do engine. Capiche?

Você pode ser levado a comparar contêineres com máquinas virtuais. Não caia nessa!

Embora o contêineres e as máquinas virtuais tenham um propósito semelhante, seu desempenho, portabilidade e suporte a sistemas operacionais diferem significativamente.

A principal diferença é que os contêineres compartilham o sistema operacional do host, enquanto as máquinas virtuais também têm um sistema operacional convidado sendo executado no sistema host. Esse método de operação afeta o desempenho, as necessidades de hardware e o suporte do SO. Confira a tabela abaixo para uma comparação detalhada.


|     | Conteiner | Máquina Virtual |
| --- | --- | --- |
| **SO**                            | SO compartilhado entre contêineres                                        | Novo SO para cada MV
| **Segurança**                     | Menos seguro¹ porque o sistema operacional e o kernel são compartilhados  | Mais seguro, pois as MVs não compartilham o sistema operacional
| **Desempenho**                    | Desempenho rápido mesmo com vários contêineres                            | Mais máquinas virtuais equivalem a desempenho menos estável
| **Tempo de inicialização**        | Rápido (segundos)                                                         | Lento (minutos)
| **Necessidades de memória**       | Leve                                                                      | Requer muita memória
| **Necessidades de armazenamento** | Geralmente megabytes                                                      | Geralmente gigabytes 
| **Portabilidade**                 | Fácil de implantar em diferentes ambientes                                | Difícil portar uma MV para outro sistema

1 -  Claro que há várias boas práticas para tornar uma aplicação em contêineres mais segura. Mas essencialmente, as máquinas virtuais estão mais isoladas umas das outras e do sistema host do que os contêineres. Isso ocorre porque as máquinas virtuais, não compartilham diretamente o kernel ou outros recursos com seu host.

**Fontes:**
- https://www.hostinger.com.br/tutoriais/o-que-e-docker
- https://www.weave.works/blog/a-practical-guide-to-choosing-between-docker-containers-and-vms
##
> [!NOTE]
> Esse tópico vai ter apenas dois links. Sim! e é tudo que você precisa 😉. O primeiro é um vídeo excelente do Fábio Akita caso você queria entender as entranhas dos contêineres. O segundo é um vídeo que eu criei para o meu canal [DualBoot](https://www.youtube.com/@DualBootTech?sub_confirmation=1) no Youtube onde faço uma lista dos **MELHORES CURSOS DE DOCKER NO YOUTUBE**. Aprecie sem moderação hehe.
##
## Recursos de Estudo:
### Obrigatórios:
- [Entendendo Funcionamento de Containers](https://www.youtube.com/watch?v=85k8se4Zo70)
- [Os melhores cursos de docker do Youtube](https://youtu.be/pVVL0CM6eWg?si=_xqBSq594LkrnD2T)
