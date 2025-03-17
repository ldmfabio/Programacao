### [**Voltar para o Início**](../../README.md)

#### [**Página Anterior**](../README.md)

***Requisitos para estar aqui:***
- Ter explorado o conteúdo introdutório sobre Estrutura de Decisão!
- Caso não tenha feito, [**CLIQUE AQUI**.](../README.md)

# <u>**IF...ELSE**</u>

## **Sintaxe básica if...else**

Nem todo _if_ tem um _else_, mas todo _if_ é baseado em uma condição. Dizemos para um programa que, baseando-se em uma condição, ele deve executar uma ação, que contempla uma ou mais instruções que são programadas para serem processadas.

Um exemplo básico de _if_ é o seguinte:

```javascript
    if (condição) {
        // instruções que serão executadas caso a condição seja verdadeira
    }
```

Para que o _if_ funcione corretamente, é necessário que a condição seja verdadeira, ou seja, que o resultado da condição seja _true_. Caso a condição seja falsa, ou seja, o resultado da condição seja _false_, o programa não executará as instruções que estão dentro do bloco do _if_.

Para que o programa execute uma ação caso a condição seja falsa, utilizamos o _else_.

```javascript
    if (condição) {
        // instruções que serão executadas caso a condição seja verdadeira
    } else {
        // instruções que serão executadas caso a condição seja falsa
    }
```

### **Mas o que seriam condições verdadeiras e falsas?**

Para que possamos entender o que são condições verdadeiras e falsas, precisamos entender o que são valores booleanos. Os valores booleanos são um dos tipos de dados que foram abordados no início da disciplina de Programação I.

> ## **<u>_Relembrando:_</u> Tipos de Dados**
> **Booleano**: é um tipo de dado que pode assumir apenas dois valores: _true_ ou _false_.
> 
> **String:** é um tipo de dado que representa um conjunto de caracteres.
> 
> **Number:** é um tipo de dado que representa números, sejam eles inteiros ou decimais.

_Agora que relembramos os tipos de dados, vamos falar sobre os operadores relacionais. Eles serão essenciais para que possamos entender o que são condições verdadeiras e falsas._

## **Operadores Relacionais**

Os operadores relacionais nos acompanharão durante todo o aprendizado de programação, pois eles são utilizados para comparar valores e, a partir dessa comparação, obter um resultado booleano, ou seja, _true_ ou _false_.

A Tabela abaixo contempla os Operadores Relacionais utilizados em JavaScript.

| Operador | Símbolo | Significado |
|:-------:|:-------|:-----------|
| **==** | <u>_Igual a_</u> | Retorna verdadeiro _(true)_ caso os dados contenham o mesmo conteúdo |
| **===** | <u>_Estritamente igual a_</u> | Retorna verdadeiro _(true)_ caso os dados contenham o mesmo conteúdo e sejam do mesmo tipo |
| **!=** | <u>_Diferente de_</u> | Retorna verdadeiro _(true)_ caso os dados não contenham o mesmo conteúdo |
| **!==** | <u>_Estritamente diferente de_</u> | Retorna verdadeiro _(true)_ caso os dados não contenham o mesmo conteúdo ou sejam de tipos diferentes |
| **>** | <u>_Maior que_</u> | Retorna verdadeiro _(true)_ caso o dado da esquerda seja maior que o dado da direita |
| **>=** | <u>_Maior ou igual a_</u> | Retorna verdadeiro _(true)_ caso o dado da esquerda seja maior ou igual ao dado da direita |
| **<** | <u>_Menor que</u>_ | Retorna verdadeiro _(true)_ caso o dado da esquerda seja menor que o dado da direita |
| **<=** | <u>_Menor ou igual a</u>_ | Retorna verdadeiro _(true)_ caso o dado da esquerda seja menor ou igual ao dado da direita |


_A Tabela acima está disponível também via imagem, [**<u>clicando aqui</u>**](operadoresRelacionais.png)._

Agora que já foram apresentados os Operadores Relacionais utilizados em JavaScript, atentem-se aos dois exemplos apresentados na sequência.

#

### **Maioridade**
_Desenvolva um programa que peça para o usuário informar a sua idade e retorne se o usuário já atingiu a maioridade ou não._

