""""""""""""""""""""
Conhecendo o Rstudio
""""""""""""""""""""

Ao instalar o a linguagem R no seu computador, também será instalado a ferramenta padrão básica chamada de GUI(graphic user interface).

.. figure:: ./images/r_gui.JPG
	:align: center
	:class: custom-img

Entretanto, a maioria dos programados e cientistas de dados consideram o R-GUI muito básico e simplista. 

Por isso usaremos o Rstudio como ferramenta para escrevermos nosso código. Algumas vantagens que ele oferece são: *highlight* de linguage, reutilização de código, correção de bugs, *autocomplete* de código e outros tantas ferramentas que aumentam a produtividade no dia a dia.

Após a instalação do Rstudio (ver seção anterior) e a execução do progama, essa será a tela inicial:

.. figure:: ./images/rstudio.png
	:align: center
	:class: custom-img

Em um primeiro momento, pode parecer muito confuso o Rstudio, principalmente se este é o seu primeiro contato com uma IDE. Por isso mesmo, iremos detalhar as principais funções para que você possa se acostumar com a IDE.

Num primeiro momento, vamos criar nosso primeiro *Script*. É nele que vamos escrever o nosso código e passar a maior parte do tempo. Para criar um novo *Script* clique em **file >> New file >> R Script** ou use o atalho **CTRL+SHIFT+N**.

.. figure:: ./images/rstudio_script.png
	:align: center
	:class: custom-img

O Rstudio automaticamente da o nome de "Untitled1" para o script até que você decida nomear e salvar. Experimente digitar qualquer coisa no script!

A maioria das pessoas(como eu) consideram a letra e a cor branca do Rstudio cansativas para visão. Como programadores e cientistas de dados passam diversas horas em frente ao computador, é comum utilizarmos letras maiores e fontes mais escuras.

Caso você também se sinta assim, é possível mudar a fonte e o tema do Rstudio. Para tanto, na barra de ferramentas, acesse ** Tools >> Global Options >> Apperance **. Em **Editor font size** escolherei o tamanho 14, mas sinta-se livre para escolher a que ficar melhor para você. O mesmo vale para o **Editor theme** que irei escolher o *Vibrant Ink*.

Para essas mudanças o Rstudio vai solicitar que o programa seja reiniciado.

.. figure:: ./images/rstudio_tema.png
	:align: center
	:class: custom-img

Agora que já resolvemos o problema visual, vamos entender um pouco mais da ferramenta. Escreve o seguinte código no seu *Script*.

.. code-block:: r

	x <- rnorm(100)

Esse código cria um vetor com 100 números normalmente distribuídos.

Para rodar o seu código existem duas opções: clique na linha do seu código e clique em **Run** ou com o atalho **CTRL+ENTER**.

.. figure:: ./images/rstudio_rodar.png
	:align: center
	:class: custom-img

Observe que várias coisas aconteceram, então vamos por parte.

Na parte de console, foi reproduzido o código que rodamos no nosso *Script*. Isso porque o console é nossa sessão ativa do R, que é muito parecido com o nosso R-GUI. Toda vez que rodarmos um código do nosso *Script*, ele aparecerá no console. Também é possível escrever código no console indepedentemente. Por exemplo, vou acessar o valor dos 100 números que geramos anteriormente. Para isso, basta escrever o nome da variável que está armazenado os dados e apertar Enter.

.. code-block:: r

	> x <- rnorm(100)
	> x
  [1]  0.523269276  1.341866406  1.755126592  0.305038999 -1.404484267
  [6] -0.514027683 -0.243763319 -0.021675211 -1.342548483  0.422455812
 [11] -0.992820486  0.860048278 -1.200263289  0.752367491 -0.947355836
 [16] -0.856189268  0.385041968 -1.017855646  1.705030612 -0.845767124
 [21] -1.059465779  1.561755828 -1.286030749  0.887765696  0.010865802
 [26] -0.340876901 -1.176313898 -1.689736344  0.836616059 -1.457260402
 [31]  0.812465960 -0.419374394 -0.963585796 -0.224716061 -1.212343558
 [36]  0.706112451 -1.611880537 -1.215366154 -0.740974630 -0.162819073
 [41]  0.822798744 -0.376292960 -0.371173265 -0.936063624 -0.817146967
 [46]  0.340212557 -0.117376394  0.911244181 -0.292027961  0.280446669
 [51] -1.447693813 -0.651037578 -0.789687634  0.078407791  1.197559817
 [56] -0.837763286 -1.391829653 -0.298665569 -2.368972380  0.505145586
 [61]  0.655814231  1.378834536  0.051638257 -1.661635372  2.204330120
 [66]  0.212464522 -1.101287709  2.298244177 -0.347502427 -0.631701034
 [71]  0.120059192  1.173714483 -0.059711509 -0.292271979 -1.058833610
 [76]  0.585852160 -0.596242624 -0.463635517 -0.003843688 -0.555720542
 [81]  0.266982664 -1.163902365  1.266956564 -0.565419796  0.016810555
 [86] -0.489056607  0.378912135  1.451784661 -0.680135531  0.130738176
 [91] -0.543489815 -2.971097415  0.001782536  0.455342497  1.124099855
 [96] -0.510042622 -0.486031094  0.072100125  0.379289881 -1.523777870

O console tem muitas utilidades. Nele você verá o resultado do seu código, pode ser utilizado para escrever código de maneira dinâmica, dentre outras coisas.

.. figure:: ./images/rstudio_console.png
	:align: center
	:class: custom-img

Outra mudança que você talvez tenha reparado é na seção **Enviroment**. Essa seção é responsável por mostrar todas os dados presentes numa seção. Observe que como atualemnte, temos apenas a variável 'x' criada no nosso código, isto é tudo que aparece. Mais pra frente, quando forem criados tabelas, listas, matrizes e etc, todas serão mostrada nesse local.

.. figure:: ./images/rstudio_ambiente.png
	:align: center
	:class: custom-img

Por fim vamos falar da seção de "administração" do nosso Rstudio, que se encontra na seção inferior esquerda. Por padrão ela está aberta na aba *Files* que irá mostrar arquivos do seu sistema.

Em seguida, a aba *Plots* é onde serão visualizados os gráficos plotados. Por exemplo, vamos plotar um histograma de 'x', que possue 100 números aleatórios. Digite no console o seguinte código e pressione Enter:

.. code-block:: r

	hist(x)

Agora você verá algo muito similar na aba *Plots*.

.. figure:: ./images/rstudio_plots.png
	:align: center
	:class: custom-img

A próxima aba é a *Packages* onde esta a lista de todos os pacotes instalados no seus sistema. Por último, a aba *Help* permite você ter acesso a várias ferramentas de ajuda e tutoriais. Na próxima seção vamos aprofundar sobre o que são pacotes e como utilizar as ajudas disponíveis.