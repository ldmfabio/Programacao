## [Voltar - Funções](../README.md) 

# Funções com passagem de parâmetros
Um exemplo de função que utilizamos é a função _alert()_. Essa função recebe um parâmetro, que é o texto que será exibido na caixa de diálogo. A função _alert()_ não retorna nenhum valor, apenas exibe o texto na caixa de diálogo.

> A função alert nos ajuda a unificar a exibição de mensagens para o usuário. Imagine se fosse necessário uma função diferente para cada mensagem que tivesse que ser exibida para o usuário. Assim, você apenas "chama" a função e passa o parâmetro para a função, que é a mensagem a ser exibida para o usuário.

```javascript
alert("Olá, mundo!");
```

```javascript
alert("Bom dia!");
```

Note que a sintaxe é a mesma para as duas chamadas da função, o que muda é o parâmetro passado para a função.

Vamos construir agora um primeiro exemplo, que tem como propósito indicar se o aluno está aprovado ou não. Para isso vamos criar uma função que recebe um parâmetro, que é a média do aluno. Se a média for maior ou igual a 6, o aluno está aprovado, caso contrário, o aluno está reprovado. [EXEMPLO01.HTML](../exemplos/exemplo01.html)

```javascript
function situacaoAluno(media) {
    if (media >= 6) {
        alert("Aprovado!");
    } else {
        alert("Reprovado!");
    }
}
```

Para chamar a função, em qualquer lugar do código, a sintaxe será a seguinte:

```javascript
situacaoAluno(7);
```

Numa situação um pouco diferente, passando dois parâmetros para a função, é possível que seja validada a aprovação do aluno considerando a possibilidade de haverem diferentes médias para a aprovação. Digamos que em um curso a média para aprovação seja 7 e em outro curso a média para aprovação seja 6. Assim, podemos passar dois parâmetros para a função, que são a média do aluno e a média para aprovação. [EXEMPLO02.HTML](../exemplos/exemplo02.html)

```javascript
function situacaoAluno(mediaAluno, mediaAprovacao) {
    if (mediaAluno >= mediaAprovacao) {
        alert("Aprovado!");
    } else {
        alert("Reprovado!");
    }
}
```

Portanto, para chamar a função, utilizando dois parâmetros, a sintaxe será da seguinte forma:

```javascript
situacaoAluno(10, 6);
```

Considere, então, que o programa perguntará ao aluno qual foi sua nota na prova e qual é a média para aprovação. Assim, o programa deve receber esses dois valores e passar para a função. Veja o exemplo: [EXEMPLO03.HTML](../exemplos/exemplo03.html)

```javascript
    //Aqui, a função recebe dois parâmetros, que são a média do aluno e a média para aprovação
    function situacaoAluno(mediaAluno, mediaAprovacao) {
        if (mediaAluno >= mediaAprovacao) {
            alert("Aprovado!");
        } else {
            alert("Reprovado!");
        }
    }

    //Na linha abaixo, o programa pergunta ao aluno qual foi sua média anual obtida
    let mediaAluno = prompt("Qual foi a sua nota na prova?");
    //Na linha abaixo, o programa pergunta ao aluno qual é a média para aprovação
    let mediaAprovacao = prompt("Qual é a média para aprovação?");
    //Na linha abaixo, o programa chama a função, passando os dois parâmetros informados pelo aluno
    situacaoAluno(mediaAluno, mediaAprovacao);
```

> Existem os parâmetros e os argumentos da funçãio. Os parâmetros são, propriamente, os nomes das variáveis - neste caso, _mediaAluno_ e _mediaAprovacao_. Os argumentos são os valores atribuídos para esses parâmetros. Assim, quando chamamos a função, passando os valores 10 e 6, estamos passando os argumentos para os parâmetros _mediaAluno_ e _mediaAprovacao_.

# [Avançar - Funções com retorno](../02_retorno/README.md)

## [Voltar - Funções](../README.md)

**`Algumas funções nativas do JavaScript que valem ser mencionadas aqui, quais podem ser úteis em algum momento da vida do programador:`**
[88funcoes.html](../88funcoes.html)