_O código fonte deste programa pode ser acessado [**<u>clicando aqui</u>**](01_maioridade.html)._

```javascript
<script>
    const idade = prompt("Informe a sua idade: ");

    if (idade >= 18) {
        alert("Você já atingiu a maioridade!");
    } else {
        alert("Você ainda não atingiu a maioridade!");
    }
</script>
```

### **Saque Bancário**
_Desenvolva um programa que peça para o usuário informar o valor que deseja sacar e retorne se o valor é maior que o saldo disponível na conta. Considere que o valor disponível em conta seja R$ 500,00._

_O código fonte deste programa pode ser acessado [**<u>clicando aqui</u>**](02_saqueBancario.html)._

```javascript
<script>
    const saldo = 500;
    const valorSaque = prompt("Informe o valor que deseja sacar: ");

    if (valorSaque > saldo) {
        alert("Saldo insuficiente!");
    } else {
        alert("Saque realizado com sucesso!");
    }
</script>
```

#

Nestes exemplos acima haviam apenas duas possibilidades de resultado. Mas e se houvessem mais possibilidades? Como poderíamos tratar isso?

Para isso, utilizamos o _else if_, que também podemos chamar de _if else aninhado_, pois aninha/agrupa todas as possibilidades de resultado em uma estrutura de decisão. Ou seja, se a primeira condição for falsa, o programa verifica a próxima condição, e assim sucessivamente até que uma condição seja verdadeira ou até que não hajam mais condições para serem verificadas.

## **Sintaxe básica if...else if...else**

```javascript
    if (condição) {
        // instruções que serão executadas caso a condição seja verdadeira
    } else if (condição) {
        // instruções que serão executadas caso a condição seja verdadeira
    } else {
        // instruções que serão executadas caso a condição seja falsa
    }
```

Vamos então adicionar complexidade ao nosso exemplo do programa desenvolvido para identificar se o usuário atingiu a maioridade ou não. Consideremos validar se:
- Ainda não atingiu a maioridade
- Já atingiu a maioridade
- Já chegou na terceira idade

### **Maioridade ou não e terceira idade**
_Desenvolva um programa que peça para o usuário informar a sua idade e retorne se o usuário já atingiu a maioridade ou não ou talvez já tenha chego na terceira idade._

_O código fonte deste programa pode ser acessado [**<u>clicando aqui</u>**](03_maioridade.html)._

```javascript
<script>
    const idade = prompt("Informe a sua idade: ");

    if (idade < 18) {
        alert("Você ainda não atingiu a maioridade!");
    } else if (idade < 60) {
        alert("Você já atingiu a maioridade!");
    } else {
        alert("Você já está na terceira idade!");
    }
</script>
```
> Note que no exemplo acima, a primeira condição verifica se a idade é menor que 18, ou seja, se o usuário ainda não atingiu a maioridade. Caso a idade seja menor que 18, o programa não verifica as demais condições, pois já sabe que o usuário ainda não atingiu a maioridade.
>
> Na segunda possibilidade, o programa analisa se a idade é menor que 60, ou seja, se o usuário já atingiu a maioridade. Caso a idade seja menor que 60, o programa não verifica a última condição, pois já sabe que o usuário já atingiu a maioridade. Não é necessário, na segunda possibilidade - _else if (idade < 60)_ - também validar se a idade é maior que 18, pois esta condição só será validada se a primeira condição for falsa, ou seja, se a idade do usuário não for menor que 18. Caso a idade seja inferior a 18 anos, o programa não verifica a próxima condição e já finaliza a estrutura de decisão, pois encontrou uma condição verdadeira.
>
> Na terceira possibilidade, o programa analisa se a idade é maior ou igual a 60, ou seja, se o usuário já chegou na terceira idade. Esta validação será feita apenas se as condições anteriores não forem verdadeiras, ou seja, se a idade do usuário não for menor que 18 e se a idade do usuário não for menor que 60. Caso alguma das condições anteriores seja verdadeira, o programa não verifica a última condição, pois já sabe que o usuário ainda não chegou na terceira idade.

Vale ressaltar que o _if...else aninhado_ serve para analisar diversas possibilidades de resultado. A quantidade de _else if_ que podemos utilizar é ilimitada, mas é importante que o programador tenha em mente que, quanto mais _else if_ forem utilizados, mais complexo o programa ficará, e isso pode dificultar a manutenção do código.

