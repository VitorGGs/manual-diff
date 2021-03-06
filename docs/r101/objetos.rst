"""""""
Objetos
"""""""

**O que são objetos**

Tudo que existe no R são objetos. Possuem duas propriedades básicas: tipos e atributos. Tipos: vetores, listas, data frames. Atributos: nome, tamanho, dimensões. Formados pelas formas de dado básico. Algumas funções servem para todos os objetos:

.. code-block:: r

	# funções universais

	class()
	typeof()
	names()
	length()
	colnames()
	rownames()
	dim()
	ncol()
	nrow()
	attributes()

	# Exemplo
	objeto <- runif(10)

	names(obj1) <- paste("x", 1:length(objeto), sep = "")
	typeof(objeto)
	class(objeto)
	dim(objeto)
	length(objeto)
	names(objeto)


=======
Vetores
=======

- Objetos atômicos
- índices são as posições do elemento do vetor: começa no 1
- x[i], x[[i]], x$a
- indices negativos subtraem o elemento
  
.. code-block:: r

	# Exemplos de vetores

	vetor1 <- 1:5 
	vetor2 <- c(TRUE, FALSE, TRUE) 
	
	# Acessando elementos
	vetor1[1:2]
	vetor2[3]

---------------------
Operações com Vetores
---------------------

- Com vetores é possível realizar todas as operações matemáticas básicas.
- Ordernar com a função sort( )
 
-----------------
Valores Especiais
-----------------

- NA: valor faltante
- Inf: infinito
- NaN: Not a number
- NULL: falta do elemento



=================
Matrizes e Arrays
=================

- Uma matriz é um objeto bidimensional que possue *m* linhas e *n* colunas
- É como uma planilha do excel que só pode ter um tipo de dado 

------------------
Construir Matrizes
------------------


.. code-block:: r

	matrix()
	rbind()  # agrupa vetores
	cbind()
	as.matrix() # transforma em matrix

	# verificar atributos

	dim() # dimensões
	ncol() # número de colunas
	nrow() # número de linhas
	colnames() # nome das colunas
	rownames()


-------------------
Acessando elementos
-------------------

- v[i, j], linha *i* e coluna *j*
- v[i, ], acessar a linha i inteira
- v[, j], acessar a coluna j inteira

----------------------
Operações com Matrizes
----------------------

.. code-block:: r
	
	# transposição
	t()

	# multiplicação de matrizes
	%*%

	# inversão de matrizes
	solve()


------
Arrays
------

- Arrays são unidimensionais
- c("linhas", "colunas", "camadas")

*Não é interessante explicar*

==========
Caracteres
==========

- Strings são textos
- Construidas com aspas simples ou duplas

---------------------
Operações com Strings
---------------------

.. code-block:: r

	nchar() # número de caracteres 
	cat() # imprimi texto 
	paste() # guarda o valor
	paste0() #
	substr() # extrai partes do texto
	strsplit() # quebra a string baseado em um padrão
	sub() # substitui parte da string baseado em um padrão
	gsub() # mesmo do sub mas para todas as ocorrências
	grep() # localiza padrões na string
	tolower() # converte todos as strings para minúsculo
	toupper() # converte todos as strings para maiusculo

-------
Fatores
-------

- São tipos de string que representam categorias de variáveis

.. code-block:: r

	# "vitor" e "eric" são fatores
	nomes <- c("vitor", "eric", "vitor", "vitor", "eric")

	# retorna os fatores do vetor 'nomes'
	factor(nomes)
	as.factor(nomes)

	# podem ser criado níveis e ordenados
	levels()


====================
Data frames e Listas
====================

- Listas são estruturas em R que podem armazenar vários objetos de tipos diversos.
- Listas são criadas com list( ) e as.list( )
- Podem ser acessadas com operador x[i] ou $(quando nomeadas)
- Você pode aninhar listas dentro de listas
  

.. code-block:: r

	enlatados <- c("molho de tomate", "atum", "milho")
	frios <- c("queijo", "requeijao", "iorgute" )
	orcamento <- c(50, 70)

	compras <- list(enlatados = enlatados, frios = frios, orcamento = orcamento)

-----------
Data Frames
-----------

- Pense em planilhas do excel
- Linha são variáveis e colunas são observações (ou vice-versa)
  

.. code-block:: r

	# construir
	data.frame()
	#ou
	as.data.frame()

	# primeiras e ultimas linhas
	head()
	tail()

	# adicionar coluna
	df$nova_coluna = c(1,2,3)
	cbind()

	# split de df's
	subset()
	split()

	# adicionar linha
	rbind()


===================
Classes e Conversão
===================

- A classe é a identidade do objeto e o R vai tratar esse objeto de acordo com seu tipo
- Um objeto pode ter sua classe mudada
  
.. code-block:: r

	# 


=====
Datas
=====

- Formato POSIX
- % para formatação

.. code-block:: r

   # principais funções
   as.Date()
   Sys.Date()
   Sys.time()

   # pacote lubridate
   library(lubridate)

   