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
   - Kaggle: Plataforma com foco em Ciência de Dados e Machine Learning, cuja função primária são suas competições, onde times ou indivíduos podem enviar seus modelos para resolver problemas específicos e ganhar prêmios, além disso ele oferece datasets, notebooks e um fórum da comunidade. Os usuários podem fazer download ou upload de datasets e notebooks;<br>
     <img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/184c7fcb-7920-4c62-a615-d0173ccb2087" />
     
   - Hugging Face: Uma empresa responsável pelo desenvolvimento de ferramentas e recursos para o desenvolvimento de plicações com Machine Learning. Sua plataforma permite que os usuários colaborem em modelos de Machine Learning e datasets;<br>
     <img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/305a3b5f-e3a4-4e9f-b333-70fefbb3405f" />
   
   - Nevermind: um jogo de suspence psicológico que adapta a dificuldade, visuais e som de acordo com o estresse detectado na expressão facial do jogador.<br>
     <img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/2ef14b47-399c-45e6-89f7-1723d66e86a5" />

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

### Personas
<!--
- Descreva as personas que irão interagir com a aplicação ou produto. Deixe claro suas principais caracteristicas e contextos sociais, econômicos e culturais.
- Quais informações sobre o usuário o serviço ou poduto deve guardar?
-->
#### Persona primária
1. Thiago Alberto Mendes, de 35 anos, é formado em Design de Jogos e atualmente trabalha como Game Director em uma empresa pequena de nome Best Games Studio. Já criou títulos como ATG VI, Armored Lore, Bright Souls. Todos esses jogos possuem características únicas, mas nenhum conseguiu colocar a empresa em posição de destaque. Sua ideia para aumentar o renome da empresa é fazer um título único e inovador.
   Thiago gostaria de adicionar em seu jogo uma mecânica única, que consiga aproximar o jogo e o jogador, de uma forma natural e que adicione elementos de jogabilidade.<br>
   <img width="256" height="256" alt="image" src="https://github.com/user-attachments/assets/840e1f88-3f76-439c-9127-e4c811bcb35c" />

2. Valter Alter, de 58 anos, tem um blog e um canal no YouTube de desenvolvimento de jogos chamado ClickGamesBR, com cerca de 1.3 milhões de inscritos. O foco de seu canal é criar, mostrar ao seu público e publicar os jogos na web. Ultimamente, seus seguidores pediram para que fizesse um jogo que interaja com o usuário a partir de suas emoções. Valter tem uma ideia de história, mas necessita que seus seguidores enviem vídeos com webcam e gameplay de diversos jogos, e dessa maneira ele poderia utilizar uma ferramenta que facilite a criação de datasets, a fim de criar o que seus seguidores desejam.<br>
    <img width="256" height="256" alt="image" src="https://github.com/user-attachments/assets/51503288-f126-448a-8377-81d675db1de1" />


<!--
   <img width="256" height="256" alt="image" src="https://github.com/user-attachments/assets/8004ef7f-e31e-4866-a6d5-e321e374af5e" />
-->
#### Persona secundária
1. Lora Barros, de 21 anos, estudante de ciências da computação tem como principal hobby jogar videogame. Costuma jogar jogos únicos com mecânicas diferentes e impactantes. Como está de férias, busca jogar um novo jogo, algo que possa ser controlado e desenvolvido a partir de identificações de rosto, emoções. Para ela, esse seria o ápice da tecnologia nos jogos eletrônicos.
2. Alberto Bezerra, de 24 anos, estudante de ciências da computação está participando de uma iniciação científica que envolve o desenvolvimento de aplicações com Deep Learning, mas o projeto acabou se estagnando pois o dataset que ele utiliza está desbalanceado. Como está no terceiro semestre da faculdade, ele não compreende completamente o conceito de data augmentation, então ele busca por métodos de criação de datasets usando o próprio rosto para suprir os dados que estão em falta no dataset original.

3. Gabriel Cavalcante, de 43 anos, trabalha como analista de dados na empresa Mind Plus, onde semanalmente necessita criar datasets para outras empresas, cujo foco principal das mesmas é o desenvolvimento de jogos. Essas empresas necessitam de datasets personalizados que consigam envolver o jogo e o jogador. Gabriel precisa de uma ferramenta que facilite a captação da emoção de pessoas enquanto jogam, dessa maneira consegue saber que tipos de jogos causariam, mais conforto, raiva e medo, a fim de auxiliar na criação de uma experiência customizada.<br>
### Mapa de empatia

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

#### Persona primária: Valter Alter, 58 anos
- O que o usuário vê: Seus seguidores do Youtube apoiando suas ideias, família bem unida, cenário de game development mais desenvolvido.
- O que o usuário ouve: As ferramentas para realizar seu trabalho estão avançando rapidamente, família apoia muito seu trabalho.
- O que o usuário diz e faz: Gosta de jogar com seus filhos, gosta de produzir jogos e distribuir a seus seguidores. Diz que ama o que faz.
- O que o usuário pensa e sente: Sente que precisa inovar em seu conteúdo e que precisa de ferramentas novas para isso.
- Dores: Sente que ainda não fez um jogo de sucesso e que gostasse. Gostaria de atrair mais pessoas para seu nicho de games.
- Ganhos: Redução do tempo de trabalho e uma produção mais rápida de conteúdo.

#### Persona primária: Thiago Alberto Mendes, 35 anos
- O que o usuário vê: Sua contribuição em desenvolvimento de jogos interessantes, 
- O que o usuário ouve: Que fez bons jogos, que precisa renovar o estado dos games.
- O que o usuário diz e faz: Diz que quer fazer um jogo que seja inovador e muito grande, que precisa criar uma família.
- O que o usuário pensa e sente: Se sente sozinho e estagnado profissionalmente.
- Dores: Não ter feito um jogo muito conhecido, não ter uma família.
- Ganhos: Muita experiência no desenvolvimento de jogos e manejamento de equipes.

