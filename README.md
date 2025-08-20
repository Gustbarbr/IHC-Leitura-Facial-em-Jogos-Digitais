# Projeto de Interface Humano-Computador

Projeto apresentado ao Centro Universitário [FEI](https://portal.fei.edu.br/), como parte dos requisitos necessários para aprovação na disciplina de Interface Humano-Computador (CC8122) do curso de Ciencia da Computação, orientado pelo Prof. Dr. [Fagner de Assis Moura Pimentel](https://github.com/fagnerpimentel).

Este projeto se baseia no Trabalho de Conclusão de Curso (TCC) entitulado Leitura Facial em Jogos Digitais: Ferramenta facilitadora de criação de datasets sob orientação do Professor Dr. Fagner de Assis Moura Pimentel e desenvolvido pelos seguintes alunos:

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
O público-alvo deste projeto são pessoas e empresas cujo trabalho impactam os seus clientes emocionalmente, como empresas de jogos, produtores de filmes e principalmente desenvolvedores que possuam projetos de DeepLearning que requer treinamento de emoções faciais.Tanto grandes estúdios de jogos quanto produtores de filmes como foco principal o desenvolvimento de entretenimento e buscam formas de aumentar o engajamento. Elas se beneficiam do projeto por promover uma maior aproximação entre o produto e consumidor, permitindo customizações mais precisas e experiências mais envolventes. Em termos de características, esse público é composto por organizações que valorizam inovação, adaptação às tendências do mercado e feedback direto do usuário, sendo mais propensas a investir em ferramentas que aumentem a retenção e a satisfação do seu público.
Enquanto a desenvolvedores de deeplearning, é comum uma etapa para desenvolvimento de uma base de dados própria porém essa atividade é extensa e trabalhosa. Este projeto como um objetivo secundário, facilitar o desenvolvimento de novas bases de dados visando encurtar o tempo necessário para a criação de um dataset original.

## Análise de concorrência
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

1. Há vários sites que permitem a criação, download e upload de datasets, e dentre eles os mais conhecidos são o Kaggle, Hugging Face e Nevermind, onde Kaggle e Hugging Face são plataformas online onde os usuários podem, entre outras coisas, fazer download e upload de datasets. Já Nevermind é um jogo de suspence psicológico que usa a detecção de expressões faciais como artífice que torna o jogo.
2. 
   - Kaggle: Plataforma com foco em Ciência de Dados e Machine Learning, cuja função primária são suas competições, onde times ou indivíduos podem enviar seus modelos para resolver problemas específicos e ganhar prêmios, além disso ele oferece datasets, notebooks e um fórum da comunidade. Os usuários podem fazer download ou upload de datasets e notebooks; 
   - Hugging Face: Uma empresa responsável pelo desenvolvimento de ferramentas e recursos para o desenvolvimento de plicações com Machine Learning. Sua plataforma permite que os usuários colaborem em modelos de Machine Learning e datasets; 
   - Nevermind: um jogo de suspence psicológico que adapta a dificuldade, visuais e som de acordo com o estresse detectado na expressão facial do jogador.
3.
   - Kaggle: Competição entre usuários utilizando modelos de Machine Learning; upload e download de datasets que podem ser públicos ou privados; upload e download de notebooks que permitem o compartilhamento de técnicas de criação de códigos e análise de dados e cursos de aprendizado de ciência de dados;
   - Hugging Face: Biblioteca Transformers que simplifica o uso de modelos transformer para geração de texto e tradução; upload e download de datasets, principalmente relacionados a modelos de Machine Learning e NLP; hub de modelos que funciona como repositório de modelos pré-treinados para tarefas relacionadas a NLP, visão computacional e áudio;
   - Nevermind: Uso de expressões faciais do jogador, captadas a partir da webcam, para alterar a jogabilidade do jogo, mudando a dificuldade, visuais e sons; O jogo se torna mais difícil conforme o estresse emocional do jogador aumenta, onde medo e ansiedade tem um foco maior.
4. A Kaggle possui uma interface minimalista e ao mesmo tempo cheia de informações, apesar de tanto texto a navegação é intuitiva.A Kaggle não foca apenas em datasets, é um ecossistema de cientistas que publicam seus estudos, com modelos e datasets utilizados e por consequência, acada se tornando um site comum para download de datasets, tendo, inclusive, uma aba dedicada apenas a datasets.
5. A kaggle baseia-se no plano freemium, onde todas as principais ferramentas são disponibilizadas de forma gratuita e a monetização vem de empresas que se interessam em criar suas próprias competições na plataforma, além da plataforma fazer parcerias com empresas como google cloud e receber uma porcentagem do prêmio das competições citadas anteriormente. Resumidamente, usuários individuais não precisam pagar um plano para ter acesso total às funcionalidades do site, mas empresas devem pagar pelo suporte da kaggle para hospedar competições pagas e para utilizar de alguma ferramenta da kaggle para projetos empresariais.
6. Na plataforma da Kaggle não existe explicitamente uma área de avaliação, mas a coleta é realizada de forma rápida distribuindo questionário de avaliação para a comunidade da kaggle fora da plataforma, opiniões de usuários em redes sociais. Também, após uma competição hosedada na kaggle, existe um formulário curto para receber o feedback daquela função. De forma um pouco mais discreta, existe a opção de reportar bugs ou falhas no sistema, que serve pode servir como crítica construtiva.
7. O mercado de Inteligência artificial vem crescendo rapidamente e de maneira desenfreada, juntamente com a IA, os datasets tornam-se fatores principais nesse meio. Desta maneira, a busca por treinamento, machine learning, só tende a aumentar e ganhar cada vez mais o mercado no mundo. Com isso, a procura por datasets / modelos treinados permite que áreas relacionadas consigam dominar.
8. O Kaggle possui um acervo enorme de datasets e informações, cerca de dezenas de milhares (de acordo com o site https://www.innovatiana.com/en/post/kaggle-for-datasets?utm_source=chatgpt.com), isso se dá pela grande quantidade de acessos e por ser open source. Este modelo vem crescendo constantemente no mercado, com mais e mais pessoas utilizando as máquinas para aprendizagem e inteligências artificiais. Com isso, a possibilidade de crescimento de Kaggle é muito grande, além disso, é a porta de entrada para muitos ourtos artifícios de acervos e disponibilização de datasets.
9. Pontos positivos:
<ul>
 <li>A plataforma Kaggle oferece muitos datasets de diversos tipos, de forma open-source;</li>
 <li>Tais datasets são disponibilizados com extensões fáceis de serem utilizadas, como CSV, Json;</li>
 <li>É um site ativo, com manutenção e adição de informações recentes,</li>
</ul>

### Personas (A FAZER)
<!--
- Descreva as personas que irão interagir com a aplicação ou produto. Deixe claro suas principais caracteristicas e contextos sociais, econômicos e culturais.
- Quais informações sobre o usuário o serviço ou poduto deve guardar?
-->
#### Persona primária
1. Thiago Alberto Mendes
   Thiago Alberto Mendes, de 35 anos, é formado em Design de Jogos e atualmente trabalha como Game Director em uma empresa pequena de nome Best Games Studio. Já criou títulos como ATG VI, Armored Lore, Bright Souls. Todos esses jogos possuem características únicas, mas nenhum conseguiu colocar a empresa em posição de destaque. Sua ideia para aumentar o renome da empresa é fazer um título único e inovador.
   Thiago gostaria de adicionar em seu jogo uma mecânica única, que consiga aproximar o jogo e o jogador, de uma forma natural e que adicione elementos de jogabilidade. 
2. Valter Alter
   Valter Alter, de 58 anos, tem um blog e um canal no YouTube de desenvolvimento de jogos chamado ClickGamesBR, com cerca de 1.3 milhões de inscritos. O foco de seu canal é criar, mostrar ao seu público e publicar os jogos na web. Ultimamente, seus seguidores pediram para que fizesse um jogo que interaja com o usuário a partir de suas emoções. Valter tem uma ideia de história, mas necessita que seus seguidores enviem vídeos com webcam e gameplay de diversos jogos, e dessa maneira ele poderia utilizar uma ferramenta que facilite a criação de datasets, a fim de criar o que seus seguidores desejam.
3. Gabriel Cavalcante
   Gabriel Cavalcante, de 43 anos, trabalha como analista de dados na empresa Mind Plus, onde semanalmente necessita criar datasets para outras empresas, cujo foco principal das mesmas é o desenvolvimento de jogos. Essas empresas necessitam de datasets personalizados que consigam envolver o jogo e o jogador. Gabriel precisa de uma ferramenta que facilite a captação da emoção de pessoas enquanto jogam, dessa maneira consegue saber que tipos de jogos causariam, mais conforto, raiva e medo, a fim de auxiliar na criação de uma experiência customizada.
#### Persona secundária
1. Lora Barros
   Lora Barros, de 21 anos, estudante de ciências da computação tem como principal hobby jogar videogame. Costuma jogar jogos únicos com mecânicas diferentes e impactantes. Como está de férias, busca jogar um novo jogo, algo que possa ser controlado e desenvolvido a partir de identificações de rosto, emoções. Para ela, esse seria o ápice da tecnologia nos jogos eletrônicos.

### Mapa de empatia (A FAZER)

![Mapa de empatia](empatia.png)

<!--
- Determine o mapa de empatia[^1] de pelo menos uma persona primária e uma sercundária.
  - O que o usuário vê: aqui estamos falando do ambiente visual em que o usuário se encontra. Ou seja, o que ele efetivamente enxerga, as pessoas e objetos que estão ao seu redor. Isso ajuda a entender o contexto em que o usuário está inserido e as influências visuais que está recebendo.
  - O que o usuário ouve: neste quadrante, buscamos entender o que o usuário está ouvindo, os sons que o cercam e como eles influenciam suas ações.
  - O que o usuário diz e faz: aqui consideramos ações e comportamentos que o usuário apresenta durante sua interação com serviço ou poduto.
  - O que o usuário pensa e sente: neste quadrante, buscamos entender os pensamentos, sentimentos, emoções e percepções que o usuário tem em relação ao serviço ou poduto. Quais expectativas o usuário cria sobre o serviço ou poduto?
  Que tipo de serviço ou poduto mais agrada essa persona?
  - Dores: quando falamos sobre dores do usuário, estamos fazendo referência a quaisquer obstáculos, necessidades ou frustrações que o usuário possa experimentar ao tentar realizar uma tarefa ou alcançar um objetivo. Isso inclui, por exemplo, problemas de usabilidade, dificuldades de acesso ou outros desafios que podem afetar a experiência do usuário.
  - Ganhos: nesse caso estamos falando de quaisquer benefícios ou recompensas que o usuário possa experimentar ao utilizar o serviço ou poduto. Isso pode incluir economia de tempo ou facilidade de uso, por exemplo. Que desejos do usuário o serviço ou poduto satisfaz?
-->

#### Persona primária: Gabriel Calvacante, 43 anos
- O que o usuário vê: Família bem estruturada; Amigos de classe média-alta, Chefe que demanda desempenho por parte dos funcionários.
- O que o usuário ouve: Precisa passar mais tempo com a família e menos no trabalho; Assiste a canais do YouTube sobre a área de dados.
- O que o usuário diz e faz: Gosta de ler livros que abordam psicologia, desde suspense até estudos científicos; Frquenta lugares de luxo moderado, de forma que a família esteja confortável sem precisar gastar mais do que deve.
- O que o usuário pensa e sente: Preciso estudar para crescer na minha área; Acredito que jogos customizados podem vender mais do que jogos comuns; Compreendo que quanto mais dados a empresa tiver, mais fácil será o trabalho dos funcionários.
- Dores: Sente que passa menos tempo com a família por conta do tempo gasto dentro de seu trabalho; Sente que não atende as demandas de seu chefe, e se conseguisse um facilitador poderia alavancar seus resultados.
- Ganhos: Redução de tempo de trabalho, tanto por parte da pesquisa de um dataset coerente, quanto por parte da criação de um novo; Facilidade ao encontrar novos dados.

#### Persona secundária: Lora Barros, 21 anos
- O que o usuário vê: 
- O que o usuário ouve:
- O que o usuário diz e faz:
- O que o usuário pensa e sente:
- Dores:
- Ganhos:
  
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
