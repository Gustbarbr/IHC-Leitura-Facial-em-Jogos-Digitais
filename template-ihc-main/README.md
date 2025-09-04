# Projeto de Interface Humano-Computador

Projeto apresentado ao Centro Universitário [FEI](https://portal.fei.edu.br/), como parte dos requisitos necessários para aprovação na disciplina de Interface Humano-Computador (CC8122) do curso de Ciencia da Computação, orientado pelo Prof. Dr. [Fagner de Assis Moura Pimentel](http://lattes.cnpq.br/6747210702910392) e Prof. Dr. [Plino Thomaz Aquino Junior](http://lattes.cnpq.br/6186413528999908).

Este projeto se baseia no Trabalho de Conclusão de Curso (TCC) entitulado **Título do TCC** sob orientação do Professor **Nome do Orientador** e desenvolvido pelos seguintes alunos:

- Nome: Gustavo Gomes Barbosa | RA: 24.122.061-5
- Nome: Pedro Munhoz Rosin | RA: 24.122.013-6
- Nome: Alan Daiki Suga | RA: 22.125.094-7

## Conhecendo o problema

Sobre o produto ou serviço que seu grupo está desenvolvendo, responda:
- Apresente uma breve descrição.
- Apresente o objetivo. 
- Apresente o usuário final.
- Apresente os principais benefícios para o usuários.
- Apresente as funcionalidades.
- Apresente as tecnologias e ferramentas computacionais utilizadas.
- Apresente o contexto de uso.
- O produto ou serviço prevê o desenvolvimento de interface? (Sim/Não)

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


## Desenvolvimento
- [Análise de Concorência](docs/2_concorencia.md)
- [Personas](docs/3_personas.md)
- [Cenário de Análise/Problema](docs/4_cenarios.md)
- [Análide de Tarefas](docs/5_analise_tarefas.md)
- [Prototipação em Papel]()
- [Coleta de Dados]()
- [Ciclo de vida da engenharia de usabilidade]()
- [Modelo Conceitual]() 
- [MOLIC]()
- [FIGMA]()
- [Planejamento da Avaliação]()
- [Avaliação de IHC através de Inspeção Heurística]()
- [Avaliação de Usabilidade baseado em Observação do Usuário]()
