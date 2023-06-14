# <u>**VARIÁVEIS E OPERADORES**</u>

## **TIPOS DE DADOS**

As variáveis (_const_ e _let_) de um programa podem possuir diferentes tipos, sendo que os principais tipos de dados em JavaScript são:
- string: textos (nomes, cidades, mensagens, etc)
- números: inteiros ou decimais (int ou Number)
- booleanos: verdadeiro ou falso (true or false)

Quando sabemos o tipo do dados, podemos também identificar quais operações são possíveis para as variáveis ou, então, como elas se comportarão durante a execução do programa.

Em JavaScript há algumas **particularidades** que devemos abordar para que não fiquem dúvidas durante o desenvolvimento dos programas. Prestem atenção nas seguintes instruções abaixo envolvendo operações matemáticas (Caso queira, crie o arquivo ***ex07.html*** e cole o código abaixo):

```javascript
<script>
    const a = "30";
    const b = a * 2; //Resultado: 60
    const c = a / 2; //Resultado: 15
    const d = a - 2; //Resultado: 28
    const e = a + 2; //Resultado: 302
    alert("e: " + e);
    document.write("O valor de e é " + e);
</script>
```

Lembram que o sinal de adição **(+)** serve para _concatenar_ strings? Pois então, na linha onde se atribui um valor para a _const_ **e**, o JavaScript entendeu que é para realizar uma _concatenação_. Nas demais linhas, todas as operações matemáticas são realizadas sem qualquer situação inesperada.

**Qual foi o problema?**
> Ocorre é que ao atribuir valor para a _const_ **a**, usamos as aspas " " e, portanto, o JavaScript entendeu que é um **TEXTO**, do tipo **string**. Assim, quando realizamos as operações matemáticas de multiplicação, divisão e subtração, a linguagem converte o valor para número e realiza a operação. Na adição o JavaScript entende que é para _concatenar_ as **strings** e, assim, retorna o resultado ***302*** ao invés do número ***32***.

Para resolver o problema, ou atribuiríamos o valor sem usar as aspas " ", sendo apenas:

**_const a = 30;_**

Ou, então, podemos converter os dados. Podemos usar vários métodos do JavaScript para a conversão, sendo ou o Number(), ou parseInt() ou parseFloat(). Para converter tanto números inteiros como números decimais, recomenda-se o uso do método **Number()**. Então, para realizar a operação matemática de adição, de forma que o JavaScript não concatene os textos, a instrução seria a seguinte:

**_const e = Number(a) + 2_**

O resultado da instrução acima, considerando que o valor atribuído para **a** foi 30, será **32**.

Se quiser percorrer o caminho inverso, ou seja, converter um número em texto (string), o comando será o:

**_document.write("O valor de a é ${a.toString()}");_**

Vale ressaltar que não é necessário, em JavaScript, atribuir um tipo para a variável na sua criação. O tipo será assumido no momento da atribuição de um valor para a variável. Quando utiliza-se as aspas simples ' ' ou aspas duplas " " o JavaScript assumirá automaticamente que a variável que recebeu o valor é do tipo **string**.

Ao trabalhar com valores numéricos, no momento de atribuir valor para a variável não utiliza-se as aspas (seja a simples ' ' ou seja a dupla " "), e, dessa forma, automaticamente a variável será reconhecida como numérica.

Um outro tipo, conforme abordado anteriormente, é o booleano. A variável será do tipo booleano quando a ela for atribuído o valor **true** ou o valor **false**.

Note o código abaixo (Caso queira, crie o arquivo ***ex08.html*** e copie o código abaixo):

```javascript
<script>
    const fruta = "Banana";
    const preco = 3.50
    const levar = true;
    let novoValor
    console.log(typeof fruta);
    console.log(typeof preco);
    console.log(typeof levar);
    console.log(typeof novoValor);
</script>
```

Observe que a variável _novoValor_, no console, será impresso **undefined**. Isso ocorre pois não houve atribuição de valor para a variável e, com isso, não será possível definir o seu tipo.

Também é possível validar se a variável é inteira ou decimal. note o código abaixo (Caso queira, crie o arquivo ***ex09.html***).
```javascript
<script>
    console.log(Number.isInteger(30)); //Deverá retornar true
    console.log(Number.isInteger(30.3)); //Deverá retornar false
</script>
```
A primeira linha retornará _true_, pois o valor que está sendo validado é um valor inteiro. Já a segunda linha retornará _false_, pois o valor que está sendo validado não é inteiro, pois possui casas decimais.

## **Pronto! Agora vamos colocar em prática!**

### [<u>**Lista de Exercícios!**</u>](02_05_01_listaExercicios/README.md)