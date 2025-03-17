## [Voltar - Funções](../README.md) 

# Funções com retorno de valores

Ao invés de as funções executarem uma ação, como é o caso da função _alert()_, é possível que as funções retornem um valor. Para isso, utilizamos a palavra reservada _return_ e, na sequência, o conteúdo que será retornado.

Utilizando o mesmo problema anterior, vamos criar uma função que recebe dois parâmetros, que são a média do aluno e a média para aprovação. A função deve retornar a mensagem "Aprovado" ou "Reprovado", dependendo da média do aluno. Veja o exemplo: [EXEMPLO04.html](../exemplos/exemplo04.html)


```javascript
function situacaoAluno(mediaAluno, mediaAprovacao) {
    if (mediaAluno >= mediaAprovacao) {
        return "Aprovado";
    } else {
        return "Reprovado";
    }
}
let resposta = situacaoAluno(10, 6);
alert(resposta);
```

Note que a função _situacaoAluno()_ retorna um valor, que é a mensagem "Aprovado" ou "Reprovado". Assim, quando chamamos a função, passando os valores 10 e 6, a função retorna o valor "Aprovado" e esse valor é atribuído à variável _resposta_. Por fim, a variável _resposta_ é exibida na caixa de diálogo.

Ainda, uma função com passagem de parâmetros pode retornar mais de um valor. Para isso, basta separar os valores por vírgula. Veja o exemplo: [EXEMPLO05.HTML](../exemplos/exemplo05.html)

```javascript
function situacaoAluno(mediaAluno, mediaAprovacao) {
    if (mediaAluno >= mediaAprovacao) {
        return ["Aprovado", mediaAluno];
    } else {
        return ["Reprovado", mediaAluno];
    }
}
let resposta = situacaoAluno(10, 6);
alert(`${resposta[0]}, ${resposta[1}`);
```

> **Alerta de spoiler**: mais adiante, veremos que é possível retornar mais de um valor utilizando objetos (_objetos em JavaScript ainda serão abordados na disciplina_).
> Veja o seguinte código em JavaScript, retornando um objeto. [EXEMPLO06.HTML](../exemplos/exemplo06.html)

```javascript
function situacaoAluno(mediaAluno, mediaAprovacao) {
    if (mediaAluno >= mediaAprovacao) {
        return {situacao: "Aprovado", media: mediaAluno};
    } else {
        return {situacao: "Reprovado", media: mediaAluno};
    }
}
let resposta = situacaoAluno(10, 6);
alert(`${resposta.situacao} com média ${resposta.media}`);
```

> Um outro exemplo, retornando um array de objetos: [EXEMPLO07.HTML](../exemplos/exemplo07.html)

```javascript
function dadosPessoa() {
    let pessoas = [
        {nome: "João", idade: 20},
        {nome: "Maria", idade: 30},
        {nome: "José", idade: 40},
        {nome: "Ana", idade: 50}
    ];
    return pessoas;
}
let resposta = dadosPessoa();
alert(`Nome: ${resposta[0].nome}, Idade: ${resposta[0].idade}`);
```

E, caso queira escrever na tela todos os dados de todas as pessoas, basta fazer um laço de repetição: [EXEMPLO08.HTML](../exemplos/exemplo08.html)

```javascript
function dadosPessoa() {
    let pessoas = [
        { nome: "João", idade: 20 },
        { nome: "Maria", idade: 30 },
        { nome: "José", idade: 40 },
        { nome: "Ana", idade: 50 }
    ];
    return pessoas;
}
let resposta = dadosPessoa();
for (let i = 0; i < resposta.length; i++) {
    document.write(`Nome: ${resposta[i].nome}, Idade: ${resposta[i].idade}<br>`);
}
```

# [Avançar - Funções anônimas](../03_anonimas/README.md)

## [Voltar - Funções](../README.md)

**`Algumas funções nativas do JavaScript que valem ser mencionadas aqui, quais podem ser úteis em algum momento da vida do programador:`**
[88funcoes.html](../88funcoes.html)