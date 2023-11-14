## [Voltar - Funções](../README.md) 

# Funções Callbacks (Retorno de Chamada)
As funções callback são funções que são passadas como parâmetro para outra função. Veja o exemplo: [EXEMPLO12.HTML](../exemplos/exemplo12.html)

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

As funções callback são muito utilizadas em eventos de elementos HTML. Por exemplo, imagine que você precisa criar um botão que, quando clicado, exibe uma mensagem na caixa de diálogo. Assim, você pode criar uma função anônima e atribuir essa função ao evento _onclick_ do botão. Veja o exemplo: [EXEMPLO13.HTML](../exemplos/exemplo13.html)

```javascript
<button onclick="function() { alert('Olá, mundo!'); }">Clique aqui</button>
```

Na verdade, as _Funções Callbacks_ foram disponibilizadas na versão mais recente do JavaScript, o ES6. Antes disso, era necessário utilizar as _Funções Anônimas_ para fazer o mesmo que as _Funções Callbacks_ fazem.

Vamos simular um outro exemplo. Considere a seguinte lista de números:
```javascript
let numeros = [1, 2, 4, 7, 5, 3, 6];
```
Digamos que você deseja obter todos os números ímpares que estão presentes no Array acima. Para tal, é possível usar a função `filter()`, que pertence ao objeto Array do JavaScript. Sem utilizar _callbacks_, o código seria o seguinte: [EXEMPLO14.HTML](../exemplos/exemplo14.html)

```javascript
let numeros = [1, 2, 4, 7, 5, 3, 6];
function ehNumeroImpar(nro) {
    return nro % 2 != 0;
}
let numerosImpares = numeros.filter(ehNumeroImpar);
alert(numerosImpares);
```
Como anteriormente ao ES6 utilizavam-se as _Funções Anônimas_, o código acima poderia ser escrito da seguinte forma: [EXEMPLO15.HTML](../exemplos/exemplo15.html)
```javascript
let numeros = [1, 2, 4, 7, 5, 3, 6];
let numerosImpares = numeros.filter(function(nro) {
    return nro % 2 != 0;
});
alert(numerosImpares);
```

Porém, com o advento do ES6, é possível utilizar as _Funções Callbacks_, que são funções que são passadas como parâmetro para outra função. Veja o exemplo: [EXEMPLO16.HTML](../exemplos/exemplo16.html)
```javascript
let numeros = [1, 2, 4, 7, 5, 3, 6];
let numerosImpares = numeros.filter(nro => nro % 2 != 0);
alert(numerosImpares);
```

# [Avançar - Funções autoexecutáveis](../05_autoexec/README.md)

## [Voltar - Funções](../README.md)

**`Algumas funções nativas do JavaScript que valem ser mencionadas aqui, quais podem ser úteis em algum momento da vida do programador:`**
[88funcoes.html](../88funcoes.html)