#### Persona secundária: Lora Barros, 21 anos
- O que o usuário vê: Amigos bem fiéis, família que apoia suas decisões. Bem disciplinada e sempre tira boas notas.
- O que o usuário ouve: Ouve que deve arrumar logo um emprego, sobre anúncio de novos jogos e sobre evoluções tecnológicas.
- O que o usuário diz e faz: Gosta de jogar videogame e estuda bastante, principalmente programação e tecnologias. Não gosta muito de sair, prefere passar o tempo em casa, seja nos estudos ou nos jogos. Gosta de ler livros técnicos.
- O que o usuário pensa e sente: Queria um jogo revolucionário, com que possa jogar e se divertir com os amigos. Sente que precisa logo arranjar um estágio, pois todos os seus amigos estão começando em um.
- Dores: Precisa logo de um emprego e quer começar a estudar o desenvolvimento de jogos e datasets.
- Ganhos: Ser bem sucedida, ter um foco profissional na área de games e ter vários amigos.
  
## Contexto de uso

### Descreva o ambiente em que o serviço ou produto deve ser utilizado:
* Gabriel Cavalcante:
Como Gabriel precisa capturar expressões faciais com precisão para gerar datasets confiáveis, o ambiente ideal de uso do produto deve ser controlado. Ele normalmente utiliza salas bem iluminadas e silenciosas em sua empresa, com webcams de pelo menos 720p e fundos neutros, garantindo que os dados não sejam comprometidos por interferências visuais. Como profissional da área, Gabriel também se certifica de que os participantes não utilizem acessórios que obstruam o rosto, como bonés, máscaras ou óculos escuros, para manter a qalidade do reconhecimento facial.
### Qual/quais o(s) contexto(s) sociais, econômicos e culturais existentes neste ambiente?
* Gabriel Cavalcante:
Gabriel atua em um contexto profissional, dentro de uma empresa de tecnologia com foco em dados e jogos digitais. Ele tem acesso a recursos computacionais avançados e trabalha com colaboradores familiarizados com tecnologia. Culturalmente, ele está inserido em um ambiente onde inovação, usabilidade e personalização são valorizados, pois os datasets gerados serão usados para melhorar a experiência de jogadores de diferentes perfis. Economicamente, sua empresa investe em ferramentas que otimizem o tempo e aumentem a qualidade dos dados, o que torna fundamental que o produto seja eficiente e compatível com sistemas mais robustos.
### Quais informações sobre o ambiente, o serviço ou poduto deve guardar antes de iniciar a interação?
* Gabriel Cavalcante:
Antes de iniciar a coleta de dados, Gabriel precisa configurar o ambiente e o sistema de forma adequada. Isso inclui garantir que os participantes estejam posicionados corretamente, com boa iluminação e sem obstruções no rosto. O sistema deve registrar informações básicas sobre o cenário de uso (como iluminação, tipo de câmera, resolução e características do ambiente), bem como armazenar fotos iniciais dos usuários para o treinamento do modelo de reconhecimento facial. Esses dados são fundamentais para que o processo ocorra sem erros e para garantir consistência nos datasets gerados.
### O que normalmente deve estar acontecendo com o ambiente quando o usuário interagir com o serviço ou poduto?
* Gabriel Cavalcante:
Durante a coleta das emoções, Gabriel garante que o ambiente permaneça estável: a iluminação constante, pouco ruído e o mínimo de movimento externo. Isso evita interferências no reconhecimento facial e garante que as emoções captadas estejam realmente relacionadas às interações do jogador com o jogo. O foco é criar uma experiência imersiva para o participante, enquanto Gabriel observa, coleta e analisa os dados gerados em tempo real ou após a sessão.

## Jornada do usuário
<!--
- Criar uma narrativa para o o seu serviço ou poduto com o usuário.
- Determine o que o usuário realiza desde a primeira até o última interação com o serviço ou poduto.
  - Descreva o que acontece ou pode acontecer passo a passo
  - Como a tarefa começa? Como a tarefa se desenvolve? Como a tarefa termina?
-->

Jorge Mateus trabalha na área de dados de uma empresa de desenvolvimento de jogos e decidiu utilizar seu próprio rosto para criar um dataset que será usado em seu trabalho.
Ele acessa o site do produto, realiza o cadastro, e em seguida cria um nome e uma descrição para o seu dataset. Depois, liga a webcam e define a quantidade de frames que deseja capturar. Durante esse processo, os frames da webcam são salvos automaticamente em uma pasta separada.
Assim que a quantidade de frames definida é atingida, Jorge inicia o treinamento do dataset clicando em um botão. Em seguida, ele aciona outro botão para começar a captura de emoções e, ao mesmo tempo, inicia sua jogatina. Durante esse período, as imagens capturadas para análise emocional são armazenadas diretamente no dataset criado.
<!--
## Análise de concorrência

- Pesquise serviços ou podutos existentes atualmente que possam realizar o objetivo deste projeto.
- Selecione pelo menos 3 serviços ou podutos diferentes.
- Em relação aos concorrentes, respondam as seguintes perguntas?
  - Existe plataforma similar que atende o mesmo mercado e funcionalidades? Se sim: Quais os pontos positivos? Quais os pontos negativos?
  - Existe plataforma diferente quanto ao serviço, mas que atenda esse mercado? Se sim: Quais os pontos positivos? Quais os pontos negativos?
 -->

## Qualidade de Uso em IHC
* A usabilidade é um dos pilares fundamentais do projeto e deve ser muito bem projetada, uma vez que qualquer um que possuir a licença poderá utilizar a plataforma.
Desta maneira, ela será intuitiva, com ícones, imagens e explicações das funcionalidades, deve ser, também, fácil de ser utilizada e deve ter um grau de aprendizagem rápido e permanente no usuário, para que não precise se utilizar de tutoriais a cada uso.
Juntamente a isso, será feito um fluxo lógico de navegação, direcionando o usuário para a próxima etapa do processo de forma fluida e focada.
Por ser um aplicativo local, a segurança será o menor dos problemas, uma vez que as imagens tiradas e os dados gerados estarão presentes no computador do usuário. <br>
* A experiência do usuário será baseada em suas emoções e expressões faciais, desta maneira, para atribuir sensações de prazer, diversão e profissionalismo, o aplicativo deverá possuir animações fluidas. interfaces modernas, feedback ao usuário e design inteligente.
Tais fatores contribuirão para a satisfação e credibilidade do usuário com o projeto. <br>
* Para acessibilidade, teremos menus simples e explicações compreensíveis para o entendimento de todo público alvo, algo a ser implementado seria uma resposta auditiva ao clicar botões, para uma maior abrangência de público.
O design inteligente e o fluxo lógico para o desenvolvimento da atividade torna o aplicativo fácil de ser utilizado e intuitivo na hora do uso. <br>
* O sistema terá boa comunicabilidade, uma vez que cada passo apresentará explicações de como usar e o que está sendo feito, com as imagens, com o usuário, com o sistgema. Serão utilizados icones, imagens, para facilitar a comunicação e interação com o usuário, a partir da aplicação.

