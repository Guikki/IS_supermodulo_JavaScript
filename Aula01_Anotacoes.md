Variáveis

A Computação tem, basicamente, duas funções: fazer cálculos e armazenar informações.

A palavra computador vem de “computar”, que é contar, e é basicamente isso que um computador faz: cálculos.

Seja em uma pesquisa científica, uma troca de mensagens no Whatsapp ou na exibição de um site da internet, os computadores precisam fazer uma série de operações binárias em seu hardware, para resultar em pixels na sua tela, onde você vê o resultado acontecer.

Porém, só fazer essas operações binárias não serve de muita coisa, se os resultados desses cálculos não forem armazenados.

Imagine que a cada vez que você desliga seu computador ou celular, todas suas informações sejam apagadas: textos, vídeos, fotos, arquivos etc. Isso é inconcebível, o computador é usado também para armazenar informações.

O ato de armazenar dados, de uma maneira temporária (até desligar o computador ou fechar um programa) ou permanente (gravar dados em um HD ou servidor), é tão essencial e importante que isso é feito de maneira bem frequente em programação, através de variáveis.

VARIÁVEIS EM JAVASCRIPT


Certamente você já se deparou com um jogo feito em JavaScript, e talvez nem tenha percebido.

Você joga uma partida, e marca 100 pontos. Depois, joga novamente e marca 200, então esse passa a ser seu novo recorde.

Mas como o jogo sabe que 200 é seu novo recorde? Para saber isso, ele teria que saber que sua pontuação anterior era menor que 200.

Ou seja, o número “100” foi armazenado pelo JavaScript em algum lugar, então quando você jogou de novo, sua nova pontuação foi comparada com essa anterior, para saber que seu recorde foi quebrado.

Você também já deve ter entrado em algum site que pedia seu nome, você digitava e depois ele exibia uma mensagem “Olá, Fulano”. Ou seja, o Javascript guardou seu nome em algum lugar, para exibir no futuro.

Uma variável foi usada para armazenar o texto “Fulano”, que você escreveu. E depois, o JavaScript foi nessa variável, pegou as informações que tinha nela e exibiu para você o “Olá, Fulano”.

As variáveis são usadas para armazenar valores em JavaScript. Existem três palavras-chave comuns para declarar variáveis: var, let e const.


Var:
Declarar uma variável é reservar memória para armazenar uma informação.

Essa informação vai ficar associada a essa variável, e para podermos fazer isso temos que usar um comando especial, que diga ao JavaScript “Ei, essa é uma variável! Guarde ela!”.

Esse comando é dado por uma palavra chamada var. Assim, para declararmos uma variável, fazemos: var nome;

A palavra-chave var é usada para declarar variáveis tradicionais em JavaScript. Elas são criadas no escopo global ou de função e podem ser reatribuídas posteriormente. Elas também têm um comportamento de "hoisting", o que significa que elas podem ser acessadas antes de serem declaradas.

exemplo:




Como declarar mais de uma variável em uma linha

Você também pode definir essas três variáveis numa mesma linha, basta separar cada nome por uma vírgula:

var dia, mes, ano;

Uma outra maneira de declarar variáveis, é da seguinte maneira:
var dia,      mes,      ano;

Ao declarar variáveis dessa maneira, apenas estamos reservando um espaço em memória, é como se disséssemos “Ei, JavaScript, reserve espaço para essas variáveis, depois vamos usar elas!”

Let:

A palavra-chave let é usada para declarar variáveis de escopo de bloco. 

Elas são criadas no escopo de bloco em que são declaradas e não podem ser acessadas antes de serem declaradas. Elas também podem ser reatribuídas posteriormente.

Mas o que é Escopo?

Em poucas palavras, escopo é a propriedade que determina onde uma variável pode ser utilizada dentro de um programa, por exemplo, se você declara uma variável dentro de uma função, só aquela função consegue utilizar a variável, e SE você declara uma variável fora de uma função, ela pode ser acessada de qualquer parte daquele mesmo script, pois ela foi declarada globalmente. 

No Javascript existem 3 tipos de escopos, o global, local e de bloco. Vamos ver em detalhes como cada um deles funciona para var e let a seguir.

Escopo é a acessibilidade de objetos, variáveis e funções em diferentes partes do código.

Em outras palavras, o que determina quais são os dados que podem ser acessados em uma determinada parte do código é o escopo. Imagine que escopo é uma caixa e tudo que for criado nessa caixa pode ser acessado por qualquer objeto dentro da mesma.

Escopo global

Quando você declara uma variável fora de qualquer função, seja ela var ou let, ela tem o escopo global, pois qualquer função no script consegue utilizar esta variável.

Escopo Local

Uma variável é local quando ela é declarada dentro de alguma função, pois isso significa que apenas aquela função consegue enxergá-la. 

As demais funções do script não conseguem utilizá-la, pois a mesma foi declarada dentro de uma função específica. Neste ponto de vista, podemos dizer que o escopo local é completamente diferente do escopo global. 

Escopo de Bloco

E é aqui o grande pulo do gato da diferença entre var e let. O escopo de bloco. Primeiro para entender como esse escopo funciona, precisamos entender o que é um bloco na linguagem Javascript.

Podemos dizer que um bloco é tudo aquilo em um código que está entre chaves ({ }), ou seja, estruturas condicionais, estruturas de repetição, entre outras entidades que trabalham com blocos. 

Então, em resumo, uma variável com escopo de bloco, é uma variável que foi declarada dentro de um determinado bloco, e apenas pode ser manipulada dentro daquele bloco, e nenhuma outra parte do código pode manipulá-la. Dentre todos os tipos de escopo este é o mais restrito.

Este tipo de escopo só funciona com variáveis declaradas com a palavra chave let e esta é a grande diferença entre let e var.



Let permite que você declare variáveis limitando seu escopo no bloco, instrução, ou em uma expressão na qual ela é usada. Isso é inverso da keyword var, que define uma variável globalmente ou no escopo inteiro de uma função, independentemente do escopo de bloco.

"independentemente do escopo de bloco", na verdade, significa dizer que variáveis declaradas dentro de blocos internos da função, por exemplo, são vinculadas no escopo da função, não no bloco no qual elas são declaradas. 

Se isso parece confuso - e realmente é -, apenas entenda que, ao contrário do que se poderia supor, em JavaScript blocos não possuem escopo como em outras linguagens, somente funções têm! Isso quer dizer que mesmo uma variável definida com a keyword var dentro de um bloco de instrução if, será visível no resto inteiro da função.

Exemplo:



O Mesmo não se aplica quando você declara uma variável com var, pois o escopo de bloco não existe na palavra reservada var. 

Const:

A palavra-chave const é usada para declarar variáveis constantes. Elas são criadas no escopo de bloco em que são declaradas e não podem ser acessadas antes de serem declaradas. Elas não podem ser reatribuídas após a sua inicialização.

Conclusão - Variáveis:

Em resumo, as variáveis são usadas para armazenar valores em JavaScript. 
Existem três palavras-chave comuns para declarar variáveis: var, let e const. Var é usada para declarar variáveis tradicionais e tem um comportamento de hoisting, let é usada para declarar variáveis de escopo de bloco e pode ser reatribuída, e const é usada para declarar variáveis constantes e não pode ser reatribuída.
