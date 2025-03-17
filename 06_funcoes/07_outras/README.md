## [Voltar - Funções](../README.md) 

## Outras funções
Neste capítulo, veremos outros tipos de funções. Trataremos de funções com parâmetros opcionais, funções com parâmetros variáveis, funções com parâmetros nomeados, funções com parâmetros nomeados e opcionais e funções com parâmetros nomeados e variáveis.

Clique abaixo e acesse diretamente o conteúdo desejado:
- [Funções com parâmetros opcionais](#funções-com-parâmetros-opcionais)
- [Funções com parâmetros variáveis](#funções-com-parâmetros-variáveis)
- [Funções com parâmetros nomeados](#funções-com-parâmetros-nomeados)
- [Funções com parâmetros nomeados e opcionais](#funções-com-parâmetros-nomeados-e-opcionais)
- [Funções com parâmetros nomeados e variáveis](#funções-com-parâmetros-nomeados-e-variáveis)

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

# Vamos para a prática!

## [Clique aqui para acessar a lista de exercícios proposta](../listaExercicios_01/README.md)

### Ou, caso queira ver os exemplos de utilização da função que foram sugeridos, [clique aqui para acessar os exemplos](../exemplos/README.md)

**`Algumas funções nativas do JavaScript que valem ser mencionadas aqui, quais podem ser úteis em algum momento da vida do programador:`**
[88funcoes.html](../88funcoes.html)