## Ambiente e contexto

### Thiago Alberto Mendes:
#### Perguntas:

### Valter Alter  
#### Perguntas de refinamento: <br>
1 - Quem pode/deve cadastrar os dados de gameplay e expressões faciais no sistema? <br>
2 - Quando são cadastradas as sessões de jogo para geração de datasets? <br>
3 - Quem fornece os dados de gameplay e das expressões? <br>
4 - Quais dados de gameplay e faciais devem ser cadastrados? <br>
5 - Quantas sessões de captura são realizadas em cada período? <br>
6 - Quem pode contribuir com gravações de gameplay e expressões? <br>
7 - Que dados são necessários para cadastrar um seguidor como participante externo? <br>
8 - Como são obtidos os vídeos enviados por seguidores? <br>
9 - De quem depende a conclusão do cadastro de um dataset? <br>
10 - De que informações Valter e seus seguidores precisam para confirmar que o dataset foi gerado corretamente? <br>
11 - Como um participante confirma que seu material foi aceito? <br>
12 - Em que pontos a interação de Valter com a aplicação pode ser mais eficiente? <br>
13 - Como Valter entra em contato com seus seguidores para organizar o envio dos dados? <br>
14 - Quem precisa ser notificado quando um dataset é concluído? <br>

#### Atores:
Valter Alter, 58 anos, criador de conteúdo para jogos digitais no canal ClickGamesBR (1,3 milhão de inscritos no YouTube). Seus seguidores frequentemente pedem novidades, incluindo jogos que respondam às emoções dos jogadores.

#### Narrativa:
Valter Alter, 58 anos, é criador do canal **ClickGamesBR**. Ele utiliza seu **PC gamer e webcam HD em seu estúdio** [Q1]. **Os atores principais são Valter e seus seguidores**, que podem enviar gravações de gameplay [Q2]. **Seu objetivo é gerar datasets de emoções para criar jogos interativos** e, como meta secundária, inovar no canal [Q3].

Primeiro, **testa a ferramenta em suas próprias lives** e depois planeja campanhas para receber vídeos dos seguidores [Q4]. Durante o uso, conecta a webcam e deixa a aplicação registrar automaticamente suas expressões [Q5]. A iluminação e qualidade da câmera podem interferir nos resultados [Q6]. Valter avalia os datasets verificando se as expressões correspondem às situações de jogo [Q7].

Ele escolhe a ferramenta por economizar tempo em relação à rotulagem manual [Q8]. Já tem experiência com gravações, mas não com análise automática de emoções [Q9]. **Pretende usar a aplicação regularmente em transmissões e gravações** [Q10]. Entre as barreiras estão iluminação inadequada e custos de equipamento [Q11]. Ele conta com softwares de edição e plataformas de streaming como apoio [Q12]. O retorno é a criação rápida de datasets rotulados [Q13]. A longo prazo, espera consolidar sua imagem como criador inovador [Q14].

### Gabriel Cavalcante:
#### Perguntas de refinamento:
1. Quem pode/deve cadastrar os dados de sessões de jogo e emoções no sistema?<br>
2. Quando são cadastradas as sessões de teste para geração dos datasets?<br>
3. Quem fornece os dados necessários (jogadores, equipe de coleta, clientes)?<br>
4. Quais informações de gameplay e expressões devem ser cadastradas?<br>
5. Quantas sessões de coleta geralmente são realizadas por projeto?<br>
6. Quem pode participar como jogador/usuário nas sessões de captura?<br>
7. Que dados são necessários para cadastrar um jogador externo no sistema?<br>
8. Como são obtidos os dados dos jogadores (capturas automáticas, formulários, vídeos)?<br>
9. De quem depende a conclusão da criação de um dataset (Gabriel, equipe, ferramenta)?<br>
10. De que informações Gabriel e a equipe precisam para validar os datasets criados?<br>
11. Como um cliente confirma que o dataset atende suas necessidades?<br>
12. Em que pontos a interação de Gabriel com a ferramenta pode ser mais eficiente?<br>
13. Como Gabriel entra em contato com jogadores ou clientes envolvidos no processo?<br>
14. Quem precisa ser notificado quando um dataset é concluído (Gabriel, equipe, empresa cliente)?<br>

#### Atores:
Gabriel Cavalcante, 43 anos, trabalha na empresa MindPlus. Semanalmente precisa criar datasets para outras empresas, cujo foco é o desenvolvimento de jogos.

### Narrativa:
Gabriel Cavalcante, 43 anos, **trabalha na MindPlus**, em um **escritório com computadores potentes e webcams** [Q1]. **O ator principal é Gabriel**; **secundários são jogadores** que participam dos testes e os clientes que recebem os datasets [Q2]. **Seu objetivo é produzir datasets personalizados de emoções**, reduzindo tempo de coleta manual [Q3].

Ele organiza sessões, ajusta ambiente e executa a ferramenta para capturar expressões durante o gameplay [Q4–Q5]. Fatores como ruído ou iluminação podem interferir [Q6]. Gabriel avalia os resultados comparando emoções detectadas com eventos do jogo [Q7].

O que o leva a usar a aplicação é a **necessidade de gerar datasets sob demanda de forma mais rápida** [Q8]. Ele tem experiência com dados, mas o reconhecimento facial automatizado é novidade [Q9]. O uso é frequente, semanal ou diário [Q10]. As barreiras envolvem limitações técnicas e prazos apertados [Q11]. Como apoio, usa bibliotecas de IA e softwares estatísticos [Q12]. O retorno é a entrega de datasets prontos e consistentes [Q13]. A longo prazo, espera fortalecer sua carreira e consolidar a MindPlus no mercado [Q14].
<br>

## Análise de tarefas

### Criar Dataset:
* HTA:
<img width="1051" height="411" alt="meuHTADownload drawio" src="https://github.com/user-attachments/assets/76536a56-a1b3-4a0e-8793-358c1da3ea3e" />

