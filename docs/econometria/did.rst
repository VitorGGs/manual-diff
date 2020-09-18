""""""""""""""""""""""""
O Modelo Diferenças em Diferenças
""""""""""""""""""""""""

No modelo diferenças em diferenças, a amostra deve ser dividida em quatro grupos: o grupo de controle anterior à mudança, o grupo de controle após a mudança, o grupo de tratamento anterior à mudança e o grupo de tratamento depois da mudança. 

Dentro do modelo, utiliza-se as variáveis indicadoras (ou dummys): dB, igual a um para os indivíduos do grupo de tratamento e zero para os indivíduos do grupo de controle; e d2, igual a um quando se referir aos dados do segundo período, após a mudança, e zero caso os dados se refiram ao período anterior à mudança. Assim, temos: 

Y = g0 + g1*d2 + g2*dB + g3*d2*dB + outros fatores 

na qual Y representa a variável em estudo, g1 o impacto no segundo período sobre a variável estudada, g2 o impacto no grupo de tratamento sobre a variável estudada, e g3 o impacto após o evento do grupo de tratamento frente ao grupo de controle sobre a variável estudada. Desse modo, g0 representa o valor esperado da variável em análise quando se estuda o grupo de controle antes da mudança, o que representa o parâmetro de comparação.

No nosso exmeplo de análise do Edital nº 10/2019 da FAPDF, podemos sugerir um modelo no seguinte formato:

indicador = α + β1 · grupo_tratado i · pós_tratamento t + β2 · grupo_tratado i + β3 · pós_tratamento i + ε i

Dito isso, considerando os indicadores, os modelos são:

1.	esforço docente = α + β1 · grupo_tratado i · pós_tratamento t + β2 · grupo_tratado i + β3 · pós_tratamento i + ε i

2.	regularidade do docente = α + β1 · grupo_tratado i · pós_tratamento t + β2 · grupo_tratado i + β3 · pós_tratamento i + ε i

3.	adequação da formação do docente = α + β1 · grupo_tratado i · pós_tratamento t + β2 · grupo_tratado i + β3 · pós_tratamento i + ε i

4.	taxa de abandono escolar = α + β1 · grupo_tratado i · pós_tratamento t + β2 · grupo_tratado i + β3 · pós_tratamento i + ε i

5.	taxa de aprovação = α + β1 · grupo_tratado i · pós_tratamento t + β2 · grupo_tratado i + β3 · pós_tratamento i + ε i

Este exemplo demonstra o modelo e a forma que poderá ser feita a avaliação. A seguir, iremos apresentar um manual com algoritmos e o passo a passo para rodar o modelo diferenças em diferenças no R para que pessoas com um mínimo de capacitação em econometria aplicada possam realizar avaliações futuras deste e outros editais para os quais esta metodologia se aplica.
