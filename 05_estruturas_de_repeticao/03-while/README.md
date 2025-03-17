### [**Voltar para o Início**](../../README.md)

#### [**Página Anterior**](../02-forControle/README.md)

***Requisitos para estar aqui:***
- Ter finalizado a Lista de Exercícios sobre a Estrutura de Repetição _For com Variável de Controle_!
- Caso não tenha feito, [**CLIQUE AQUI**.](../02-forControle/listaExercicios_01/README.md)

# Repetição com variável de controle
## Laços de repetição com While

O laço de repetição **while** é um laço de repetição com variável de controle. Isso significa que, para que o laço seja executado, é necessário que uma condição seja verdadeira. Caso a condição seja falsa, o laço não será executado.

A sintaxe do laço **while** é a seguinte:

```javascript
while (condicao) {
    // código a ser executado
}
```

Uma outra sintaxe, ainda utilizando o conceito do _faça enquanto_ (do while), é a seguinte:

```javascript
do {
    // código a ser executado
} while (condicao);
```

Vamos exemplificar com uma condição estabelecida, ainda com pouca complexidade, para que possamos entender o funcionamento do laço de repetição **while**.  Veja o exemplo abaixo:

```javascript
let contador = 0;
while (contador < 5) {
    console.log(contador);
    contador++;
}
```

O código acima irá imprimir no console os números de 0 a 4. Isso acontece porque a variável `contador` é inicializada com o valor 0. A condição do laço é `contador < 5`, ou seja, enquanto o valor da variável `contador` for menor que 5, o laço será executado. A cada execução do laço, o valor da variável `contador` é incrementado em 1. Quando o valor da variável `contador` for igual a 5, a condição do laço será falsa e o laço será encerrado.

O laço **while** é muito útil quando não sabemos quantas vezes o laço será executado. Por exemplo, se quisermos que o usuário digite um número entre 1 e 10, podemos utilizar um laço **while** para garantir que o usuário digite um número válido. Veja o exemplo abaixo:

```javascript
let numero = Number(prompt("Digite um número entre 1 e 10:"));
while (numero < 1 || numero > 10) {
    numero = Number(prompt("Digite um número entre 1 e 10:"));
}
```

O código acima irá solicitar que o usuário digite um número entre 1 e 10. Caso o usuário digite um número menor que 1 ou maior que 10, o laço será executado novamente, solicitando que o usuário digite um número válido. O laço será executado até que o usuário digite um número válido.

### ***Qual a diferença?***
#### ***While e Do While***
> O While irá executar a repetição apenas caso a condição seja verdadeira. Já o Do While irá executar a repetição pelo menos uma vez, independente da condição ser verdadeira ou falsa.

<u>Considere a seguinte situação:</u>

O usuário, previamente, já inseriu um dado para uma variável que será validada no laço de repetição. Neste caso, o mais indicado é o `while`, pois a condição será testada antes de executar o bloco de código.

Por outro lado, se o usuário ainda não inseriu nenhum dado, o mais indicado é o `do while`, pois o bloco de código será executado pelo menos uma vez, independente da condição ser verdadeira ou falsa.

Veja a diferença na prática:

```javascript
let genero = "F";
while (genero != "F" && genero != "M") {
    genero = prompt(`Informe o gênero (M/F): `).toUpperCase();
}
```
> Neste exemplo, o `while` será executado apenas se a condição não for atendida, ou seja, se o valor previamente atribuído para a let `genero` não for "F" ou "M".

No exemplo seguinte, não foi atribuído nenhum valor ainda para a let `genero`. Assim, o `do while` será executado pelo menos uma vez, pois será a primeira vez que será atribuído valor para a let `genero` e, assim, o `do while` se encarregará de validar se o valor inserido atende a condição estabelecida.

```javascript
let genero = "";
do {
    genero = prompt(`Informe o gênero (M/F): `).toUpperCase();
} while (genero != "F" && genero != "M");
```

#### **ATENÇÃO!**

> O que não pode ocorrer é o seguinte código:
> ```javascript
> let genero = "F";
> do {
>     genero = prompt(`Informe o gênero (M/F): `).toUpperCase();
> } while (genero != "F" && genero != "M");
> ```
> *Este código está incorreto, pois já há um valor atribuído para a let `genero` e, mesmo assim, o `do while` será executado, desconsiderando o valor já atribuído para a let `genero`.*

Todo o conteúdo que já trabalhamos até aqui na disciplina de Programação será aplicado ao trabalharmos com estruturas de repetição.
Os temas que aparecerão aqui repetidamente são:
* if... else (e if... else aninhado)
* operador ternário (e operador ternário aninhado)
* switch... case
* variáveis e operadores (muitas operações matemáticas!)
* e, principalmente, [**Arrays!!**](../../04_arrays/README.md)

#
## BÓRA PRATICAR?

Colocando em prática o conhecimento apresentado sobre Arrays, vamos para uma pequena lista de exercícios.

## [**<u>Clique aqui para acessar a Lista de Exercícios</u>**](listaExercicios_01/README.md)


##### Alguns links para estudos complementares

* [Developer.mozilla - for](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/for)
* [W3Schools - JavaScript For Loop](https://www.w3schools.com/js/js_loop_for.asp)
* [DevMedia - For em Javascript - Dica](https://www.devmedia.com.br/for-em-javascript-dica/28554)

##### Vídeos de apoio
* [Código Fonte TV](https://youtu.be/NfHVPEzo5Ik)
* [Brazilian Dev](https://www.youtube.com/watch?v=HJcZKxd-Uas)

##### Dúvidas da comunidade sobre ***for***
* [Stack Overflow - Loop JavaScript for (...)](https://pt.stackoverflow.com/questions/403105/loop-javascript-for)