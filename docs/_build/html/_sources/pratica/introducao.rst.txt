""""""""""
Introdução
""""""""""

A fim de facilitar a reprodução de um modelo econométrico para avaliação de política pública, iremos realizar um passo a passo de uma proposta de avaliação da efetividade da iniciativa prevista no Edital nº 10/2019, por meio de um modelo de diferenças em diferenças (diff-in-diff).

Conforme apresentado na parte teórica, a amostra deve ser dividida em quatro grupos: o grupo de controle anterior à mudança, o grupo de controle após a mudança, o grupo de tratamento anterior à mudança e o grupo de tratamento depois da mudança. Ademais o modelo diff-in-diff deve seguir o seguinte modelo:

indicador = α + β1 · grupo_tratado i · pós_tratamento t + β2 · grupo_tratado i +
+ β3 · pós_tratamento i + ε i
  
De acordo com o edital em análise, a iniciativa refere-se à seleção pública de propostas de apoio à participação em eventos de natureza científica, tecnológica e de inovação para docentes da rede pública de ensino do Distrito Federal. Está prevista a seleção de até 80 propostas (60 nacionais e 20 internacionais) habilitadas e/ou ao limite da disponibilidade orçamentária e financeira da FAPDF, no primeiro ano de vigência.

O objeto do Edital é o apoio à apresentação de trabalhos em eventos de ciência, tecnologia e inovação no país ou no exterior, que tenham sido selecionados por instituições de reconhecida capacidade científica, técnica e pedagógica. Já o público alvo são os docentes e estudantes da Rede Pública de Educação Básica do Distrito Federal.

Uma dificuldade comum na avaliação de políticas públicas diz respeito à escassez de dados, sobretudo em relação ao modelo diff-in-diff. Nesse sentido, buscaremos, ao máximo, utilizar indicadores já existentes, como, por exemplo, os produzidos pelo Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira – INEP. No entanto, para um estudo econométrico preciso, é necessário o acompanhamento do grupo de controle, de modo que o impacto da política possa ser mensurado.

Nesse sentido, considerando que o objetivo dos exemplos práticos é demonstrar o passo a passo e devido à falta de dados disponíveis no momento de sua elaboração, iremos utilizar bases de dados simuladas.