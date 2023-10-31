# Funções

Aqui falaremos um pouco de funções em JavaScript. É possível criar funções com passagem de parâmetros, com retorno de um valor ou um conjunto de valores e até mesmo funções anônimas. Ainda, podemos fazer com que uma função seja utilizada como um módulo, que contém um trecho de código que se repete e, assim, pode ser acionado várias vezes num mesmo programa ou em diversos programas diferentes.

No que respeita aos módulos, o processo de modularização de programas é uma técnica de programação que consiste em dividir um programa em pequenos módulos, que podem ser desenvolvidos e testados de forma independente. Ainda, a modularização facilita a manutenção, pois quando uma função, que é utilizada em vários programas, precisa ser alterada, basta alterar o módulo correspondente, sem a necessidade de alterar todos os programas que utilizam a função. Em outras palavras, podemos dizer que uma função é um `subprograma` que pode ser chamado por um programa principal ou por outra função.

Um exemplo: Imagine que você precisa desenvolver um programa que coletará os dados de clientes, funcionários e estagiários. Todos esses cadastros coletarão o CPF da pessoa. Assim, você pode desenvolver uma única função para validação do CPF e utilizar essa função em todos os cadastros. Se, por acaso, a regra de validação do CPF mudar, você altera a função e todos os cadastros estarão atualizados.

Embora já utilizemos algumas funções, agora criaremos e manipularemos algumas funções. 

## Funções com passagem de parâmetros
Um exemplo de função que utilizamos é a função _alert()_. Essa função recebe um parâmetro, que é o texto que será exibido na caixa de diálogo. A função _alert()_ não retorna nenhum valor, apenas exibe o texto na caixa de diálogo.

> A função alert nos ajuda a unificar a exibição de mensagens para o usuário. Imagine se fosse necessário uma função diferente para cada mensagem que tivesse que ser exibida para o usuário. Assim, você apenas "chama" a função e passa o parâmetro para a função, que é a mensagem a ser exibida para o usuário.

```javascript
alert("Olá, mundo!");
```

```javascript
alert("Bom dia!");
```

Note que a sintaxe é a mesma para as duas chamadas da função, o que muda é o parâmetro passado para a função.

Vamos construir agora um primeiro exemplo, que tem como propósito indicar se o aluno está aprovado ou não. Para isso vamos criar uma função que recebe um parâmetro, que é a média do aluno. Se a média for maior ou igual a 6, o aluno está aprovado, caso contrário, o aluno está reprovado. [EXEMPLO01.HTML](exemplos/exemplo01.html)

```javascript
function situacaoAluno(media) {
    if (media >= 6) {
        alert("Aprovado!");
    } else {
        alert("Reprovado!");
    }
}
```

Para chamar a função, em qualquer lugar do código, a sintaxe será a seguinte:

```javascript
situacaoAluno(7);
```

Numa situação um pouco diferente, passando dois parâmetros para a função, é possível que seja validada a aprovação do aluno considerando a possibilidade de haverem diferentes médias para a aprovação. Digamos que em um curso a média para aprovação seja 7 e em outro curso a média para aprovação seja 6. Assim, podemos passar dois parâmetros para a função, que são a média do aluno e a média para aprovação. [EXEMPLO02.HTML](exemplos/exemplo02.html)

```javascript
function situacaoAluno(mediaAluno, mediaAprovacao) {
    if (mediaAluno >= mediaAprovacao) {
        alert("Aprovado!");
    } else {
        alert("Reprovado!");
    }
}
```

Portanto, para chamar a função, utilizando dois parâmetros, a sintaxe será da seguinte forma:

```javascript
situacaoAluno(6, 10);
```

Considere, então, que o programa perguntará ao aluno qual foi sua nota na prova e qual é a média para aprovação. Assim, o programa deve receber esses dois valores e passar para a função. Veja o exemplo: [EXEMPLO03.HTML](exemplos/exemplo03.html)

