""""""""""
Introdução
""""""""""

===================
Elementos Essencias
===================

-----------------
Como pedir ajuda?
-----------------

Na sua jornada como programador, você irá se deparar diversas vezes com assuntos desconhecidos, bugs e outra infinidade de momentos em que você sentirá a necessidade de ajuda.

No próprio Rstudio, existem formas de você sanar várias de suas dúvidas. 

.. code-block:: r

	# digite este código no seu console e pressione Enter
	help.start()

Essa função abrirá, na aba *Help*, os principais links do R, com praticamente tudo que se tem de fundamental sobre a linguagem.

Outra situação é quando você se deparar com funções que você não conhece. Por exemplo, vimos na seção anterior que a função *rnorm* cria uma lista de números normalmente distribuídos, mas se não soubessemos o que a função faz poderiamos digitar:

.. code-block:: r

	help(rnorm)

E na seção *Help* será aberta a documentação dessa função, com sua descrição, forma de usar, argumentos que aceita, detalhes e etc. Isto é muito poderoso! Sempre que você se deperar com uma função que não sabe o funcionamento ou não se lembra exatamente quais argumentos ela aceita, você poderá invocar o help dessa função. De forma geral:

.. code-block:: r

	# para qualquer função
	help(nome_da_função)

O mais comum de se acontecer é que você mesmo após ler o help da função, você ainda necessite de mais informações e existem alguns sites que podem te auxiliar.

O StackOverflow é um site de perguntas e respostas ao estilo "Yahoo Respostas", que basicamente "possui todas as dúvidas do mundo". Isto porque muito provavelmente algum programador já se deparou com a mesma dúvida que você e fez uma pergunta no site.

Outro site muito conhecido é o Github. É nele que a maioria dos programadores do mundo todo armazenam seu código, então é possível entender mais como outras pessoas trabalham e ler toneladas de código.

Por último, a todo momento você irá se deparar com erros no seus programas - os chamados bugs - e é importante que você não tenha medo deles e se disponha a entender o erro. Por exemplo, vamos rodar o seguinte código:

.. code-block:: r

	> 'a'/2
	Error in "a"/2 : argumento não-numérico para operador binário
  
Veja que dividir a letra 'a' por 2 resulta em um erro, que me diz que nao posso dividir algo não-númerico, uma letra por exemplo, por um operador binário, no caso um número.

Esse exemplo pode parecer esdrúxulo, mas salienta que lendo o Erro é possível entender o que aconteceu de errado. Entrentanto, na maioria das vezes outras pessoas já tiveram o mesmo erro que você, então vale a pena pesquisar na internet essa mensagem de Erro.

-------
Pacotes
-------

O R é uma ferramenta incrível que possui diversas funcionalidades e uma imensidão de usuários. Essa característica permitiu a criação de um universo de pacotes que tem o objetivo de dar ainda mais poder para quem utiliza o R.

Pacotes são códigos já escritos por terceiros, que você poderá utilizar nos seus *Scripts* sem precisar recriar tudo.

O Tidyverse é um conjunto de pacotes para manipulação e extração de dados muitíssimo utilizado. É composto pelo 'ggplot2' para manipulação de dados, o 'tidyr' para limpeza, o 'dplyr' para manipulação e alguns outros pacotes. O Tidyverse é apenas um exemplo da importância que os pacotes tem hoje em dia na comunidade R, existem ainda milhares de pacotes que podem ser encontrados no CRAN em https://cran.r-project.org/.

Para instalar ou remover pacotes, siga as instruções a seguir

.. code-block:: r

	# Instalando um pacote
	install.packages("tidyr")

	# Instalando vários pacotes
	install.packages(c("plyr", "tidyr", "dplyr"))
	

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