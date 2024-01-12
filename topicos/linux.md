# Linux 🐧

Conhecer o essencial de Linux e se virar bem no terminal é a primeira etapa a ser conquistada para você se tornar um Engenheiro DevOps de sucesso. Eu costumo falar que antes de ser um bom profissional DevOps, primeiro você precisa ser um ótimo SysAdmin no Linux.

## Afinal, o que é Linux?

Muitas pessoas se referem ao [Linux](https://github.com/torvalds/linux) como um Sistema Operacional assim como Windows e MacOs, porém não é bem assim. O Linux é, na verdade, um Kernel. 

Kernel é como o cérebro de um Sistema Operacional (Windows, Ubuntu, MacOs), ele atua como o gerente principal que controla todas as operações e recursos do computador. 

Imagine o kernel como o maestro de uma orquestra, coordenando cada instrumento para tocar em harmonia. Esses "instrumentos" são o hardware (como processador, memória e dispositivos) e o software (os programas que você usa na máquina). 

Quando você interage com seu computador, o kernel está lá, garantindo que tudo funcione sem problemas, permitindo que aplicativos e hardware se entendam e trabalhem juntos de maneira eficiente.

Há literalmente dezenas de Sistemas Operacionais que usam o kernel do Linux como "maestro". Quase sempre você ta usufruindo dessa onipresença do Linux e nem percebe.

Duvida?! Então aqui vai algumas estatisticas :sunglasses::
- 47% dos desenvolvedores profissionais usam sistemas operacionais baseados em Linux. (Estatista)
- O Linux alimenta 39,2% dos sites cujo sistema operacional é conhecido. (W3Techs)
- O Linux alimenta 85% dos smartphones. (Hayden James)
- Linux, o terceiro sistema operacional de desktop mais popular, tem uma participação de mercado de 2,09%. (Estatista)
- O tamanho do mercado Linux em todo o mundo chegará a US$ 15,64 bilhões até 2027. (Fortune Business Insights)
- Os 500 supercomputadores mais rápidos do mundo rodam em Linux. (Preto)
- 96,3% dos um milhão de servidores da Web estão executando o Linux. (ZDNet)
- Hoje, existem mais de 600 distribuições Linux ativas. (Tecmint)

Fonte: [o-ano-do-linux-no-desktop-ainda-chegara](https://www.edivaldobrito.com.br/o-ano-do-linux-no-desktop-ainda-chegara/)


Nesse guia vou sugerir você realizar teus estudos e exercícios no **Ubuntu**, porque muitos servidores rodam nele por conta da sua segurança e robustez. Eu mesmo uso a versão desktop desde sempre hehe.

Então segura na mão do [Tux](https://pt.wikipedia.org/wiki/Tux) 🐧 e vai na fé :)

## Instalação
Vou sugerir algumas formas de você usar o Ubuntu na tua máquina:

**Método 1** - Criar uma VM (máquina virtual) do Ubuntu, assim você não vai precisar desinstalar o Windows. Recomendo você assistir esse [vídeo](https://www.youtube.com/watch?v=xzOmCxZSQWw&list=PLAp37wMSBouCqJnY-Qck_XDwplEud3ELc&ab_channel=HardwareRedesBrasil) aqui para saber como criar uma máquina virtual do Ubuntu pelo Virtual Box.

**Método 2** - [Instalar WSL2 no Windows](https://www.youtube.com/watch?v=qlLcnSvG1rA). O Subsistema do Windows para Linux (WSL2) é um recurso do Windows que permite executar um ambiente Linux (como Ubuntu, OpenSUSE, Kali, Debian, Arch Linux etc) em sua máquina Windows, sem a necessidade de uma máquina virtual separada ou DualBoot.

**Método 3** - Fazer o DualBoot do Windows e Ubuntu. Dualboot é basicamente manter dois sistemas operacionais na mesma máquina, porém você só pode usar um por vez. Primeiro você precisa ter um [pendrive bootavel](https://www.youtube.com/watch?v=fekbCvIGwSI&ab_channel=ROVEEb) com o Ubuntu e depois fazer o processo de DualBoot. Esse [vídeo aqui](https://www.youtube.com/watch?v=VK4eCi7ktCE&ab_channel=LSRSolu%C3%A7%C3%B5es) vai te ajudar com isso. 
> [!CAUTION]
> **Fique atento que o método 3 é avançado, e se não for feito de forma correta pode causar perda dos dados da tua máquina, então faça um backup antes. Se você não estiver seguro, siga o método 1.**

**Método 4** - Formatar a máquina instalando o Linux Ubuntu. Esse método é diferente do DualBoot que mantém o Ubuntu e Windows na mesma máquina. Nesse caso aqui você vai manter somente o Ubuntu. Caso ainda não esteja preparado para sair da matrix :wink:, recomendo seguir o método 1, 2 ou 3.


## Recursos de estudo:
- [LPIC-1 PDF](https://learning.lpi.org/pdfstore/LPI-Learning-Material-101-500-pt.pdf) <sup>GRÁTIS</sup>
- [Curso de Linux Ubuntu Básico](https://www.youtube.com/watch?v=aW4Owxgcvq4&list=PLnDvRpP8BnezDTtL8lm6C-UOJZn-xzALH&index=1&ab_channel=MatheusBattisti-HoradeCodar) <sup>YOUTUBE</sup>
- [LinuxFoundationX: Introduction to Linux](https://www.edx.org/learn/linux/the-linux-foundation-introduction-to-linux?index=product&queryID=94f1b3b8dd11b444494d8dcfb10ece99&position=18&results_level=second-level-results&term=&objectID=course-5a631d1c-cb20-4cfc-9b49-1cc9c8fc981e&campaign=Introduction+to+Linux&source=edX&product_category=course&placement_url=https%3A%2F%2Fwww.edx.org%2Fsearch)<sup>GRÁTIS - INGLÊS</sup>
- [Linux Essentials](https://www.netacad.com/courses/os-it/ndg-linux-essentials?ref=itsfoss.com)<sup>GRÁTIS - INGLÊS</sup>