<table>
 <tr>
  <th>Objetivos / Operações</th>
  <th>Problemas e recomendações</th>
 </tr>
 <tr>
  <td>0. Criar Dataset</td>
  <td>Input: Nome a ser utilizado no dataset e quantidade de capturas de rosto. <br>
  Feedback: As imagens coletadas são salvas em uma pasta com o nome adicionado. <br>
  Plano: Informar o nome do usuário e criar um dataset com uma grande quantidade de imagens, para ter um melhor resultado. <br>
  Recomendação: Utilizar uma boa webcam e estar em um ambiente com boa iluminação, pouco movimento. Assim como um  hardware mediano e uma quantidade grande de imagens.
  </td>
 </tr>
 <tr>
  <td>1. Escolha do hardware</td>
  <td>Recomendação: É necessário a utilização de uma webcam de qualidade igual ou maior que 720p, assim como ter um hardware de média potência, para uma maior fluidez e rapidez na execução do programa.</td>
 </tr>
  <tr>
  <td>2. Planejamento de cenário</td>
   <td>Recomendação: É necessário manter o ambiente em que o teste é executado limpo e sem ruídos, com boa iluminação e sem muitos movimentos atrás do usuário.</td>
 </tr>
  <tr>
  <td>2. Adicionar nome do dataset</td>
   <td>Input: Recebe de entrada uma string. <br>
   Feedback: após a execução final da tarefa, é possível visualizar nos arquivos do computador uma pasta com o nome inserido. <br>
    Plano: Informar o nome a ser utilizado no dataset para a criação e organização de pastas.
   </td>
 </tr>
   <tr>
  <td>3. Capturar imagens do rosto</td>
    <td>Input: Inteiro com a quantidade de capturas a serem realizadas e o intervalo de cada captura.
    Feedback: Ao clicar no botão de capturar rosto, uma janela aparecerá para adicionar a quantidade de capturas e outra janela para a adição de intervalo de capturas. <br>
    Recomendação: É recomendado utilizar um grande número de capturas, para obter um resultado melhor. <br>
     Plano: Informar o número de capturas que serão tiradas e seus intervalos para o treinamento do sistema.
    </td>
    
 </tr>
 
</table>

* GOMS:
  * Goal 0: Criar Dataset (Salvar imagens do rosto do usuário)
    * Goal 1: Escolha do hardware
      * Method 1: Selecionar equipamentos adequados
      * (SEL.RULE: O hardware deve possuir webcam melhor ou igual a 720p e processamento de média potência para garantir fluidez e repidez);
        * OP. 1.1: Utilizar webcam com resolução mínima de 720p;
        * OP. 1.2: Utilizar hardware de potência média ou superior.
    * Goal 2: Planejamento de cenário
      * Method 1: Preparar ambiente antes da captura
      * (SEL.RULE: O ambiente deve estar com boa iluminação e sem muitos movimentos no fundo);
        * OP. 2.1: Garantir boa iluminação;
        * OP. 2.2: Evitar ruídos no ambiente;
        * OP. 2.3: Minimizar movimentos atrás do usuário.
    * Goal 3: Adicionar nome do dataset
      * Method 1: Inserir nome do usuário
      * (SEL.RULE: O nome inserido deve ser uma string);
        * OP. 3.1.1: Digitar string com o nome do dataset;
        * OP. 3.1.2: Confirmar criação da pasta.
      * Method 2: Inserir nome do usuário por meio de voz
      * (SEL.RULE: O nome inserido deverá ser comunicado por voz);
        * OP. 3.2.1: Falar o nome do dataset para o programa;
        * OP. 3.2.2: Confirmar criação da pasta.
    * Goal 4: Capturar imagens do rosto
      * Method 1: Configurar capturas por meio de botão
      * (SEL.RULE: O usuário deve clicar no botão para definir a quantidade de capturas);
        * OP. 4.1.1: Clicar no botão “Criar Dataset”;
        * OP. 4.1.2: Inserir número de capturas (inteiro) e seu intervalo;
        * OP. 4.1.3: Esperar conclusão das capturas.
      * Method2: Configurar capturas por meio do teclado
      * (SEL.RULE: O usuário deve clicar no botão enter do teclado para definir a quantidade de capturas);
        * OP. 4.2.1: Clicar no botão “Criar Dataset”;
        * OP. 4.2.2: Inserir número de capturas (inteiro) e seu intervalo;
        * OP. 4.2.3: Pressionar o botao Enter do teclado;
        * OP. 4.2.4: Esperar conclusão das capturas.
    * Goal 5: Salvar dataset criado
      * Method 1: Finalizar processo e validar resultados
      * (SEL.RULE: As imagens devem estar salvas na pasta criada com o nome fornecido);
        * OP. 5.1: Verificar quantidade de imagens salvas;
        * OP. 5.2: Confirmar encerramento da aba de captura.
* CTT
<img width="905" height="536" alt="meuCTTDownload drawio" src="https://github.com/user-attachments/assets/1bf6a5be-d7ea-4469-b39e-a92e60854185" />

### Iniciar reconhecimento
* HTA:
<img width="1200" height="1200" alt="image" src="https://github.com/user-attachments/assets/def560a6-560d-4b9f-9ef8-ce322bf5e87f" />

