.. Guia diff-in-diff com R e Rstudio documentation master file, created by
   sphinx-quickstart on Wed Jul 29 16:33:37 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Bem Vindos!
===========

Este é um guia de como mensurar os impactos das políticas da FAP-DF. Nele você irá aprender a utilizar o software "R", umas das principais ferramentas utilizadas pelos cientistas de dados. 

É importante lembrar que a implementação de programas públicos demanda recursos cada vez mais escassos tornando a necessidade de avaliações de eficiência e efetividade de sua aplicação. Os recursos públicos apresentam um “custo de oportunidade”. Em economia, o custo de oportunidade é um conceito teórico que mede o custo daquilo que se poderia fazer em vez daquilo que se está fazendo. Nesse sentido, a avaliação de programas públicos permite mensurar o impacto dessa política, auxiliando a comparação com o custo de oportunidade a fim de:

   1. escolher o melhor programa dentre várias possibilidades;

   2. descontinuar programas que não têm um impacto/benefício significativo;

   3. evitar acabar com programas que têm impacto/benefício expressivos;

   4. melhorar o desenho do programa, sua custo-efetividade e eficácia; e

   5. decidir sobre a replicação ou ampliação do programa.

Mais especificamente, as avaliações de impacto medem mudanças em um resultado de interesse atribuídas a uma intervenção (tratamento/programa) específica. O foco se dá nos resultados (como desempenho escolar e emprego) e, somente em alguns casos, nos produtos (como atendimentos, matrículas e formandos). Para tanto, é necessário dados de um grupo exposto ao programa (tratados) e de um grupo não exposto (controle), além de um corte temporal de antes e depois da implantação do programa.

Neste guia, a fim de facilitar o entendimento, iremos apresentar uma sugestão de avaliação da efetividade da iniciativa prevista no Edital nº 10/2019 da FAPDF, que refere-se à seleção pública de propostas de apoio à participação em eventos de natureza científica, tecnológica e de inovação para docentes da rede pública de ensino do Distrito Federal.

Iremos sugerir a utilização de três indicadores: esforço docente, nota do Enem e média escolar. Por meio do modelo econométrico chamado *diferenças em diferenças* ou diff in diff, vamos mensurar os impactos da política previsa no Edital em análise e interpretar os resultados. 

================
Exemplo de vídeo
================

.. raw:: html

   <div style="text-align: center; margin-bottom: 2em;">
    <iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/F5mRW0jo-U4" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
   </div>
   


.. toctree::
   :caption: Primeiros passos
   :hidden:

   intro/motivacao
   intro/instalacao
   intro/rstudio

.. toctree::
   :caption: R Básico
   :hidden:

   r101/introdução
   r101/objetos
   r101/funções
   r101/gráficos

.. toctree::
   :caption: Econometria
   :hidden:

   econometria/Avaliação de Impacto de Políticas Públicas
   econometria/regressões
   econometria/did

.. toctree::
   :caption: Prática
   :hidden:

   pratica/introducao
   pratica/1_exemplo
   pratica/2_exemplo
   pratica/3_exemplo
   
