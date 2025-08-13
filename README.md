# Projeto de Interface Humano-Computador

Projeto apresentado ao Centro Universitário [FEI](https://portal.fei.edu.br/), como parte dos requisitos necessários para aprovação na disciplina de Interface Humano-Computador (CC8122) do curso de Ciencia da Computação, orientado pelo Prof. Dr. [Fagner de Assis Moura Pimentel](https://github.com/fagnerpimentel).

Este projeto se baseia no Trabalho de Conclusão de Curso (TCC) entitulado **Título do TCC** sob orientação do Professor **Nome do Orientador** e desenvolvido pelos seguintes alunos:

- Nome: Gustavo Gomes Barbosa | RA: 24.122.061-5
- Nome: Pedro Munhoz Rosin | RA: 24.122.013-6
- Nome: Alan Daiki Suga | RA: 22.125.094-7

## Resumo

O presente trabalho propõe o desenvolvimento de uma ferramenta automatizada para a geração de datasets de expressões faciais humanas, com foco na identificação de sentimentos e emoções de jogadores durante sessões de jogos digitais. A ferramenta será capaz de capturar, em tempo real, imagens da face do jogador a partir de uma webcam, processá-las e classificá-las segundo suas expressões emocionais predominantes, utilizando modelos de reconhecimento facial baseados em aprendizado profundo (Deep Learning), especificamente o modelo DeepFace.

## Introdução

 <!--
 
- Apresente o propósito do produto ou serviço e quais são os principais benefícios que ele oferece aos usuários.
- Identifique os problemas ou necessidades que o produto ou serviço resolve ou satisfaz.
- Liste as características e funcionalidades do seu produto ou serviço de forma detalhada.
- Liste as tecnologias e ferramentas computacionais que pretendem usar neste projeto (TCC).
- Apresente o contexto de uso dessa aplicação. (“Usuários, tarefas, equipamentos (hardware, software e materiais) e o ambiente físico e social no qual um produto é usado.”)

-->

A criação de datasets de imagens rotuladas é uma etapa essencial em projetos de visão computacional, especialmente no contexto de reconhecimento facial e detecção de emoções. No entanto, esse processo é, em geral, demorado e trabalhoso, exigindo classificação manual de uma grande quantidade de imagens antes que seja possível iniciar o treinamento automático de modelos de aprendizado de máquina. Este projeto busca explorar alternativas que tornem esse processo mais ágil, confiável e acessível. Ao minimizar o custo produtivo da coleta e rotulagem inicial, é possível direcionar mais atenção à curadoria e à qualidade das classificações, aspecto relevante quando se trata de emoções, que são frequentemente ambíguas e subjetivas à interpretação humana.

As expressões faciais são um dos principais meios de comunicação não verbal, permitindo a manifestação e a interpretação de sentimentos mesmo na ausência da fala. Este trabalho propõe o desenvolvimento de uma ferramenta que automatize a criação de datasets de expressões faciais humanas, associadas a diferentes emoções, com foco específico em sessões reais de jogos digitais. Diferente de abordagens existentes, que dependem de jogos específicos que instruem o jogador a imitar emoções pré-definidas, a ferramenta aqui proposta visa capturar expressões espontâneas, registradas naturalmente por uma facecam enquanto o jogador interage com qualquer jogo eletrônico. Ao relacionar essas expressões ao contexto do que está sendo exibido na tela, busca-se construir conjuntos de dados mais representativos e aplicáveis a cenários reais.

- Webcam: Será utilizada uma câmera voltada para computadores, que possua resolução de no mínimo 720p, para captura das expressões faciais do usuário. A webcam foi escolhida em relação a outros tipos de câmeras pelo seu preço, pela facilidade de utilização e pela portabilidade. Levamos em conta na escolha, também, pois já possuímos esse material em nossas residências.
- Computador: Utilizaremos um computador ou notebook que possuam no mínimo as seguintes especificações: processador i5-8400 (ou equivalente/melhor) e 16 GB de memória RAM. Usaremos essas máquinas para realizar a programação, design e desenvolvimento do projeto, assim como seus testes e correções. Também o utilizaremos como um artifício para teste e prototipação em jogos, para identificar e definir as expressões faciais do usuário. Utilizaremos o computador para testes e não videogames, pois a interface da aplicação estará no próprio aparelho, facilitando a captura.
- Dataset: Datasets contendo imagens de expressões faciais serão utilizados para a realização da comparação e identificação dessas expressões. A intenção é utilizar datasets já disponíveis, para otimizar e agilizar o processo de desenvolvimento do nosso projeto. Alguns datasets recomendados incluem: Kaggle - Face Expression Recognition Dataset e DFEW (Dynamic Facial Expression in-the-Wild).
- IA: Utilizaremos uma IA que consiga ser alimentada de modo a analisar o contexto presente na tela e reconhecer corretamente a relação entre a expressão do indivíduo e o contexto que se apresenta. Algumas IAs que podem ser utilizadas são: FER - Facial Expression Recognition e MediaPipe.

## Publico Alvo

<!-- 
- Determine qual o grupo específico de pessoas ou organizações para as quais este produto ou serviço é direcionado.
- Descreva as caracteristicas demográficas, comportamentais, psicográficas ou geográficas deste público alvo que o torna mais propenso a se interessar pelo que está sendo oferecido neste projeto ou serviço.

-->

O público-alvo deste projeto são empresas de jogos digitais, tanto grandes estúdios quanto estúdios independentes (indies). Essas empresas têm como foco principal o desenvolvimento de jogos e buscam formas de aumentar o engajamento dos jogadores. Elas se beneficiam do projeto por promover uma maior aproximação entre jogo e jogador, permitindo customizações mais precisas e experiências mais envolventes. Em termos de características, esse público é composto por organizações que valorizam inovação, adaptação às tendências do mercado e feedback direto do usuário, sendo mais propensas a investir em ferramentas que aumentem a retenção e a satisfação dos jogadores.

## Análise de concorrência (A FAZER)
<!--
1. Identifique os principais concorrentes ou softwares mais utilizados pelo seu público-alvo.
2. Colete informações sobre os concorrentes selecionados.
3. Analise as características e funcionalidades dos concorrentes.
4. Avalie a experiência do usuário (UX).
5. Examine os preços e modelos de negócio.
6. Pesquisa de satisfação do cliente e opiniões.
7. Identifique padrões e tendências no mercado.
8. Elabore relatórios e sumarize os resultados.
9. Extraia pontos positivos e faça recomendações.
-->

1. Há vários sites que permitem a criação, download e upload de datasets, e dentre eles o mais conhecido é o Kaggle, que se trata de uma plataforma online onde os usuários podem fazer download e upload de datasets. Levando em consideração que nosso projeto é dividio entre aplicativo e site, o Kaggle faz mais relação com a parte do site, onde o mesmo funciona como um Hub de datasets.
2. 


### Personas (A FAZER)

- Descreva as personas que irão interagir com a aplicação ou produto. Deixe claro suas principais caracteristicas e contextos sociais, econômicos e culturais.
- Quais informações sobre o usuário o serviço ou poduto deve guardar?

  - Persona primaira ...
  - Persona secundária ...
  - Outras personas ...

### Mapa de empatia (A FAZER)

![Mapa de empatia](empatia.png)

- Determine o mapa de empatia[^1] de pelo menos uma persona primária e uma sercundária.
  - O que o usuário vê: aqui estamos falando do ambiente visual em que o usuário se encontra. Ou seja, o que ele efetivamente enxerga, as pessoas e objetos que estão ao seu redor. Isso ajuda a entender o contexto em que o usuário está inserido e as influências visuais que está recebendo.
  - O que o usuário ouve: neste quadrante, buscamos entender o que o usuário está ouvindo, os sons que o cercam e como eles influenciam suas ações.
  - O que o usuário diz e faz: aqui consideramos ações e comportamentos que o usuário apresenta durante sua interação com serviço ou poduto.
  - O que o usuário pensa e sente: neste quadrante, buscamos entender os pensamentos, sentimentos, emoções e percepções que o usuário tem em relação ao serviço ou poduto. Quais expectativas o usuário cria sobre o serviço ou poduto?
  Que tipo de serviço ou poduto mais agrada essa persona?
  - Dores: quando falamos sobre dores do usuário, estamos fazendo referência a quaisquer obstáculos, necessidades ou frustrações que o usuário possa experimentar ao tentar realizar uma tarefa ou alcançar um objetivo. Isso inclui, por exemplo, problemas de usabilidade, dificuldades de acesso ou outros desafios que podem afetar a experiência do usuário.
  - Ganhos: nesse caso estamos falando de quaisquer benefícios ou recompensas que o usuário possa experimentar ao utilizar o serviço ou poduto. Isso pode incluir economia de tempo ou facilidade de uso, por exemplo. Que desejos do usuário o serviço ou poduto satisfaz?

## Contexto de uso (A FAZER)

- Descreva o ambiente em que o serviço ou poduto deve ser utilizado.
- Qual/quais o(s) contexto(s) sociais, econômicos e culturais existentes neste ambiente?
- Quais informações sobre o ambiente, o serviço ou poduto deve guardar antes de iniciar a interação?
- O que normalmente deve estar acontecendo com o ambiente quando o usuário interagir com o serviço ou poduto?

## Jornada do usuário (A FAZER)

- Criar uma narrativa para o o seu serviço ou poduto com o usuário.
- Determine o que o usuário realiza desde a primeira até o última interação com o serviço ou poduto.
  - Descreva o que acontece ou pode acontecer passo a passo
  - Como a tarefa começa? Como a tarefa se desenvolve? Como a tarefa termina?


<!--
## Análise de concorrência

- Pesquise serviços ou podutos existentes atualmente que possam realizar o objetivo deste projeto.
- Selecione pelo menos 3 serviços ou podutos diferentes.
- Em relação aos concorrentes, respondam as seguintes perguntas?
  - Existe plataforma similar que atende o mesmo mercado e funcionalidades? Se sim: Quais os pontos positivos? Quais os pontos negativos?
  - Existe plataforma diferente quanto ao serviço, mas que atenda esse mercado? Se sim: Quais os pontos positivos? Quais os pontos negativos?
 -->
 
## Coleta de dados (A FAZER)

## Modelo de tarefas (A FAZER)

## Design (A FAZER)

- Pense nas características de Affordances do seu serviço ou poduto. 
    - Que tipo de acessibilidades devem ser consideradas dentro do seu projeto?
- Discuta o papel das expectativas do usuário no projeto deste serviço ou poduto. Qual a importância e pontos a serem considerados se você quiser vender esse serviço ou poduto?

### Prototipação em baixo nível (papel) (A FAZER)
#### Avaliação heurística

### Prtotipação em médio nível (Figma) (A FAZER)
#### Avaliação heurística

### Prtotipação em alto nível (React) (A FAZER)
#### Avaliação heurística

[^1]: Fonte: Adaptado de <https://hazeshift.com.br/mapa-de-empatia/>

<!-- TODOs:
- Add exemplos
 -->