<table>
 <tr>
  <th>Objetivos / Operações</th>
  <th>Problemas e recomendações</th>
 </tr>
 <tr>
  <td>0. Iniciar Reconhecimento</td>
  <td>Input: Face do usuário no enquadro da webcam.<br>
  Feedback: Frame do rosto do usuário é salvo em uma pasta com o nome da expressão demonstrada.<br>
  Plano: Informar nome do usuário e criar o dataset com o maior número de frames possível.<br>
  Recomendação: Criar um dataset por pessoa, estando em um ambiente isolado preferencialmente.</td>
 </tr>
 <tr>
  <td>1. Configurações Dataset</td>
  <td>Input: Frames dos rostos do usuário e aplicativo apto a compreender as expressões do usuário.<br>
  Plano: Utilizar as imagens capturadas para alimentar a ferramenta.</td>
 </tr>
 <tr>
  <td>1.1. Criar dataset</td>
  <td>Plano: Informar nome do usuário e quantia de frames desejada.<br>
   Feedback: Fonte de alimento para a ferramenta.</td>
 </tr>
  <tr>
  <td>1.1.1. Informar nome</td>
  <td>Feedback: Uma pasta será criada após a execução, onde ela possuirá esse mesmo nome.</td>
 </tr>
 <tr>
  <td>1.1.2. Inserir a quantia de capturas desejadas</td>
  <td>Problema: Valores muito altos na quantidade de captura podem gerar travamentos, a depender do hardware.<br>
  Feedback: As imagens serão utilizadas na criação do dataset e posteriormente em seu treinamento.</td>
 </tr>
 <tr>
  <td>1.2. Treinar dataset</td>
  <td>Feedback: Aplicativo adaptado a compreender as expressões do usuário.</td>
 </tr>
 <tr>
  <td>2.1. Cenário isolado</td>
  <td>Problema: Se houverem várias pessoas no alcance da webcam, a ferramenta poderá ter problemas para reconhecer o usuário principal.<br>
  Recomendação: Sempre que possível, utilizar a ferramenta onde o alcance da webcam atinja apenas uma pessoa.</td>
 </tr>
 <tr>
  <td>2.2. Webcam de boa resolução</td>
  <td>Problema: Webcams de baixa resolução, trincadas ou sujas podem não reconhecer corretamente o rosto do usuário.<br>
  Recomendação: É recomendado o uso de uma webcam de no mínimo 720p, de preferência limpa e sem rachaduras.</td>
 </tr>
 
</table>

* GOMS:
  *	Goal 0: Salvar a expressão facial de uma pessoa (realizar reconhecimento facial)
    *	Goal 1: Capturar a expressão facial
        *	Method 1.A: Clicar em “Criar dataset” utilizando um mouse;
        *	(SEL.RULE: O usuário não possui tela touchscreen);
            *	OP. 1.A.1: Direcionar o ponteiro até o botão;
       * Method 1.B: Utilizar a função touchscreen para clicar em "Criar Dataset";
       *	(SEL.RULE: O usuário possui um mouse com defeito);
            *	OP. 1.B.1: Utilizar a função "touchscreen" do monitor para poder clicar no botão; 
    *	Goal 2: Salvar a expressão facial
        *	Method 1: Clicar no botão “Treinar dataset” e em seguida clicar no botão “Iniciar Reconhecimento”;
        *	(SEL.RULE: A pessoa que aparece na webcam após clicar em “Iniciar Reconhecimento” deve ser a mesma que apareceu durante o “Criar Dataset”);
             *	OP. 1.1: Utilizar de preferência em ambientes isolados.
    * Goal 3: Configuração da webcam
      *	Method 1: Ajustar webcam:
      * (SEL. RULE: O usuário deve aparecer na webcam);
           * OP. 1.1: Mover a webcam para reconhecer todo o rosto;
           * OP. 1.2: Ajustar o enquadramento da webcam;
           * OP. 1.3: Utilizar uma webcam de maior resolução.

* CTT:
<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/b6690f0e-d429-460a-8072-03a8171345ed" />


<!--
## Coleta de dados (A FAZER)

## Modelo de tarefas (A FAZER)

## Design (A FAZER)

- Pense nas características de Affordances do seu serviço ou poduto. 
    - Que tipo de acessibilidades devem ser consideradas dentro do seu projeto?
