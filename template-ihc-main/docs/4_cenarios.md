# Cenário de Análise/Problema
<!--
> **_NOTE:_**: A equipe deve pensar em cenários existentes na atualidade (que causam problemas para os usuários) e que a interface prevista ajudará a resolver o problema. Cenário de Análise/Problema é uma história triste. Não descreve a solução. Descreve somente o problema.

1. Cenário de Análise/Problema
2. Questões de Refinamento
3. Refinamento do Cenário Análise/Problema
-->
### Thiago Alberto Mendes:
#### Perguntas:

### Valter Alter  
#### Perguntas de refinamento: <br>
1 - Onde a interação ocorre? Quais recursos estão disponíveis? Há restrições físicas, técnicas ou sociais? <br>
2 - Quem são os usuários principais e secundários? Quais características influenciam o uso da aplicação? <br>
3 - O que o usuário deseja alcançar? Há objetivos secundários? <br>
4 - Como o usuário pretende atingir esses objetivos? Ele define uma estratégia? <br>
5 - Quais passos o usuário executa? São automáticos ou manuais? <br>
6 - Que acontecimentos externos influenciam a interação? <br>
7 - Como o usuário interpreta os resultados? Há métricas de sucesso? <br>
8 - O que leva o usuário a usar a aplicação? <br>
9 - O usuário já tem experiência com tarefas semelhantes? <br>
10 - Com que regularidade a aplicação será usada? <br>
11 - Existem barreiras técnicas, sociais ou financeiras? <br>
12 - Que apoios ou ferramentas externas são usados? <br>
13 - Que tipo de retorno o usuário recebe da aplicação? <br>
14 - O que o usuário espera a longo prazo? <br>

#### Atores:
Valter Alter, 58 anos, criador de conteúdo para jogos digitais no canal ClickGamesBR (1,3 milhão de inscritos no YouTube). Seus seguidores frequentemente pedem novidades, incluindo jogos que respondam às emoções dos jogadores.

#### Narrativa:
Valter está em seu escritório, equipado com um computador gamer de alto desempenho e uma webcam HD posicionada sobre o monitor [Q1]. Ele decidiu atender aos pedidos de seus seguidores criando um protótipo de jogo interativo baseado em emoções. Para isso, precisa coletar e organizar vídeos que relacionem expressões faciais e momentos de gameplay [Q2].

Seu objetivo é gerar datasets de qualidade que possam ser usados para treinar um modelo de reconhecimento de emoções, reduzindo o tempo que ele gastaria se fizesse esse processo manualmente [Q3]. Ele planeja organizar campanhas no canal, pedindo para seguidores enviarem trechos de gameplay gravados com facecam, mas antes deseja testar a ferramenta com sua própria captura [Q4].

Valter abre a aplicação, conecta a webcam e inicia o processo de captura [Q5]. Ele executa um jogo de ação em seu PC enquanto a ferramenta grava automaticamente suas expressões faciais em paralelo. Durante a sessão, algumas interrupções ocorrem: a iluminação ambiente interfere na precisão da captura e a webcam apresenta um pequeno delay [Q6].

Ao final, a ferramenta gera um dataset com imagens rotuladas automaticamente. Valter avalia o resultado, observando que, apesar de alguns erros de classificação, a ferramenta poupou horas de trabalho manual e já fornece um material consistente para testes [Q7]. Ele conclui que, com pequenos ajustes de iluminação e configuração, poderá expandir o uso da ferramenta para o público do seu canal.

### Gabriel Cavalcante:
#### Perguntas de refinamento:
1. Por que o ator quer utilizar a ferramenta?
2. Quais as pré-condições para a utilização?
3. Quem pode utilizar a ferramenta?
4. Como é feito o processo de utilização?
5. Como o usuário sabe que o processo acabou?
6. Qual é o resultado da utilização da ferramenta?
7. Para que a ferramenta é utilizadda?
8. A ferramenta pode ir além?
9. A ferramenta é fácil de ser utilizada?
10. Como deve ser o ambiente?
11. O projeto usa qual artifício como base de processamento?
12. A ferramenta trabalha em qualquer hardware?

#### Atores:
Gabriel Cavalcante, 43 anos, trabalha na empresa MindPlus. Semanalmente precisa criar datasets para outras empresas, cujo foco é o desenvolvimento de jogos.

### Narrativa:
Gabriel, está em seu escritório dentro das instalações da empresa MindPlus. [1] Ele necessita da disponibilização de dataset a partir de um jogo específico de terror, chamado Outcast.
Neste projeto é necessário que as [11] emoções das pessoas sejam correlacionadas com o que está acontecendo no jogo, elementos, criaturas. Depois de pesquisar, [7] encontrou uma ferramenta facilitadora de criação de datasets que [3] poderia ser usada por qualquer pessoa, com o mesmo propósito que estava buscando.
Para testar, [2] viu que necessitava de uma webcam, [10] um espaço bem iluminado, sem muito movimento e de um [12] computador de média potência para operar. Ao iniciar o teste, [4] foram tiradas várias capturas para o treinamento da ferramenta, depois realizou o treinamento e, por fim, conseguiu entrar no jogo e, [5] depois de terminada a sessão, [6] ver os resultados correlacionados.
A partir dela, conseguiu, por meio de capturas de emoções e de cenário, contribuir com o projeto de maneira rápida, efetiva e de [9] uma maneira simplificada e inutitiva, [8] conseguindo ainda publicar o dataset publicamente para uso.
<br>