Entretanto, para reforçar o aprendizado, vamos adicionar mais algumas possibilidades de resultado ao nosso exemplo.

### **Categorias de Idade**
_Desenvolva um programa que peça para o usuário informar a idade e retorne a categoria de idade correspondente. As categorias são:_

_- Bebê: de 0 a 2 anos_

_- Criança: de 2 a 11 anos_

_- Adolescente: de 11 a 18 anos_

_- Adulto: de 18 a 60 anos_

_- Idoso: acima de 60 anos_

_O código fonte deste programa pode ser acessado [**<u>clicando aqui</u>**](04_categoriaIdade.html)._

```javascript
<script>
    const idade = prompt("Informe a sua idade: ");

    if (idade < 2) {
        alert("Bebê!");
    } else if (idade < 11) {
        alert("Criança!");
    } else if (idade < 18) {
        alert("Adolescente!");
    } else if (idade < 60) {
        alert("Adulto!");
    } else {
        alert("Idoso!");
    }
</script>
```

> Note que, neste exemplo, a primeira condição verifica se a idade é menor que 2, ou seja, se o usuário é um bebê. Caso a idade seja menor que 2, o programa não verifica as demais condições, pois já sabe que o usuário é um bebê.
>
> A segunda condição verificará se a idade é menor que 11, ou seja, se o usuário é uma criança. Caso a idade seja menor que 11, o programa não verifica as demais condições, pois já sabe que o usuário é uma criança. Não é necessário, na segunda condição - _else if (idade < 11)_ - também validar se a idade é maior que 2, pois esta condição só será validada se a primeira condição for falsa, ou seja, se a idade do usuário não for menor que 2.
>
> As mesmas regras são aplicadas para validar se a idade é menor que 18 - _else if (idade < 18)_ - e se a idade é menor que 60 - _else if (idade < 60)_.
>
> A última condição - _else_ - será validada apenas se as condições anteriores não forem verdadeiras, ou seja, se a idade do usuário não for menor que 2, se a idade do usuário não for menor que 11, se a idade do usuário não for menor que 18 e se a idade do usuário não for menor que 60. Caso alguma das condições anteriores seja verdadeira, o programa não verifica a última condição, pois já sabe que o usuário não é um bebê, não é uma criança, não é um adolescente e não é um adulto.

Finalizando a introdução sobre _if...else_ e _if...else if...else_, segue abaixo mais um exemplo de programa que utiliza esta estrutura de decisão.

### **Previsão do Tempo**
_Desenvolva um programa que peça para o usuário informar se está chovendo ou não ou, ainda, se há possibilidade de chuva para a cidade. As opções a serem validadas são:_

-_S: Sim_

-_N: Não_

-_T: Talvez_

_O código fonte deste programa pode ser acessado [**<u>clicando aqui</u>**](05_estaChovendo.html)._

```javascript
    const chuva = prompt(`Está chovendo? (Responda S-Sim, N-Não, T-Talvez)`).toUpperCase().trim();
    if (chuva == "S") {
        alert(`Leve o guarda-chuva!`);
    }
    else if (chuva == "N") {
        alert(`Não precisa do guarda-chuva!`);
    }
    else if (chuva == "T") {
        alert(`Bom levar o guarda-chuva!`);
    }
    else {
        alert(`Opção Inválida - Responda S-Sim, N-Não ou T-Talvez!`);
    }
```
> Neste exemplo, valida-se o dado informado pelo usuário, que deverá ser S, N ou T. Caso o usuário informe S, o programa informa que o usuário deve levar o guarda-chuva. Caso o usuário informe N, o programa informa que o usuário não precisa levar o guarda-chuva. Caso o usuário informe T, o programa aconselha o usuário a levar o guarda-chuva.
>
> Caso o usuário informe qualquer outra opção, o programa informa que a opção é inválida e solicita que o usuário informe uma das opções válidas.

Para complementar o assunto sobre estrutura de decisão usando _if...else_ e _if...else if...else_, falaremos sobre os Operadores Lógicos.

## Como o tema é extenso, ele será abordado em uma seção separada, que pode ser acessado [**<u>clicando aqui</u>**](03_01_01_opLogicos/README.md).