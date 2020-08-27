""""""""
Gráficos
""""""""

R tem grande flexibilidade para gráficos.
Base Graphics = existe desde os primórdios do R
lattice Graphics = uma versão mais atual, traz novos recursos
ggplot = trás a ideia de uma biblioteca gráfica

ggplot é o mais completo: flexibilidade e possibilidade
Faremos os gráficos estatisticos mais comuns

================
Gráficos básicos
================

- É o sistema mais antigo
- Utiliza o sistema de grid(x,y)
- Não é muito flexível para gráficos em grupos
  
.. code-block:: r

    # carrega um grande conjuntos de parâmentros gráficos
    par()

    # margens, números de figuras
    ?par()

    # dividi a área gráfica em mutias linhas e colunas
    layout()




=====================
Gráficos com "ggplot"
=====================
