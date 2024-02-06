### [**Voltar para o Início**](../../README.md)

#### [**Página Anterior**](../03_02_operador_ternario/README.md)

***Requisitos para estar aqui:***
- Ter finalizado a lista de exercícios obrigatória sobre Operador Ternário!
- Caso ainda não tenha finalizado, [**CLIQUE AQUI**.](../03_02_operador_ternario/03_02_01_listaExercicios/README.md)

# <u>**Estruturas de Decisão - Switch...Case**</u>

## _**Como assim... Switch...Case?**_

### **Outra estrutura de decisão**
  * Praticamente todas as linguagens de programação possuem distintas estruturas de decisão.

**Quando usar?**
- Quando houverem várias alternativas a partir do valor de uma constante/variável;
- É uma lógica fácil e intuitiva.

**Sobre a utilização**
* O comando switch inicia pela definição da variável/constante que escolhe a condição a ser executada. Cada instrução deve conter um valor de comparação (seguida pelos dois pontos ":"), como no exemplo abaixo.

```javascript
<meta charset="UTF-8">
<script>
let mesDoAno = 1;
switch (mesDoAno) {
  case 1:
    document.write("Janeiro");
    break;
  case 2:
    document.write("Fevereiro");
    break;
}
</script>
```
 _Os comandos sempre devem ser finalizados por_
 ```javascript
 break;
 ```
O comando acima escreverá **Janeiro** na tela, pois a primeira linha já atribuiu o valor 1 logo ao criar a **_let_** **mesDoAno** (*let mesDoAno = 1;*).

## **IMPORTANTE!!!**
Caso o comando _break;_ não seja incluído logo após o comando que será executado atendendo a condição - que nesse caso será _document.write("Janeiro");_ - o programa entrará em todas as condições seguintes, até que encontre um comando _break;_ em alguma das próximas condições.

> _O comando break; para a execução do switch...case, indo para a próxima linha logo após o término das instruções que fazem parte do block switch...case. Ou seja, o programa continua sendo executado, apenas o switch...case que finaliza com o comando break;_

Outro recurso do **_switch...case_** que vale ser mencionado é a utilização da opção *default*. Esta opção é a opção padrão e o que houver de instrução nela será executado quando as comparações realizadas não forem validadas. Por exemplo:

```javascript
<meta charset="UTF-8">
<script>
const diaDaSemana = "domingo";
switch (diaDaSemana) {
    case "sábado":
        document.write("Dia de folga!");
        break;
    case "domingo":
        document.write("Dia de folga!");
        break;
    default:
        document.write("Dia de trabalho!");
        break;
}
</script>
```

Nesse caso, o resultado será **"Dia de folga!"**. Porém, caso o valor da _const_ **_diaDaSemana_** fosse qualquer coisa diferente de _sábado_ ou _domingo_, por exemplo, o programa executaria a opção **default**.

Ainda, considerando o exemplo anterior, é possível que otimizemos o código. Observe que existem dois dias de folga (sábado e domingo). Portanto, como ou um ou outro dia são de folga, e diferente deles é trabalho, podemos otimizar da seguinte forma:

```javascript
<meta charset="UTF-8">
<script>
const diaDaSemana = "segunda";
switch (diaDaSemana) {
    case "sábado":
    case "domingo":
        document.write("Dia de Folga!");
        break;
    default:
        document.write("Dia de Trabalho!");
        break;
}
</script>
```

Esta otimização é equivalente com a utilização do operador **OU**, que refere a utilização dos caracteres " || ".
> **_A principal vantagem do switch...case é a facilidade para compreender a sua estrutura, sendo extremamente intuitivo._**


## **Bóra praticar...**

Colocando em prática o conhecimento apresentado sobre Switch...Case, vamos para uma pequena lista de exercícios.

## [**<u>Clique aqui para acessar a Lista de Exercícios</u>**](03_03_01_listaExercicios/README.md)