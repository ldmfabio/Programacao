### [**Voltar para o Início**](../README.md)

#### [**Página Anterior**](../03_estruturas_de_decisao/03_03_switch_case/README.md)

***Requisitos para estar aqui:***
- Ter compreendido as Estruturas de Decisão IF...Else, Operador Ternário e Switch...Case!
- Caso ainda tenha alguma dúvida sobre alguma Estrutura de Decisão, clique no link correspondente:
  - [**IF...ELSE**.](../03_estruturas_de_decisao/03_01_if_else/README.md)
  - [**Operador Ternário**.](../03_estruturas_de_decisao/03_02_operador_ternario/README.md)
  - [**Switch...Case**.](../03_estruturas_de_decisao/03_03_switch_case/README.md)


# Arrays

Os arrays são estruturas que nos permitem armazenar uma lista de dados na memória do computador.
**Exemplos:** Lista de compras, alunos de uma turma, etc.

Para recuperar os itens de uma lista, utilizamos os arrays, indicando, numericamente, qual a posição do item que desejamos recuperar.

*Importante: Lembre que a primeira posição da lista corresponde com o número **0**, conforme representado na tabela abaixo .*

| Posição | Produto |
| :---: | :--- |
| 0 | Acerola |
| 1 | Banana |
| 2 | Laranja |
| 3 | Melancia |

***Guarde esta tabela como referência para os exemplos seguintes.***

Para armazenar os dados descritos acima em um array, usando JavaScript (JS), é necessário o seguinte código:
```javascript
const listaCompras = ["Acerola", "Banana", "Laranja", "Melancia"];
```
Para recuperar o conteúdo da primeira posição da lista, é necessário o seguinte código:
```javascript
listaCompras[0];
```
O conteúdo retornado será **"Acerola"**.

Já para recuperar o conteúdo da segunda posição da lista, o código será:
```javascript
listaCompras[1];
```
O conteúdo retornado será, portanto, **"Banana"**.

## Métodos para manipulação de Arrays
| Método | Utilidade |
| :--- | :--- |
| push() | Adiciona um elemento ao final do array. |
| pop() | Remove o último elemento ao final do array. |
| shift() | Remove o primeiro elemento do array e desloca os seguintes para cima. |
| unshift() | Adiciona um elemento no início do array e desloca os elementos para uma posição abaixo. |

Portanto, o código para adicionar um item (tanto ao fim - *push()* - quanto no início - *unshift()* - do array), será, respectivamente:
```javascript
listaCompras.push("Melão");
listaCompras.unshift("Abacaxi");
```

Já para remover um item (tanto ao fim - *pop()* - quanto no início - *shift()* - do array), será, respectivamente:
```javascript
listaCompras.pop();
listaCompras.shift();
```

Podemos também atribuir o valor de uma posição do array para uma const/let/var, usando o seguinte comando:
```javascript
const primeiroItem = listaCompras[0];
```
Considerando os itens descritos na Tabela, o conteúdo da const primeiroItem será **"Acerola"**.

Também existem alguns outros métodos que podem ser utilizados, tais quais:
| Método | Utilidade |
| :--- | :--- |
| splice() | Possibilita *emendar* o array. Utilizam-se parâmetros junto do método. |
| slice() | Tem por função *fatiar* o array. Também são necessários parâmetros para sua utilização. |

Imagine os seguintes exemplos:

* *const* **listaCompras** = ["Acerola", "Banana", "Laranja", "Melancia"];
* *const* **itensFim** = listaCompras.slice(-2);
  * Armazenará os dois últimos itens: **itensFim** terá os itens ["Laranja", "Melancia"]
* *const* **itensInicio** = listaCompras.slice(0, -1);
  * Armazenará todos os itens, com exceção do último: **itensInicio** terá os itens ["Acerola", "Banana", "Laranja"]