- Discuta o papel das expectativas do usuário no projeto deste serviço ou poduto. Qual a importância e pontos a serem considerados se você quiser vender esse serviço ou poduto?
-->
## Prototipação em baixo nível (papel) (A FAZER)
### Tela de inicialização / menu:
![tela1](https://github.com/user-attachments/assets/ca96c1cd-db81-49fd-a01e-4570721f6f2b)
### Tela de selecionar quantidade e tela de realizar capturas:
![tela2_3](https://github.com/user-attachments/assets/3ad26864-f4c8-448f-aff3-89bc2e1154f3)
### Tela de treinar dataset e iniciar reconhecimento
![17c83d43-633f-40df-9390-9d6dde1a4ed8](https://github.com/user-attachments/assets/45fea3ae-069a-480a-aaaf-86488c702d92)
### Tela de informações
![d95a0803-a446-43bb-ae41-057f29e881f2](https://github.com/user-attachments/assets/4cd7e9cf-9698-416b-ac9b-92922b5bdc87)

## Ciclo da Engenharia de Usabilidade
### Características de plataforma:
* Descrição de software e hardware:

| Item | Descrição | 
| -------- | ------- |
| Hardware  | PC1 - Processador: Ryzen 7 5700x (Cores: 8 / Threads: 16 / Clock base: 3.4 GHz), RAM: 32gb, Placa gráfica: RTX 4060 (VRAM: 8Gb) <br>PC2 - Processador: Ryzen 9 5900xt (Cores: 16 / Threads: 32 / Clock base: 3.3 GHz), RAM: 32gb, Placa gráfica: RTX 9070xt (VRAM: 12Gb) <br>PC3 -   |
| Software | UI: customTkinter <br> Código fonte: Python <br> Principais bibliotecas utilizadas: TensorFlow, openCv, deepFace, customTkinter, yolo, ultralytics <br> Versões: Python (3.10), TensorFlow (2.19.0) |

* Capacidades da plataforma:

| Capacidade | Justificativa | 
| -------- | ------- |
| Suporte a dispositivos de vídeo  | É necessária para a realização das atividades. |
| Placa de vídeo dedicada | É necessária para rodar jogos mais atuais. |

* Restrições da plataforma:

| Restrição | Justificativa | 
| -------- | ------- |
| Dispositivos de vídeo de resolução mínima 720p  | Apesar do data augmentation, é necessária uma resolução maior para uma maior clareza nas atividades. |
| Necessidade de um hardware mediano | A grande quantidade de processamento de informações requer um hardware de computador além do básico, para ter uma experiência mais rápida e fluida. |

### Princípios gerais de projeto:
#### Descreva o ambiente em que o serviço ou produto deve ser utilizado:
* Gabriel Cavalcante:
Como Gabriel precisa capturar expressões faciais com precisão para gerar datasets confiáveis, o ambiente ideal de uso do produto deve ser controlado. Ele normalmente utiliza salas bem iluminadas e silenciosas em sua empresa, com webcams de pelo menos 720p e fundos neutros, garantindo que os dados não sejam comprometidos por interferências visuais. Como profissional da área, Gabriel também se certifica de que os participantes não utilizem acessórios que obstruam o rosto, como bonés, máscaras ou óculos escuros, para manter a qalidade do reconhecimento facial.
#### Qual/quais o(s) contexto(s) sociais, econômicos e culturais existentes neste ambiente?
* Gabriel Cavalcante:
Gabriel atua em um contexto profissional, dentro de uma empresa de tecnologia com foco em dados e jogos digitais. Ele tem acesso a recursos computacionais avançados e trabalha com colaboradores familiarizados com tecnologia. Culturalmente, ele está inserido em um ambiente onde inovação, usabilidade e personalização são valorizados, pois os datasets gerados serão usados para melhorar a experiência de jogadores de diferentes perfis. Economicamente, sua empresa investe em ferramentas que otimizem o tempo e aumentem a qualidade dos dados, o que torna fundamental que o produto seja eficiente e compatível com sistemas mais robustos.
#### Quais informações sobre o ambiente, o serviço ou poduto deve guardar antes de iniciar a interação?
* Gabriel Cavalcante:
Antes de iniciar a coleta de dados, Gabriel precisa configurar o ambiente e o sistema de forma adequada. Isso inclui garantir que os participantes estejam posicionados corretamente, com boa iluminação e sem obstruções no rosto. O sistema deve registrar informações básicas sobre o cenário de uso (como iluminação, tipo de câmera, resolução e características do ambiente), bem como armazenar fotos iniciais dos usuários para o treinamento do modelo de reconhecimento facial. Esses dados são fundamentais para que o processo ocorra sem erros e para garantir consistência nos datasets gerados.
#### O que normalmente deve estar acontecendo com o ambiente quando o usuário interagir com o serviço ou poduto?
* Gabriel Cavalcante:
Durante a coleta das emoções, Gabriel garante que o ambiente permaneça estável: a iluminação constante, pouco ruído e o mínimo de movimento externo. Isso evita interferências no reconhecimento facial e garante que as emoções captadas estejam realmente relacionadas às interações do jogador com o jogo. O foco é criar uma experiência imersiva para o participante, enquanto Gabriel observa, coleta e analisa os dados gerados em tempo real ou após a sessão.

### Referências:

| Nome | Descrição | Importância para o projeto | Link |
| -------- | ------- | ------- | ------- |
| FER – Facial Expression Recognition  | Biblioteca open source para reconhecimento de expressões faciais.  | Base inicial para testes de detecção de emoções via IA. | https://imotions.com/blog/learning/research-fundamentals/facial-expression-recognition-fer/ |
| Kaggle – Face Expression Recognition Dataset | Dataset com milhares de imagens de expressões faciais rotuladas. | Fonte principal de dados para treinar e validar o modelo de reconhecimento. | https://www.kaggle.com/datasets/jonathanoheix/face-expression-recognition-dataset |
| Mediapipe – Google AI | Framework do Google para visão computacional e reconhecimento facial em tempo real. | Usado para rastreamento facial eficiente e suporte à detecção em vídeo. | https://developers.google.com/mediapipe |
| Nevermind (Flying Mollusk, 2015) | Jogo que utiliza leitura biométrica (batimento cardíaco) para alterar a experiência do jogador. | Referência prática de como emoções podem ser integradas na jogabilidade. | https://store.steampowered.com/app/342260/Nevermind/ |
| DFEW: Dynamic Facial Expression in the Wild | Base de dados de expressões faciais em vídeos reais. | Complemento para aumentar a robustez do modelo de reconhecimento. | https://arxiv.org/abs/2008.05924 |
| HuggingFace – Transformers | Biblioteca para processamento de linguagem natural e modelos de deep learning. | Possível apoio em técnicas de transferência de aprendizado e uso de arquiteturas modernas. | https://huggingface.co/transformers/ |

# Coleta de dados:
## Quais dados coletar:
### Dado demográfico:
* Idade.
### Educação:
* Grau de escolaridade.
### Experiências:
* Quais suas experiências nos jogos eletrônicos;
* Quais suas experiências em criação/desenvolvimento de datasets.
### Hardware pessoal:
* Quanta memória RAM possui;
* Qual a placa de vídeo possui;
* Qual processador possui;
* Quanto de armazenamento bruto possui.
### Objetivos:
* Qual é o objetivo final para usar o projeto;
* Já existe um meio para atingir tal objetivo?
### Ocupação:
* Que cargo ocupa atualmente;
* Qual a relação do cargo com seus objetivos.
### Treinamento:
* Como prefere a apresentação do produto;
* Preferência em vídeos ou tutorial em texto.
### De quem coletar os dados:
* Pessoas que jogam videogame;
* Empresas de desenvolvimento de games;
* Influenciadores de desenvolvimento de games.
## Aspectos éticos:
O projeto se utilizará da imagem do rosto do usuário, para isso, deve ser trabalhado de acordo com a LGPD.
Para isso, juntamente com o teste e a utilização do produto, há um termo de conscientização e de aceitação de uso de imagem pelo projeto.

# Meios de coleta de dados:
## Questionário:
Antes da utilização da aplicação pelo usuário, o mesmo deve preencher um questionário para análise. <br>
Link: https://forms.gle/L7Jg8UU5BZrddnmZ7

Antes da utilização da aplicação pelo usuário, o mesmo deve participar de uma entrevista para análise. <br>
Link: https://forms.gle/8g5qw6PbaMjYnkrv7

Depois  da utilização da aplicação pelo usuário, o mesmo deve participar de um questionário de avaliação  de feedback para análise.
Link: https://docs.google.com/forms/d/e/1FAIpQLSd9G9Rf3yw6F7WKJcFMYrEKmHNcrv0TJB_HqQ7ZTZgRZaO6cQ/viewform?usp=publish-editor
# Cenário de interação
## Cenário
**Cenário de problema:** Geração automatizada de datasets de expressões faciais durante sessões de jogos digitais <br>
**Atores:** Lucas Andrade (pesquisador/desenvolvedor), Marina Costa (usuária/jogadora), Ana Ribeiro (analista de dados) <br>

Na fase inicial de testes do projeto, Lucas Andrade, pesquisador responsável pelo desenvolvimento da ferramenta, precisa coletar e organizar dados para treinar o modelo de reconhecimento de emoções baseado em Deep Learning [1]. Ele é o responsável por configurar o sistema e supervisionar as sessões de coleta, garantindo que as informações sejam devidamente registradas e validadas.

Durante a primeira sessão de testes [2], Marina Costa, jogadora voluntária, acessa o sistema de coleta com seu login e concede autorização para o uso de sua imagem e dados faciais [3]. Assim que a sessão de jogo começa, o sistema ativa automaticamente a webcam do computador e inicia a captura das expressões faciais de Marina em tempo real. Cada frame é processado, e a ferramenta utiliza o modelo DeepFace para identificar emoções predominantes como alegria, frustração, surpresa ou concentração [4].

A cada nova captura, os dados são armazenados localmente e enviados para o banco de dados do sistema, que organiza automaticamente as imagens de acordo com o tipo de emoção e o contexto em que foram registradas [5]. Lucas acompanha remotamente o andamento da coleta e recebe relatórios automáticos de status de cada sessão [9].

Durante o processo, o sistema detecta que a iluminação do ambiente variou de forma significativa, o que pode comprometer a qualidade das imagens. Uma notificação é enviada a Lucas, sugerindo ajustes automáticos de contraste e brilho na webcam [11]. Ele aceita a sugestão e a ferramenta aplica as correções sem interromper a sessão, otimizando o desempenho da captura [12].

Após o término da jogatina, o sistema gera um relatório automático contendo: número total de imagens coletadas, tempo de gravação, emoções predominantes e nível de confiança médio das classificações [10]. Esse relatório é armazenado no servidor e disponibilizado para Ana Ribeiro, analista de dados responsável pela validação e curadoria dos datasets.

Ao acessar o sistema, Ana visualiza todas as sessões realizadas e inicia a etapa de verificação dos dados [6]. Ela observa que algumas imagens foram classificadas de forma incorreta devido a expressões ambíguas ou mudanças bruscas de iluminação. O sistema, então, oferece uma ferramenta de revisão manual, permitindo que Ana corrija as classificações e marque amostras problemáticas para descarte [7].

Para corrigir inconsistências, o sistema entra automaticamente em contato com o jogador responsável (neste caso, Marina) solicitando autorização para o uso das imagens corrigidas e confirmando a liberação dos dados para fins de pesquisa [8]. Marina recebe a notificação por e-mail e acessa um link de confirmação, validando sua participação e a utilização dos dados capturados [13].

Concluída a etapa de curadoria, Ana aprova o dataset final, que é consolidado e salvo em um formato padronizado para uso em futuros treinamentos de modelos de IA. O sistema envia uma notificação para Lucas, confirmando a conclusão do processo, e outra para Marina, informando que seus dados foram oficialmente incluídos no dataset validado [14].

## Perguntas de cenário
1. Quem pode/deve iniciar a coleta e o cadastro dos dados de expressões faciais no sistema?
2. Quando são capturados e armazenados os dados de expressões faciais dos jogadores?
3. Quem fornece os dados de imagem e consentimento para o sistema?
4. Quais dados (imagens, classificações, metadados) devem ser armazenados no dataset final?
5. Quantos datasets ou sessões de captura são realizados em cada período de teste?
6. Quem pode supervisionar e validar os resultados de uma sessão de captura?
7. Que dados são necessários para cadastrar um novo participante (jogador)?
8. Como são obtidos e processados os dados de um participante durante a sessão?
9. De quem depende a conclusão e validação da geração do dataset final?
10. De que informações o pesquisador precisa para confirmar a qualidade das capturas?
11. Como o sistema pode ajustar ou confirmar automaticamente as condições de captura?
12. Em que pontos a interação entre jogador e sistema pode ser mais eficiente?
13. Como entrar em contato com um participante para confirmar o uso dos dados?
14. Quem precisa ser notificado da conclusão e validação do dataset?

## Design Centrado na Comunicação
| Tópico | Falas e signos |
| -------- | ------- |
| Iniciar sessão de captura | U: Quero iniciar uma nova sessão de captura de expressões faciais.<br>D: OK. Deseja associar a sessão a um jogo específico ou deixar em modo genérico?<br>U: Modo genérico, vou testar em um jogo qualquer.<br>D: A webcam será ativada e as capturas ocorrerão em tempo real. Confirma o início? |
| > Configurar captura | U: Sim. Mas quero ajustar a resolução para 720p e definir o intervalo de captura em 2 segundos.<br>D: Configuração salva. Parâmetros definidos: vídeo 720p, intervalo 2s. |
| > Calibrar reconhecimento facial | D: Antes de começar, precisamos calibrar o reconhecimento. Olhe para a câmera e mantenha uma expressão neutra.<br>U: Certo.<br>D: Calibração concluída. Expressão neutra registrada como referência. |
| > Iniciar coleta de dados | D: A coleta será iniciada agora. O sistema capturará expressões faciais e classificará emoções em tempo real.<br>U: OK.<br>D: Primeiras capturas realizadas. Emoções detectadas: neutra, surpresa, alegria. |
| > Consultar resultados parciais | U: Quero ver o resumo das emoções capturadas até agora.<br>D: Foram registradas 120 imagens: 45 neutras, 50 alegres, 25 surpresas.<br>U: Quero excluir as imagens com baixa confiança.<br>D: Removendo 12 imagens com probabilidade abaixo de 70%. |
| > Rotular e salvar dataset | D: Deseja gerar um dataset com as imagens validadas?<br>U: Sim.<br>D: Informe o nome do dataset.<br>U: “Emoções_GameTest_01”.<br>D: Dataset gerado com sucesso e armazenado em /datasets/Emoções_GameTest_01. |
| > Revisar classificações | U: Quero verificar as classificações feitas pelo sistema.<br>D: Mostrando 10 imagens com suas respectivas emoções detectadas. Deseja corrigir manualmente alguma delas?<br>U: Sim, altere “neutra” para “tristeza” em duas imagens.<br>D: Correções aplicadas. |
| > Exportar dataset | D: Deseja exportar o dataset em qual formato? (CSV, JSON, ou TensorFlow TFRecord)<br>U: CSV e JSON.<br>D: Exportação concluída. Os arquivos estão prontos para download. |
| > Encerrar sessão | U: Quero encerrar a sessão de captura.<br>D: Deseja salvar a configuração atual como um perfil padrão?<br>U: Sim, nomeie como “Captura Padrão 720p_2s”.<br>D: Perfil salvo. Sessão encerrada com sucesso. |
<br>

 Os outros cenários e derivados: https://docs.google.com/document/d/1YYrUdm6h7E00gUmF2o5TV_LmPQy0TSghKg02urThFSE/edit?usp=sharing

# Mapa de Objetivo
| Tipo de objetivo | formulação: usuário | 
|--------------------|------------------|
| final | Quer utilizar o sistema para gerar Datasets de imagens de rostos classificados de acordo com a expressão     |
| instrumental | quer aumentar a eficiência na geração de dataset enquanto realiza outra atividade     |
| instrumental direto | quer gerar dataset de forma mais rápida para utilizar em coleta de dados com contexto ou treinamento de modelos de IA     |
| instrumental indireto | quer gerar dataset de expressões de usuários com a tela para identificar o contexto que motivou a expressão e acumular dados para futuras análises que podem gerar resultados com informações do ambiente ou cenário que o usuário se encontrava. |

<img width="379" height="520" alt="image" src="https://github.com/user-attachments/assets/aec83cea-bf9c-43c2-af29-a73fb2f9401e" />




# Esquema conceitual de signos: conteúdo
<table>
  <tr>
    <th><strong>Criar dataset (C) - funcionalidade de criação de dataset</strong></th>
  </tr>
  <tr>
    <td><strong>signo</strong></td>
    <td><strong>origem</strong></td>
    <td><strong>observações</strong></td>
  </tr>
  <tr>
    <td>quantidade de capturas</td>
    <td>domínio</td>
    <td>indica a quantidade de capturas, quanto mais capturas, melhor o sistema opera</td>
  </tr>
   <tr>
    <td>tempo de intervalo entre capturas</td>
    <td>domínio</td>
    <td>indica de quanto em quanto tempo serão realizadas as capturas</td>
  </tr>
  <tr>
    <td>capturas restantes</td>
    <td>domínio</td>
    <td>indica quantas capturas ainda faltam para a finalização do processo</td>
  </tr>
  <tr>
    <td>captura finalizada</td>
    <td>domínio</td>
    <td>indica que todas as capturas já foram realizadas e que o usuário pode ir para o próximo passo</td>
  </tr>
</table>

# Esquema conceitual de signos: prevenção e recuperação de rupturas comunicativas
<table>
  <tr>
    <th><strong>Criar dataset (C) - funcionalidade de criação de dataset</strong></th>
  </tr>
  <tr>
    <td><strong>signo</strong></td>
    <td><strong>prevenção</strong></td>
    <td><strong>recuperação</strong></td>
  </tr>
  <tr>
    <td>quantidade de capturas</td>
    <td>PP + AL : campo numérico obrigatório</td>
    <td>RA</td>
  </tr>
   <tr>
    <td>tempo de intervalo entre capturas</td>
    <td>PP + AL: campo numérico obrigatório</td>
    <td>RA</td>
  </tr>
  <tr>
    <td>capturas restantes</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>captura finalizada</td>
    <td>-</td>
    <td>-</td>
  </tr>
</table>

### Mapa de objetivos Thiago Alberto Mendes
| tipo de objetivo | formulação |
|-----------|-----------|
| final   | Quer utilizar o sistema para  criar um jogo de renome, que aumente a fama da empresa.|
| instrumental   | Utiliza a definição de quantidade de capturas, intervalo de captura e jogo a ser jogado para facilitar o processo.   |
| instrumental direto   |  Caso o usuário já tenha passado pelos dois primeiros passos uma vez, poderá partir para a execução do projeto em todas as outras execução, clicando em iniciar reconhecimento.   |
| instrumental indireto   | Uma vez realizada a captura de imagens para treinamento, não será necessários esses passos novamente.   |

## MOLIC
### Criar Dataset
<img width="472" height="492" alt="criar" src="https://github.com/user-attachments/assets/3dfb91a0-9cf6-4e4b-b148-e930e9de772a" />

### Treinar Dataset
<img width="678" height="602" alt="molic2" src="https://github.com/user-attachments/assets/f5314c68-ee06-4796-8f4b-7178e9e7f4bd" />

<br>

### Iniciar Captura
<img width="671" height="587" alt="molic3" src="https://github.com/user-attachments/assets/3ec1f0bd-27d6-4f35-af56-1b2210035ae3" />

## FIGMA
### Main
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/debaba14-dcce-4734-a0ec-fd383d0623e4" /><br>
### Info
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/cccbcbc7-6b8d-49ed-8837-022d943eaa8a" /><br>
### FaceCam
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/c7af8e40-dfbb-4b9d-b409-342404fa1672" /><br>
### FaceCam & Screen
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/d6990e62-c9b3-47dc-b797-d84a2d42042b" /><br>
### Train
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/f8bb6fb8-c66b-4253-82c9-ff4c6b6ef6d9" /><br>
### How to use
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/8867919f-142b-46d4-a92b-dea63ef34f89" /><br>
### HUB
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/db5afb38-0c6d-4230-9f27-8afcdfa7bd40" /><br>

## Planejamento de usabilidade:
D: Analisar o uso do software. <br>
E: O usuário entendeu como usar sozinho? O usuário conseguiu obter um resultado satisfatório? O programa foi intuitivo? <br>
C: Nielsen. São 10 regras que visam o bom funcionamento e boa interatividade com o usuário. <br>
I: Entrevistas e questionários para interação com usuários, assim como reuniões para tratar de projeções futuras do projeto. <br>
D: Antes do usuário utilizar o produto, deverá concordar com um termo de autorização de uso de imagem, caso não aceite, sairá do programa. Na fase de testes, os testadores tiveram de assinar um termo físico de uso de imagem. <br>
E: Ao finalizar os testes, os testadores devem preencher um formulário que possui perguntas relacionadas ao projeto, funcionamento, usabilidade. <br>

## Lista de instrumentos:
* Entrevista;
* Questionários;
* Avaliação posterior ao uso do programa.

<!--
#### Avaliação heurística

### Prtotipação em médio nível (Figma) (A FAZER)
#### Avaliação heurística

### Prtotipação em alto nível (React) (A FAZER)
#### Avaliação heurística

[^1]: Fonte: Adaptado de <https://hazeshift.com.br/mapa-de-empatia/>

<!-- TODOs:
- Add exemplos
 -->