```javascript
    //Aqui, a função recebe dois parâmetros, que são a média do aluno e a média para aprovação
    function situacaoAluno(mediaAluno, mediaAprovacao) {
        if (mediaAluno >= mediaAprovacao) {
            alert("Aprovado!");
        } else {
            alert("Reprovado!");
        }
    }

    //Na linha abaixo, o programa pergunta ao aluno qual foi sua média anual obtida
    let mediaAluno = prompt("Qual foi a sua nota na prova?");
    //Na linha abaixo, o programa pergunta ao aluno qual é a média para aprovação
    let mediaAprovacao = prompt("Qual é a média para aprovação?");
    //Na linha abaixo, o programa chama a função, passando os dois parâmetros informados pelo aluno
    situacaoAluno(mediaAluno, mediaAprovacao);
```

> Existem os parâmetros e os argumentos da funçãio. Os parâmetros são, propriamente, os nomes das variáveis - neste caso, _mediaAluno_ e _mediaAprovacao_. Os argumentos são os valores atribuídos para esses parâmetros. Assim, quando chamamos a função, passando os valores 10 e 6, estamos passando os argumentos para os parâmetros _mediaAluno_ e _mediaAprovacao_.

## Funções com retorno de valores

Ao invés de as funções executarem uma ação, como é o caso da função _alert()_, é possível que as funções retornem um valor. Para isso, utilizamos a palavra reservada _return_ e, na sequência, o conteúdo que será retornado.

Utilizando o mesmo problema anterior, vamos criar uma função que recebe dois parâmetros, que são a média do aluno e a média para aprovação. A função deve retornar a mensagem "Aprovado" ou "Reprovado", dependendo da média do aluno. Veja o exemplo: [EXEMPLO04.html](exemplos/exemplo04.html)


```javascript
function situacaoAluno(mediaAluno, mediaAprovacao) {
    if (mediaAluno >= mediaAprovacao) {
        return "Aprovado";
    } else {
        return "Reprovado";
    }
}
let resposta = situacaoAluno(10, 6);
alert(resposta);
```

Note que a função _situacaoAluno()_ retorna um valor, que é a mensagem "Aprovado" ou "Reprovado". Assim, quando chamamos a função, passando os valores 10 e 6, a função retorna o valor "Aprovado" e esse valor é atribuído à variável _resposta_. Por fim, a variável _resposta_ é exibida na caixa de diálogo.

Ainda, uma função com passagem de parâmetros pode retornar mais de um valor. Para isso, basta separar os valores por vírgula. Veja o exemplo: [EXEMPLO05.HTML](exemplos/exemplo05.html)