* *const* **itemRemovido** = listaCompras.splice(2, 1);
  * A partir do terceiro item da lista (correspondente com o número 2 do método splice), retirará um item (correspondente com o número 1 do método splice). Portanto, **itemRemovido** terá o conteúdo ["Laranja"], enquanto que o array original, **listaCompras**, será atualizado para ["Acerola", "Banana", "Melancia"];


#### Explorando o método _splice()_

Podemos usar dois ou três parâmetros no método splice(). Consideremos novamente a nossa lista de compras:

* *const* **listaCompras** = ["Acerola", "Banana", "Laranja", "Melancia"];

* Um parâmetro:

```javascript
listaCompras.splice(2);
```

Com o método acima, o resultado da lista de compras será:

**["Acerola", "Banana"]**

Afinal, o splice(2) fará com que todos os elementos à partir da posição 2 sejam removidos.

* Dois parâmetros:

Considere que a lista de compras voltou a ter o conteúdo original:

```javascript
listaCompras = ["Acerola", "Banana", "Laranja", "Melancia"];
```
E então o código abaixo será executado:

```javascript
listaCompras.splice(2, 1);
```

O resultado da lista de compras será:

**["Acerola", "Banana", "Melancia"]**

Isso se deve ao fato de que, à partir da posição 2, foi removido 1 elemento, que corresponde, respectivamente ao primeiro parâmetro e ao segundo parâmetro da função **splice(2, 1)**. O elemento removido foi o "Laranja", pois estava na segunda posição (posição 2 - primeiro parâmetro da função). Foi removido apenas um elemento pois o segundo parâmetro indicou exatamente isso (número 1).

* Tres parâmetros:

Considere novamente que a lista de compras voltou a ter o conteúdo original:

```javascript
listaCompras = ["Acerola", "Banana", "Laranja", "Melancia"];
```
E então o código abaixo será executado:

```javascript
listaCompras.splice(2, 1, "Abacaxi");
```

O resultado da lista de compras será:

**["Acerola", "Banana", "Abacaxi", "Melancia"]**

Com três parâmetros, a lógica é a seguinte:

* Primeiro parâmetro: indica a posição do array que será afetada;
* Segundo parâmetro: poderá ser 0 ou 1. Neste caso foi 1, que significa que será **ALTERADO** o item da posição 2, especificada no primeiro parâmetro. Ou seja, o item "Laranja".
* Terceiro parâmetro: indica o item que será inserido na posição indicada no primeiro parâmetro. Neste caso, foi inserido o item "Abacaxi".

O resultado da lista de compras será:

**["Acerola", "Banana", "Abacaxi", "Melancia"]**

Ao invés do número 1, colocado como segundo parâmetro, poderia ser então utilizado o número **0**. Sendo assim, ao invés de substituir um valor por outro, ao utilizar o **0** como parâmetro, será adicionado um novo item na posição indicada no primeiro parâmetro. 

Considerando que a instrução é a mesma:

```javascript
listaCompras.splice(2, 0, "Abacaxi");
```

O resultado da lista de compras será:

**["Acerola", "Banana", "Abacaxi", "Laranja", "Melancia"]**

Portanto, ao invés de substituir o item da posição 2 pelo item "Abacaxi", o item "Abacaxi" será adicionado na posição 2, fazendo com que os elementos após a posição 2 sejam empurrados para a posição seguinte.

Para ordenar os elementos do array, existem métodos que ordenam os itens de forma crescente e de forma decrescente.

***Após ordenar, não será possível retornar para a sequência anterior.*** 

| Método | Utilidade |
| :--- | :--- |
| sort() | Ordena os itens de forma crescente - do menor para o maior: **A->Z**. |
| reverse() | Ordena os itens de forma descrescente - do maior para o menor:  **Z->A**. |

Entretanto, para ordenar um Array de números, não utiliza-se apenas o método sort() ou reverse().

```javascript
const numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
numeros.sort();
```

O resultado será o seguinte:

**[1, 10, 2, 3, 4, 5, 6, 7, 8, 9]**

