## [Voltar - Funções](../README.md) 

# Funções recursivas
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

# [Avançar - Outros Tipos de Funções](../07_outras/README.md)

## [Voltar - Funções](../README.md)

**`Algumas funções nativas do JavaScript que valem ser mencionadas aqui, quais podem ser úteis em algum momento da vida do programador:`**
[88funcoes.html](../88funcoes.html)