```javascript
function situacaoAluno(mediaAluno, mediaAprovacao) {
    if (mediaAluno >= mediaAprovacao) {
        return ["Aprovado", mediaAluno];
    } else {
        return ["Reprovado", mediaAluno];
    }
}
let resposta = situacaoAluno(10, 6);
alert(`${resposta[0]}, ${resposta[1}`);
```

> **Alerta de spoiler**: mais adiante, veremos que é possível retornar mais de um valor utilizando objetos (_objetos em JavaScript ainda serão abordados na disciplina_).
> Veja o seguinte código em JavaScript, retornando um objeto. [EXEMPLO06.HTML](exemplos/exemplo06.html)

```javascript
function situacaoAluno(mediaAluno, mediaAprovacao) {
    if (mediaAluno >= mediaAprovacao) {
        return {situacao: "Aprovado", media: mediaAluno};
    } else {
        return {situacao: "Reprovado", media: mediaAluno};
    }
}
let resposta = situacaoAluno(10, 6);
alert(`${resposta.situacao} com média ${resposta.media}`);
```

> Um outro exemplo, retornando um array de objetos: [EXEMPLO07.HTML](exemplos/exemplo07.html)

```javascript
function dadosPessoa() {
    let pessoas = [
        {nome: "João", idade: 20},
        {nome: "Maria", idade: 30},
        {nome: "José", idade: 40},
        {nome: "Ana", idade: 50}
    ];
    return pessoas;
}
let resposta = dadosPessoa();
alert(`Nome: ${resposta[0].nome}, Idade: ${resposta[0].idade}`);
```

E, caso queira escrever na tela todos os dados de todas as pessoas, basta fazer um laço de repetição: [EXEMPLO08.HTML](exemplos/exemplo08.html)

```javascript
function dadosPessoa() {
    let pessoas = [
        { nome: "João", idade: 20 },
        { nome: "Maria", idade: 30 },
        { nome: "José", idade: 40 },
        { nome: "Ana", idade: 50 }
    ];
    return pessoas;
}
let resposta = dadosPessoa();
for (let i = 0; i < resposta.length; i++) {
    document.write(`Nome: ${resposta[i].nome}, Idade: ${resposta[i].idade}<br>`);
}
```

## Funções anônimas
As funções anônimas permitem definir uma função sem nome. Para isso, utilizamos a palavra reservada _function_ e, na sequência, os parâmetros da função e o corpo da função. Veja o exemplo: [EXEMPLO09.HTML](exemplos/exemplo09.html)

```javascript
let situacaoAluno = function(mediaAluno, mediaAprovacao) {
    if (mediaAluno >= mediaAprovacao) {
        return "Aprovado";
    } else {
        return "Reprovado";
    }
}
let resposta = situacaoAluno(10, 6);
alert(resposta);
```

No geral, as funções anônimas são usadas para a inserção de pequenos trechos de código. Por exemplo, imagine que você precisa criar um botão que, quando clicado, exibe uma mensagem na caixa de diálogo. Assim, você pode criar uma função anônima e atribuir essa função ao evento _onclick_ do botão. Veja o exemplo: [EXEMPLO10.HTML](exemplos/exemplo10.html)

```javascript
<button onclick="function() { alert('Olá, mundo!'); }">Clique aqui</button>
```

Um outro exemplo mais prático, considerando que desejamos mostrar o parcelamento de um produto a ser comprado em uma loja, sendo que o cliente pode escolher o número de parcelas, desde 1 até 10 parcelas. Assim, o programa deve receber o valor do produto e calcular o valor de cada parcela, para que o cliente escolha qual a melhor maneira de efetuar pagamento. Veja o exemplo: [EXEMPLO11.HTML](exemplos/exemplo11.html)

```javascript
    let valorProduto = Number(prompt("Qual é o valor do produto?"));
    let mensagem = "";
    let formasPagamento = function (valorProduto) {
        for (let i = 1; i <= 10; i++) {
            let valorParcela = valorProduto / i;
            mensagem += ("Em " + i + " parcelas, o valor de cada parcela é de R$ " + valorParcela.toFixed(2).replace(".", ",") + "<br>");
        }
        return mensagem;
    }
    let resultado = formasPagamento(valorProduto);
    document.write(resultado);
```

Note que a função anônima recebe um parâmetro, que é o valor do produto. A função calcula o valor de cada parcela e retorna uma mensagem, que é atribuída à variável _resultado_. Por fim, a variável _resultado_ é exibida na página.

## Funções Callbacks (Retorno de Chamada)
As funções callback são funções que são passadas como parâmetro para outra função. Veja o exemplo: [EXEMPLO12.HTML](exemplos/exemplo12.html)

```javascript
function soma(a, b) {
    return a + b;
}
function subtracao(a, b) {
    return a - b;
}
function multiplicacao(a, b) {
    return a * b;
}
function divisao(a, b) {
    return a / b;
}
function calculadora(a, b, operacao) {
    return operacao(a, b);
}
let resultado = calculadora(10, 5, soma);
alert(resultado);
```

Este é um exemplo simples, onde temos quatro funções, que são as operações matemáticas básicas. A função _calculadora()_ recebe três parâmetros, que são os dois valores e a operação matemática. A função _calculadora()_ retorna o resultado da operação matemática. Por fim, a função _calculadora()_ é chamada, passando os dois valores e a operação matemática. Note que a operação matemática é passada como parâmetro, que é uma função. Assim, a função _calculadora()_ chama a função passada como parâmetro, passando os dois valores. O resultado da operação matemática é atribuído à variável _resultado_ e, por fim, a variável _resultado_ é exibida na caixa de diálogo.

As funções callback são muito utilizadas em eventos de elementos HTML. Por exemplo, imagine que você precisa criar um botão que, quando clicado, exibe uma mensagem na caixa de diálogo. Assim, você pode criar uma função anônima e atribuir essa função ao evento _onclick_ do botão. Veja o exemplo: [EXEMPLO13.HTML](exemplos/exemplo13.html)

```javascript
<button onclick="function() { alert('Olá, mundo!'); }">Clique aqui</button>
```

Na verdade, as _Funções Callbacks_ foram disponibilizadas na versão mais recente do JavaScript, o ES6. Antes disso, era necessário utilizar as _Funções Anônimas_ para fazer o mesmo que as _Funções Callbacks_ fazem.

Vamos simular um outro exemplo. Considere a seguinte lista de números:
```javascript
let numeros = [1, 2, 4, 7, 5, 3, 6];
```
Digamos que você deseja obter todos os números ímpares que estão presentes no Array acima. Para tal, é possível usar a funçã `filter()`, que pertence ao objeto Array do JavaScript. Sem utilizar _callbacks_, o código seria o seguinte: [EXEMPLO14.HTML](exemplos/exemplo14.html)

```javascript
let numeros = [1, 2, 4, 7, 5, 3, 6];
function ehNumeroImpar(nro) {
    return nro % 2 != 0;
}
let numerosImpares = numeros.filter(ehNumeroImpar);
alert(numerosImpares);
```
Como anteriormente ao ES6 utilizavam-se as _Funções Anônimas_, o código acima poderia ser escrito da seguinte forma: [EXEMPLO15.HTML](exemplos/exemplo15.html)
```javascript
let numeros = [1, 2, 4, 7, 5, 3, 6];
let numerosImpares = numeros.filter(function(nro) {
    return nro % 2 != 0;
});
alert(numerosImpares);
```

Porém, com o advento do ES6, é possível utilizar as _Funções Callbacks_, que são funções que são passadas como parâmetro para outra função. Veja o exemplo: [EXEMPLO16.HTML](exemplos/exemplo16.html)
```javascript
let numeros = [1, 2, 4, 7, 5, 3, 6];
let numerosImpares = numeros.filter(nro => nro % 2 != 0);
alert(numerosImpares);
```


## Funções autoexecutáveis
As funções autoexecutáveis são funções que são executadas automaticamente, sem a necessidade de serem chamadas. Para isso, utilizamos a palavra reservada _function_ e, na sequência, os parâmetros da função e o corpo da função. Veja o exemplo: [EXEMPLO17.HTML](exemplos/exemplo17.html)

```javascript
(function() {
    alert("Olá, mundo!");
})();
```

Note que a função é definida entre parênteses e, na sequência, há dois parênteses. Isso indica que a função será executada automaticamente, sem a necessidade de ser chamada.

## Funções recursivas
As funções recursivas são funções que chamam a si mesmas. Para isso, utilizamos a palavra reservada _function_ e, na sequência, os parâmetros da função e o corpo da função. Veja o exemplo: [EXEMPLO18.HTML](exemplos/exemplo18.html)

```javascript
function fatorial(numero) {
    if (numero == 1) {
        return 1;
    } else {
        return numero * fatorial(numero - 1);
    }
}
let resultado = fatorial(5);
alert(resultado);
```

Note que a função _fatorial()_ recebe um parâmetro, que é o número a ser calculado o fatorial. A função verifica se o número é igual a 1. Se for, retorna 1. Caso contrário, retorna o número multiplicado pelo fatorial do número menos 1. Assim, a função chama a si mesma, passando o número menos 1. Esse processo se repete até que o número seja igual a 1. Por fim, o resultado do fatorial é atribuído à variável _resultado_ e, por fim, a variável _resultado_ é exibida na caixa de diálogo.

## Funções com parâmetros opcionais
As funções com parâmetros opcionais são funções que recebem parâmetros que não são obrigatórios. Para isso, utilizamos a palavra reservada _function_ e, na sequência, os parâmetros da função e o corpo da função. Veja o exemplo: [EXEMPLO19.HTML](exemplos/exemplo19.html)


```javascript
function situacaoAluno(mediaAluno, mediaAprovacao = 6) {
    if (mediaAluno >= mediaAprovacao) {
        return "Aprovado";
    } else {
        return "Reprovado";
    }
}
let resposta = situacaoAluno(10);
alert(resposta);
```

Note que a função _situacaoAluno()_ recebe dois parâmetros, que são a média do aluno e a média para aprovação. O segundo parâmetro, que é a média para aprovação, é opcional. Assim, se o segundo parâmetro não for passado, a média para aprovação será 6. Por fim, a variável _resposta_ é exibida na caixa de diálogo.

## Funções com parâmetros variáveis
As funções com parâmetros variáveis são funções que recebem uma quantidade variável de parâmetros. Para isso, utilizamos a palavra reservada _function_ e, na sequência, os parâmetros da função e o corpo da função. Veja o exemplo: [EXEMPLO20.HTML](exemplos/exemplo20.html)

```javascript
function soma() {
    let resultado = 0;
    for (let i = 0; i < arguments.length; i++) {
        resultado += arguments[i];
    }
    return resultado;
}
let resultado = soma(10, 20, 30, 40, 50);
alert(resultado);
```

Note que a função _soma()_ não recebe nenhum parâmetro. Porém, dentro da função, é utilizado o objeto _arguments_, que é um objeto que contém todos os parâmetros passados para a função. Assim, a função _soma()_ percorre todos os parâmetros passados para a função e soma todos os valores. Por fim, o resultado da soma é atribuído à variável _resultado_ e, por fim, a variável _resultado_ é exibida na caixa de diálogo.

## Funções com parâmetros nomeados
As funções com parâmetros nomeados são funções que recebem parâmetros nomeados. Para isso, utilizamos a palavra reservada _function_ e, na sequência, os parâmetros da função e o corpo da função. Veja o exemplo: [EXEMPLO21.HTML](exemplos/exemplo21.html)

```javascript
function situacaoAluno({ mediaAluno, mediaAprovacao }) {
    if (mediaAluno >= mediaAprovacao) {
        return "Aprovado";
    } else {
        return "Reprovado";
    }
}
let resposta = situacaoAluno({ mediaAluno: 10, mediaAprovacao: 6 });
alert(resposta);
```

Note que a função _situacaoAluno()_ recebe um parâmetro, que é um objeto com os parâmetros _mediaAluno_ e _mediaAprovacao_. Assim, ao chamar a função, passamos um objeto com os parâmetros _mediaAluno_ e _mediaAprovacao_. Por fim, a variável _resposta_ é exibida na caixa de diálogo.

## Funções com parâmetros nomeados e opcionais
As funções com parâmetros nomeados e opcionais são funções que recebem parâmetros nomeados e opcionais. Para isso, utilizamos a palavra reservada _function_ e, na sequência, os parâmetros da função e o corpo da função. Veja o exemplo: [EXEMPLO22.HTML](exemplos/exemplo22.html)

```javascript
function situacaoAluno({ mediaAluno, mediaAprovacao = 6 }) {
    if (mediaAluno >= mediaAprovacao) {
        return "Aprovado";
    } else {
        return "Reprovado";
    }
}
let resposta = situacaoAluno({ mediaAluno: 10 });
alert(resposta);
```

Note que a função _situacaoAluno()_ recebe um parâmetro, que é um objeto com os parâmetros _mediaAluno_ e _mediaAprovacao_. O segundo parâmetro, que é a média para aprovação, é opcional. Assim, se o segundo parâmetro não for passado, a média para aprovação será 6. Por fim, a variável _resposta_ é exibida na caixa de diálogo.

## Funções com parâmetros nomeados e variáveis
As funções com parâmetros nomeados e variáveis são funções que recebem parâmetros nomeados e variáveis. Para isso, utilizamos a palavra reservada _function_ e, na sequência, os parâmetros da função e o corpo da função. Veja o exemplo: [EXEMPLO23.HTML](exemplos/exemplo23.html)

```javascript
function soma({ a, b, ...resto }) {
    let resultado = 0;
    for (let i = 0; i < arguments.length; i++) {
        resultado += arguments[i];
    }
    return resultado;
}
let resultado = soma({ a: 10, b: 20, c: 30, d: 40, e: 50 });
alert(resultado);
```

Note que a função _soma()_ recebe um parâmetro, que é um objeto com os parâmetros _a_ e _b_. O parâmetro _resto_ é um parâmetro variável, que recebe todos os parâmetros passados para a função. Assim, a função _soma()_ percorre todos os parâmetros passados para a função e soma todos os valores. Por fim, o resultado da soma é atribuído à variável _resultado_ e, por fim, a variável _resultado_ é exibida na caixa de diálogo.


##
**`Algumas funções nativas do JavaScript que valem ser mencionadas aqui, quais podem ser úteis em algum momento da vida do programador:`**

>Todas as funções abaixo possuem exemplos disponíveis no arquivo [`88funcoes.html`](88funcoes.html). Você pode acessar o arquivo [clicando aqui](88funcoes.html).

1. **alert()**: exibe uma mensagem na caixa de diálogo;
2. **confirm()**: exibe uma mensagem na caixa de diálogo, com as opções "OK" e "Cancelar";
3. **prompt()**: exibe uma mensagem na caixa de diálogo, com um campo para entrada de dados;
4. **Number()**: converte o valor informado para o tipo numérico;
5. **parseInt()**: converte o valor informado para o tipo numérico inteiro;
6. **parseFloat()**: converte o valor informado para o tipo numérico decimal;
7. **toFixed()**: formata o valor numérico, definindo a quantidade de casas decimais;
8. **replace()**: substitui um caractere por outro caractere;
9. **length**: retorna a quantidade de caracteres de uma string;
10. **toUpperCase()**: converte todos os caracteres de uma string para maiúsculo;
11. **toLowerCase()**: converte todos os caracteres de uma string para minúsculo;
12. **trim()**: remove os espaços em branco no início e no final de uma string;
13. **split()**: divide uma string em um array de strings, de acordo com o caractere informado;
14. **join()**: junta os elementos de um array, separando-os pelo caractere informado;
15. **sort()**: ordena os elementos de um array;
16. **reverse()**: inverte a ordem dos elementos de um array;
17. **push()**: adiciona um elemento no final de um array;
18. **pop()**: remove o último elemento de um array;
19. **shift()**: remove o primeiro elemento de um array;
20. **unshift()**: adiciona um elemento no início de um array;
21. **slice()**: retorna um novo array, de acordo com o início e o fim informados;
22. **splice()**: remove ou substitui elementos de um array, de acordo com o início e a quantidade informados;
23. **concat()**: concatena dois ou mais arrays;
24. **indexOf()**: retorna a posição de um elemento de um array;
25. **lastIndexOf()**: retorna a última posição de um elemento de um array;
26. **includes()**: verifica se um elemento existe em um array;
27. **filter()**: retorna um novo array, de acordo com a condição informada;
28. **map()**: retorna um novo array, de acordo com a condição informada;
29. **reduce()**: retorna um novo array, de acordo com a condição informada;
30. **forEach()**: executa uma função para cada elemento de um array;
31. **some()**: verifica se pelo menos um elemento de um array atende à condição informada;
32. **every()**: verifica se todos os elementos de um array atendem à condição informada;
33. **find()**: retorna o primeiro elemento de um array que atende à condição informada;
34. **findIndex()**: retorna a posição do primeiro elemento de um array que atende à condição informada;
35. **Math.random()**: retorna um número aleatório entre 0 e 1;
36. **Math.round()**: arredonda um número para o inteiro mais próximo;
37. **Math.ceil()**: arredonda um número para o inteiro mais próximo, sempre para cima;
38. **Math.floor()**: arredonda um número para o inteiro mais próximo, sempre para baixo;
39. **Math.pow()**: retorna a potência de um número;
40. **Math.sqrt()**: retorna a raiz quadrada de um número;
41. **Math.abs()**: retorna o valor absoluto de um número;
42. **Math.min()**: retorna o menor valor de um conjunto de números;
43. **Math.max()**: retorna o maior valor de um conjunto de números;
44. **Math.PI**: retorna o valor de PI;
45. **Math.E**: retorna o valor de E;
46. **Date()**: retorna a data e a hora atual;
47. **getFullYear()**: retorna o ano atual;
48. **getMonth()**: retorna o mês atual;
49. **getDate()**: retorna o dia atual;
50. **getDay()**: retorna o dia da semana atual;
51. **getHours()**: retorna a hora atual;
52. **getMinutes()**: retorna o minuto atual;
53. **getSeconds()**: retorna o segundo atual;
54. **getMilliseconds()**: retorna o milissegundo atual;
55. **getTime()**: retorna o timestamp atual;
56. **setFullYear()**: altera o ano;
57. **setMonth()**: altera o mês;
58. **setDate()**: altera o dia;
59. **setHours()**: altera a hora;
60. **setMinutes()**: altera o minuto;
61. **setSeconds()**: altera o segundo;
62. **setMilliseconds()**: altera o milissegundo;
63. **setTimeout()**: executa uma função após um determinado tempo;
64. **setInterval()**: executa uma função em intervalos de tempo regulares;
65. **clearTimeout()**: cancela a execução de uma função agendada com o setTimeout();
66. **clearInterval()**: cancela a execução de uma função agendada com o setInterval().
67. **addEventListener()**: adiciona um evento a um elemento;
68. **removeEventListener()**: remove um evento de um elemento;
69. **stopPropagation()**: interrompe a propagação de um evento;
70. **preventDefault()**: cancela o comportamento padrão de um evento;
71. **target**: retorna o elemento que acionou o evento;
72. **type**: retorna o tipo de evento;
73. **keyCode**: retorna o código da tecla pressionada;
74. **which**: retorna o código da tecla pressionada;
75. **charCode**: retorna o código da tecla pressionada;
76. **pageX**: retorna a posição do eixo X do mouse;
77. **pageY**: retorna a posição do eixo Y do mouse;
78. **offsetX**: retorna a posição do eixo X do mouse, em relação ao elemento;
79. **offsetY**: retorna a posição do eixo Y do mouse, em relação ao elemento;
80. **clientX**: retorna a posição do eixo X do mouse, em relação à janela;
81. **clientY**: retorna a posição do eixo Y do mouse, em relação à janela;
82. **screenX**: retorna a posição do eixo X do mouse, em relação à tela;
83. **screenY**: retorna a posição do eixo Y do mouse, em relação à tela;
84. **altKey**: retorna true se a tecla ALT foi pressionada;
85. **ctrlKey**: retorna true se a tecla CTRL foi pressionada;
86. **shiftKey**: retorna true se a tecla SHIFT foi pressionada;
87. **button**: retorna o botão do mouse pressionado;
88. **buttons**: retorna os botões do mouse pressionados;