Portanto, para ordenar um Array de números, utiliza-se o seguinte comando:
```javascript
numeros.sort(function(a, b) {
    return a - b;
});
```
O parâmetro *a* representa o primeiro elemento e o parâmetro *b* representa o segundo elemento. O comando acima irá ordenar o array de números de forma crescente.

A função para ordenar também poderá ser escrita assim:
```javascript
numeros.sort((a, b) => a - b);
```

Isso para ordenar de forma **CRESCENTE**!

Caso deseje ordenar de forma **DECRESCENTE**, utiliza-se o seguinte comando:
```javascript
numeros.sort((a, b) => b - a);
```

## Propriedades dos Arrays

Existem propriedades que podem ser acessadas após a criação dos arrays. Uma das mais importantes é a propriedade que retorna a quantidade de elementos do array (tamanho), que é a propriedade *length*.
Ou seja, considerando o nosso array:

```javascript
const listaCompras = ["Acerola", "Banana", "Laranja", "Melancia"];
```

Ao executarmos o comando:
```javascript
listaCompras.length;
```
O conteúdo que retornará será **4**, que corresponde aos elementos que contém - que são as quatro frutas.

Alguns comandos úteis para retornar os dados do array em uma string (texto), são os:
```javascript
listaCompras.join();
```
O retorno será o seguinte:

**Acerola,Banana,Laranja,Melancia**

É possível passarmos um parâmetro ao usar o método **join()**, como no exemplo abaixo:
```javascript
listaCompras.join(" - ");
```
Ou seja, adicionamos ***espaço + hífen + espaço*** entre cada elemento do array para formar a string/texto de retorno, que será:
**Acerola - Banana - Laranja - Melancia**

*Também há o método toString() - listaCompras.toString() - porém não há possibilidade de customizar o retorno, estando sempre os itens separados por vírgula (Acerola,Banana,Laranja,Melancia).*

### Soletrando
Você sabia que também dá para soletrar um texto usando JS?

Existe o método Array.from(texto) que separa as letras de uma string. Veja o código abaixo:
```javascript
Array.from("Soletrando");
```
Ao executar esta instrução, o retorno será:

**["S", "o", "l", "e", "t", "r", "a", "n", "d", "o"]**

Ou seja, ele cria um array contendo todas as letras do parâmetro enviado para o método **from()**;

## Outros métodos relevantes

### ***concat()***

Imagine os dois arrays abaixo:
* *const* **frutas**  = ["Maçã", "Laranja", "Banana"];
* *const* **vegetais** = ["Tomate", "Cenoura", "Cebola"];

Para unir o conteúdo dos dois em apenas um array, é possível usar o método concat(), conforme descrito abaixo:
```javascript
const listaGeral = frutas.concat(vegetais);
```
O resultado será um array contendo todos os elementos dos dois arrays, sendo que nas primeiras posições estarão os elementos do array frutas. O conteúdo do array **listaGeral** será:

**["Maçã", "Laranja", "Banana", "Tomate", "Cenoura", "Cebola"];**

### ***indexOf()***
O método indexOf() retorna a primeira posição do caractere indicado no parâmetro. Considere o exemplo abaixo:
```javascript
const fruta = "banana";
const primeiraLetraA = fruta.indexOf("a");
alert(primeiraLetraA);
```
Assim, o valor que deverá ter na *const* **primeiraLetraA** será **1**.

Porém, para o usuário saber exatamente a posição, temos que considerar o fato de que o array inicia na posição 0. Portanto, o valor que deverá ser apresentado para o usuário, pensando na sua melhor compreensão, deverá ser acrescido com um valor. Ou seja, no caso acima, o valor que deverá ser apresentado para o usuário deverá ser **1 + 1 = 2**. O código deverá ficar da seguinte forma:
```javascript
const fruta = "banana";
const primeiraLetraA = fruta.indexOf("a") + 1;
alert(primeiraLetraA);
```
Assim, o valor que deverá ter na *const* **primeiraLetraA** sera **2**.

