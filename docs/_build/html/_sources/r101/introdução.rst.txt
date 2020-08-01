""""""""""
Introdução
""""""""""


*Em construção*


===================
Elementos Essencias
===================

*Em construção*

-----------------
Como pedir ajuda?
-----------------


No Rstudio

.. code-block:: r

	# Principais links do R
	help.start()

	# Abre a ajuda de uma função específica
	help(nome_da_funcao)

	# Demonstra funcionalidades do R e seus pacotes
	demo()

Online:

- Google 
- Stackoverflow
- Github
- Log de erro
  

-------
Pacotes
-------

**Instalar pacotes**

.. code-block:: r

	# Instalando um pacote
	install.packages("tidyr")

	# Instalando vários pacotes
	install.packages(c("plyr", "tidyr", "dplyr"))

**Remover Pacotes**

.. code-block:: r

	# Removendo um pacote
	remove.packages("tidyr")

	# Removendo vários pacotes
	remove.packages(c("plyr", "tidyr", "dplyr"))

--------
Ambiente
--------

.. code-block:: r

	# Exibe a versão atual do R
	version

	# Mostra tudo que está carregado no ambiente
	ls()

	# Retorna o diretório de trabalho atual
	getwd()

	# Lista as pastar e arquivos atual
	dir()

	# Define um caminho do diretório de trabalho
	setwd()




=======================
Operadores e Sequências
=======================

*Em construção*

------------------------
Operadores de Atribuição
------------------------

.. code-block:: r

	# Atribuo o valor 5 à variável 'x'
	x <- 5

	# Também é possível atribuir com =
	x = 5


----------------------
Operadores Aritméticos
----------------------

.. code-block:: r

	# Soma +
	2 + 2

	# Subtração -
	10 - 4

	# Multiplicação *
	5 * 4

	# Divisão /
	10 / 5

	# Exponenciação ^
	3 ^ 2

	# Resto da divisão %%
	10 %% 3


----------------------
Operadores Relacionais
----------------------

.. code-block:: r

	# maior que >
	10 > 2

	# menor que <
	3 < 1

	# igual a ==
	10 == 10

	# maior ou igual a >=
	5 >= 5

	# menor ou igual a <=
	3 <= 4

	# diferente de !=
	7 != 6




------------------
Operadores Lógicos
------------------

.. code-block:: r

	# Retorna verdadeiro se ambas as condições forem verdadeiras 
	10 > 5 & 6 < 13

	# Retorna verdadeiro se pelo menos uma condição for verdadeira
	3 > 2 | 10 > 4




----------
Sequências
----------

Função:
	- Loop
	- Repetições
	- Amostras aleatórios

--------------------
Sequências Regulares
--------------------

**rep( ) e :**

.. code-block:: r

	# repete 10 vezes o número 4
	rep(4, 10)

	# cria uma sequência de 0 à 5
	0:5

**seq( )**

.. code-block:: r

	# de 0 a 10 
	seq(from = 0, to = 10)

	# de 0 a 10, de 2 em 2
	seq(from = 0, to = 10, by = 2)

	# sequência com 10 número entre 0 e 1
	seq(from = 0, to = 1, length.out = 10)





--------------------
Sequência Aleatórias
--------------------

**sample( )**

.. code-block:: r

	# cria uma sequência de 1 a 50
	seq <- 1:50

	# cria uma amostra com 10 elementos da sequência 'seq'
	y <- sample(x = seq, size = 10)

	# O mesmo que o anterior mas com repetição
	z <- sample(x = seq, size = 10, replace = TRUE)

**Famílias de distribuição de probabilidades**

.. code-block:: r

	# as sequências terão 20 números
	N <- 20

	runif(N) # Uniforme
	rnorm(N) # Normal
	rpois(N) # Poisson
	rexp(N) # Exponencial



=======================
Estruturas de repetição
=======================

-----------------------
Estruturas Condicionais
-----------------------

**if**

.. code-block:: r
	
	if(condição){
		faça alguma coisa
	}
	saia


	# exemplo
	x <- 1
	# se 'x' for igual a 1, então imprima o valor de 'x'
	if(x == 1){
		print(x)
	}


**else**

.. code-block:: r

	if(condição){
		faça alguma coisa
	} else {
		faça outra coisa 
	}


	# exemplo
	x <- 1
	# x não é igual a 2, então imprima "estou no else"
	if(x == 2){
		print(x)
	} else {
		print("estou no else")
	}

**if - else - if**

.. code-block:: r
	
	if(condição 1){
		print("parei na condicao 1")
	} else if(condicao 2){
		print("parei na condicao 2")
	} else if(condicao 3){
		print("parei na condicao 3")
	} else {
		print("nenhum condicao era verdade")
	}



-----------------------
Estruturas de Repetição
-----------------------

**for**

.. code-block:: r
	
	for(i in sequencia){
		faça alguma coisa que se repete
	} 


	# exemplo: imprime os números de 0 a 5
	x <- 0:5
	for(i in x){
		print(i)
	}

**while**

.. code-block:: r

	inicio
	while(condicao){
		faça alguma coisa
	} 
	atualizar inicio


	# Exemplo: o código vai imprimir de 0 a 5
	x <- 0
	while(x <= 5){
		print(x)
		x <- x + 1
	}

**repeat**

.. code-block:: r

	repeat{
		if(condicao){
			break
		} else {
			faca isso
		}
	}