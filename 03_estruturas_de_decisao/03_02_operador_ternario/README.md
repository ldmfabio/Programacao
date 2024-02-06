### [**Voltar para o Início**](../../README.md)

#### [**Página Anterior**](../03_01_if_else/README.md)

***Requisitos para estar aqui:***
- Ter finalizado a Lista de Exercícios Obrigatória sobre Estrutura de Decisão [If...Else]!
- Caso não tenha feito, [**CLIQUE AQUI**.](../03_01_if_else/03_01_02_listaExercicios/README.md)

# <u>**Estruturas de Decisão - Operador Ternário**</u>

## **Operador ternário - O que é?**

* **_Conditional Ternary Operator_**
* Existem operações unárias, binárias, ternárias...

## **Operações Unárias**
- Contém apenas _um_ operando!
  - _Significa que contém apenas uma variável de entrada._
  - Exemplos:
    * Raiz Quadrada: √4
    * Negação: !x
    * Fatorial: n!

## **Operações Binárias**
- Contém _dois_ operandos!
  - _Ou seja, contém duas variáveis de entrada._
  - Exemplos:
    * Adição: x + y
    * Multiplicação: x * y

## **Operações Ternárias**
- Contém _três_ operandos!
  - _Consequentemente, três variáveis de entrada._
  - Exemplos:
    * Estruturas de Decisão - Programação (JavaScript)
    * Equivalente ao if...else
      * **<condição> ? <valor_se_verdadeiro> : <valor_se_falso>**
      * **<condição> ? <instruções "_if_"> : <instruções "_else_">**
    * Equivalente ao if...else aninhado
      * **<condição> ? <instruções "_if_">**
        **: <outra_condição> ? <intruções "_else...if_">**
        **: <instruções "_else_">**


### <u>Objetivo é, com operador ternário, obter a seguinte estrutura:</u>*
**_condição ? valor verdadeiro : valor falso_**

Ou então, quando necessário aninhar operador ternário:
**_condição ? valor verdadeiro : nova condição ? valor verdadeiro : valor falso_**

> **_O maior ganho ao utilizar operador ternário é a economia de linhas!_**

> ***Vale ressaltar que todo if, em um operador ternário, deve ser acompanhado de um else.***

## ***Exemplos***

Aqui demonstraremos alguns exemplos de utilização do operador ternário.

_**Exemplo 1**: Peça para o usuário informar o seu ano de nascimento. Caso o ano de nascimento do usuário tenha sido anterior ao ano 2000, deverá mostrar a mensagem "<u>Viu o Bug do Milênio</u>". Caso contrário, deverá mostrar a mensagem "<u>Não viu o Bug do Milênio</u>"._

O código necessário para resolver o problema descrito acima é o seguinte:

```javascript
<meta charset="UTF-8">
<script>
    //Entrada
    const anoNascimento = parseInt(prompt("Informe o seu ano de nascimento: "));

    //Processamento
    let mensagemFinal = "";
    (anoNascimento < 2000) ? mensagemFinal = "Viu o Bug do Milênio" : mensagemFinal = "Não viu o Bug do Milênio";
    
    //Saída
    document.write(mensagemFinal);
</script>

```

_**Exemplo 2:** Colocando um nível a mais de complexidade no problema anteriormente descrito, considere que:_
- _Se o usuário nasceu <u>antes do ano 1900</u>, o programa deverá apresentar a mensagem: **Você é Imortal!**_
- _Se o usuário nasceu <u>após o ano 1900 (inclusive)</u> mas <u>anterior ao ano 2000</u>, o programa deverá apresentar a mensagem: **Viu o Bug do Milênio.**_
- _Se o usuário <u>nasceu após o ano 2000</u>, o programa deverá apresentar a mensagem: **Não viu o Bug do Milênio.**_

O código necessário para resolver o problema descrito acima é o seguinte:

```javascript
<meta charset="UTF-8">
<script>
    //Entrada
    const anoNascimento = parseInt(prompt("Informe o seu ano de nascimento: "));

    //Processamento
    let mensagemFinal = "";
    (anoNascimento < 1900) ? mensagemFinal = "Você é Imortal!" : (anoNascimento < 2000) ? mensagemFinal = "Viu o Bug do Milênio" : mensagemFinal = "Não viu o Bug do Milênio";

    //Saída
    document.write(mensagemFinal);
</script>
```

## **Bóra praticar...**

Colocando em prática o conhecimento apresentado sobre Operador Ternário, vamos para uma pequena lista de exercícios.

## [**<u>Clique aqui para acessar a Lista de Exercícios</u>**](03_02_01_listaExercicios/README.md)