""""""""""""""""""""""""
Diferenças em Diferenças
""""""""""""""""""""""""

Conforme apresentamos, a amostra deve ser dividida em quatro grupos: o grupo de controle anterior à mudança, o grupo de controle após a mudança, o grupo de tratamento anterior à mudança e o grupo de tratamento depois da mudança. Ademais o modelo diff-in-diff deve seguir o seguinte modelo:

indicador = α + β1 · grupo_tratado i · pós_tratamento t + β2 · grupo_tratado i +
+ β3 · pós_tratamento i + ε i

Dito isso, considerando os indicadores, os modelos são:

i.	esforço docente = α + β1 · grupo_tratado i · pós_tratamento t + β2 · grupo_tratado i +
+ β3 · pós_tratamento i + ε i

ii.	regularidade do docente da educação básica = α + β1 · grupo_tratado i · pós_tratamento t + β2 · grupo_tratado i + + β3 · pós_tratamento i + ε i

iii.	adequação da formação do docente = α + β1 · grupo_tratado i · pós_tratamento t + β2 · grupo_tratado i + + β3 · pós_tratamento i + ε i

iv.	taxa de abandono escolar = α + β1 · grupo_tratado i · pós_tratamento t + β2 · grupo_tratado i + + β3 · pós_tratamento i + ε i

v.	taxa de aprovação = α + β1 · grupo_tratado i · pós_tratamento t + β2 · grupo_tratado i + + β3 · pós_tratamento i + ε i

Este relatório parcial demonstra o modelo e a forma que poderá ser feita a avaliação. A seguir, iremos apresentar um manual com algoritmos e o passo a passo para rodar um regressão DIFF and DIFF no R (ferramenta gratuita e amplamente utilizada) para que servidores com um mínimo de capacitação em econometria aplicada possam rodas avaliações futuras deste e outros editais para os quais esta metodologia se aplica.
