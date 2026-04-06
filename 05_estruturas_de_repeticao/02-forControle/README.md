### [**Voltar para o Início**](../../README.md)

#### [**Página Anterior**](../01-forOf/README.md)

***Requisitos para estar aqui:***
- Ter finalizado a Lista de Exercícios sobre a Estrutura de Repetição For...Of!
- Caso não tenha feito, [**CLIQUE AQUI**.](../01-forOf/listaExercicios_01/README.md)

# Repetição com variável de controle
## Laços de repetição com For

Ao invés de utilizarmos o ***for of*** limitado ao número de itens que possuem em uma lista, podemos determinar a quantidade de vezes que o nosso for repetirá as instruções que programarmos.

Para esse fim, o ***for*** será composto por três instruções, que são:
* O valor inicial da variável que controlará a quantidade de repetições das instruções do programa;
* A condição que determina se a repetição deve ou não continuar;
* O incremento ou decremento da variável de controle.

    *Dica: Considere que você precisa adicionar valor para uma let, e este valor será incrementado para o próximo número em um valor. Ou seja, a let número vale 1 e você deseja que ela valha 2. Para fazer isso, você tem algumas formas distintas:*

<details>
<summary><b>Solução em JavaScript</b></summary>

```javascript
    let numero = 1; //Valor inicial da let numero
    numero = numero + 1; //Agora a número valerá 2
    numero += 1 //Agora a número valerá 3
    numero ++ //Ou numero++, que atribuirá valor 4 para a let número
```
</details>

<details>
<summary><b>Solução em Python</b></summary>

```python
numero = 1  # Valor inicial de numero
numero = numero + 1  # Agora numero valerá 2
numero += 1  # Agora numero valerá 3
# Python não tem ++, use += 1
numero += 1  # Agora numero valerá 4
```
</details>

*Todas as formas acima adicionarão um valor acima para a let numero.*

Então, em uma estrutura de repetição em que você deseja controlar a quantidade de vezes que as instruções serão repetidas, o for deverá ser da seguinte forma:

<details>
<summary><b>Solução em JavaScript</b></summary>

```javascript
for (let contador = 1; contador <= 5; contador++) {
    alert(contador);
}
```
</details>

<details>
<summary><b>Solução em Python</b></summary>

```python
for contador in range(1, 6):
    print(contador)
```
</details>

*As instruções que você colocar entre as chaves { } serão as instruções que você deseja repetir.*

No exemplo acima, definimos a *let contador* para que ela determinasse a quantidade de vezes que a instrução que está dentro do *for* fosse executada. O resultado será um programa que apresentará um alerta cinco vezes, começando com o valor ***1*** no alerta na primeira vez. Na segunda vez, o alerta apresenta o valor ***2***, na terceira vez o valor ***3***, na quarta vez o valor ***4*** e na quinta vez o valor ***5***.

Temos a possibilidade de atribuir um valor diferente para a *let contador*, por exemplo. Caso deseja que o alerta seja exibido a partir do valor 3, por exemplo, basta mudar o código para que a estrutura de repetição comece já com o valor 3 na let contador.

<details>
<summary><b>Solução em JavaScript</b></summary>

```javascript
for (let contador = 3; contador <= 5; contador++) {
    alert(contador);
}
```
</details>

<details>
<summary><b>Solução em Python</b></summary>

```python
for contador in range(3, 6):
    print(contador)
```
</details>

Assim, o alerta começa apresentando o valor ***3***, posteriormente o valor ***4*** e, por último, o valor ***5***.

Outra possibilidade, caso exista essa demanda, é incrementar valores diferentes para a *let contador*. Digamos que você quer incrementar de dois em dois valores, iniciando do 1 e indo para o 5. Considere o exemplo abaixo.

<details>
<summary><b>Solução em JavaScript</b></summary>

```javascript
for (let contador = 1; contador <= 5; contador+=2) {
    alert(contador);
}
```
</details>

<details>
<summary><b>Solução em Python</b></summary>

```python
for contador in range(1, 6, 2):
    print(contador)
```
</details>

A imagem abaixo explica, com mais detalhes, cada elemento da sintaxe do ***for*** com variável de controle.


![estruturaFor](estruturaFor.png)

Em um outro exemplo clássico de utilização do ***for*** com variável de controle, considere calcular a tabuada.

Para calcular a tabuada de 2, por exemplo, será necessário o seguinte código em JavaScript:

<details>
<summary><b>Solução em JavaScript</b></summary>

```javascript
for (let contador = 1; contador <= 10; contador++) {
    document.write(`2 x ${contador} = ${contador * 2}</br>`);
}
```
</details>

<details>
<summary><b>Solução em Python</b></summary>

```python
for contador in range(1, 11):
    print(f"2 x {contador} = {contador * 2}")
```
</details>

*A tag br colocada ao final da instrução document.write servirá para quebrar linha após apresentar o cálculo respectivo com a instrução executada pelo programa.*

Assim, o resultado que será escrito na tela será:

![tabuadaDe2](tabuadaDe2.png)

Contudo, caso queira deixar que o usuário insira o número que deseja calcular a tabuada, não sendo apenas a tabuada de 2, o código será o seguinte:

<details>
<summary><b>Solução em JavaScript</b></summary>

```javascript
let numeroUsuario = Number(prompt("Número para calcular tabuada:"))
    for (let contador = 1; contador <= 10; contador++) {
        document.write(`${numeroUsuario} x ${contador} = ${contador * numeroUsuario}</br>`)
    }
```
</details>

<details>
<summary><b>Solução em Python</b></summary>

```python
numeroUsuario = int(input("Número para calcular tabuada:"))
for contador in range(1, 11):
    print(f"{numeroUsuario} x {contador} = {contador * numeroUsuario}")
```
</details>

Inicialmente, o programa perguntará para o usuário qual o número que deseja calcular a tabuada, que é o nosso já conhecido prompt.

![tabuadaDoUsuario](tabuadaDoUsuario.png)

Assim, o resultado da tabuada, conforme solicitado pelo usuário, será o apresentado na imagem abaixo.

![TabuadaDoUsuarioResultado](tabuadaDoUsuarioResultado.png)

# IMPORTANTE!!!

Todo o conteúdo que já trabalhamos até aqui na disciplina de Programação será aplicado ao trabalharmos com estruturas de repetição.
Os temas que aparecerão aqui repetidamente são:
* if... else (e if... else aninhado)
* operador ternário (e operador ternário aninhado)
* switch... case
* variáveis e operadores (muitas operações matemáticas!)
* e, principalmente, [**Arrays!!**](../../04_arrays/README.md)

#
## BÓRA PRATICAR?

Colocando em prática o conhecimento apresentado sobre For com Variável de Controle, vamos para uma pequena lista de exercícios.

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