### ***lastIndexOf()***
Assim como o método indexOf(), aqui adiciona-se a palavra *last*. Ou seja, retornará a última posição do caractere indicado no parâmetro para a utilização deste método. Considere o exemplo abaixo:
```javascript
const fruta = "banana";
const ultimaLetraA = fruta.lastIndexOf("a");
```
Assim, o valor que deverá ter na *const* **ultimaLetraA** será **5**.

Porém, da mesma forma como no método indexOf(), o valor que retornará será a posição do Array, que começa na posição **0**. Portanto, pensando na melhor compreensão do usuário, sempre será acrescido com um valor. Ou seja, no caso acima, o valor que deverá ser apresentado para o usuário deverá ser **5 + 1 = 6**. O código deverá ficar da seguinte forma:
```javascript
const fruta = "banana";
const ultimaLetraA = fruta.lastIndexOf("a") + 1;
```
Assim, o valor que deverá ter na *const* **ultimaLetraA** sera **6**, pois corresponde com a sexta letra da palavra.

### ***search()***;
Usa-se passando um parâmetro para fazer busca, mas com um pedaço de texto para buscar em uma frase. Considere o exemplo abaixo:
```javascript
const frase = "Olá mundo!";
const posicaoTexto = frase.search("mun");
```
O valor que será atribuído para a *const* **posicaoTexto** será **4**. Isso se deve ao fato de que o texto **"mun"** é encontrado na posição 4 no texto onde foi realizada a busca.

### ***substr()***;
Este método é utilizado para extrair conteúdo de uma string. São utilizados dois parâmetros: posição inicial e quantidade de caracteres a serem extraídos.
Veja o exemplo abaixo:
```javascript
const frase = "Olá mundo!";
const pedacoFrase = frase.substr(0, 3);
```
O conteúdo da *const* **pedacoFrase** será, portanto, **"Olá"**, pois, a partir da posição 0 (primeiro parâmetro do método substr) foram copiados três caracteres (segundo parâmetro do método substr).

### ***replace()***
O método replace() serve para substituir um texto em uma string. Imagine o exemplo abaixo:
```javascript
const tempoHoje = "Hoje está ensolarado!";
const tempoHojeEmJoinville = tempoHoje.replace("ensolarado", "chuvoso");
```
Portanto, considerando a lógica para Joinville, temos que considerar substituir a palavra "ensolarado" para "chuvoso". Assim, o valor da *const* **tempoHojeEmJoinville** será ***"Hoje está chuvoso!"***.

#
## BÓRA PRATICAR?

Colocando em prática o conhecimento apresentado sobre Arrays, vamos para uma pequena lista de exercícios.

## [**<u>Clique aqui para acessar a Lista de Exercícios</u>**](listaExercicios_01/README.md)

##### Alguns links para estudos complementares

* [Developer.mozilla - Array](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array)
* [W3Schools - JavaScript Arrays](https://www.w3schools.com/js/js_arrays.asp)
* [DevMedia - JavaScript Arrays](https://www.devmedia.com.br/javascript-arrays/4079)
* [Bognar Junior - STRING JAVASCRIPT – MÉTODOS.](https://bognarjunior.wordpress.com/2015/01/12/string-javascript-metodos/)
* [Alura - Strings com JavaScript: o que são e como manipulá-las](https://www.alura.com.br/artigos/strings-com-javascript-o-que-sao-e-como-manipular)

##### Vídeos de apoio
* [Código Fonte TV](https://www.youtube.com/watch?v=NfHVPEzo5Ik)
* [Trybe](https://www.youtube.com/watch?v=defBuY0nLrc)
* [Dev Aprender](https://www.youtube.com/watch?v=5nm7lPwNroU)

##### Dúvidas da comunidade sobre switch... case
* [Stack Overflow - Creating arrays in Javascript](https://stackoverflow.com/questions/9543518/creating-arrays-in-javascript)