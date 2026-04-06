## [Voltar - Funções](../README.md) 

# Funções anônimas
As funções anônimas permitem definir uma função sem nome. Para isso, utilizamos a palavra reservada _function_ e, na sequência, os parâmetros da função e o corpo da função. Veja o exemplo: [EXEMPLO09.HTML](../exemplos/exemplo09.html)

<details>
<summary><b>Solução em JavaScript</b></summary>

```javascript
let situacaoAluno = function(mediaAluno, mediaAprovacao) {
    if (mediaAluno >= mediaAprovacao) {
        return "Aprovado";
    } else {
        return "Reprovado";
    }
}
let resposta = situacaoAluno(10, 6);
alert(resposta);
```
</details>

<details>
<summary><b>Solução em Python</b></summary>

```python
situacaoAluno = lambda mediaAluno, mediaAprovacao: "Aprovado" if mediaAluno >= mediaAprovacao else "Reprovado"

# Ou de forma mais legível:
def situacaoAluno(mediaAluno, mediaAprovacao):
    if mediaAluno >= mediaAprovacao:
        return "Aprovado"
    else:
        return "Reprovado"

resposta = situacaoAluno(10, 6)
print(resposta)
```
</details>

No geral, as funções anônimas são usadas para a inserção de pequenos trechos de código. Por exemplo, imagine que você precisa criar um botão que, quando clicado, exibe uma mensagem na caixa de diálogo. Assim, você pode criar uma função anônima e atribuir essa função ao evento _onclick_ do botão. Veja o exemplo: [EXEMPLO10.HTML](../exemplos/exemplo10.html)

<details>
<summary><b>Solução em JavaScript</b></summary>

```javascript
<button onclick="function() { alert('Olá, mundo!'); }">Clique aqui</button>
```
</details>

<details>
<summary><b>Solução em Python</b></summary>

```python
# Em Python, para interfaces gráficas usa-se bibliotecas como tkinter
import tkinter as tk
from tkinter import messagebox

root = tk.Tk()
botao = tk.Button(root, text="Clique aqui", command=lambda: messagebox.showinfo("Mensagem", "Olá, mundo!"))
botao.pack()
root.mainloop()
```
</details>

Um outro exemplo mais prático, considerando que desejamos mostrar o parcelamento de um produto a ser comprado em uma loja, sendo que o cliente pode escolher o número de parcelas, desde 1 até 10 parcelas. Assim, o programa deve receber o valor do produto e calcular o valor de cada parcela, para que o cliente escolha qual a melhor maneira de efetuar pagamento. Veja o exemplo: [EXEMPLO11.HTML](../exemplos/exemplo11.html)

<details>
<summary><b>Solução em JavaScript</b></summary>

```javascript
    let valorProduto = Number(prompt("Qual é o valor do produto?"));
    let mensagem = "";
    let formasPagamento = function (valorProduto) {
        for (let i = 1; i <= 10; i++) {
            let valorParcela = valorProduto / i;
            mensagem += ("Em " + i + " parcelas, o valor de cada parcela é de R$ " + valorParcela.toFixed(2).replace(".", ",") + "<br>");
        }
        return mensagem;
    }
    let resultado = formasPagamento(valorProduto);
    document.write(resultado);
```
</details>

<details>
<summary><b>Solução em Python</b></summary>

```python
valorProduto = float(input("Qual é o valor do produto?"))
mensagem = ""

def formasPagamento(valorProduto):
    global mensagem
    for i in range(1, 11):
        valorParcela = valorProduto / i
        mensagem += f"Em {i} parcelas, o valor de cada parcela é de R$ {valorParcela:.2f}\n"
    return mensagem

resultado = formasPagamento(valorProduto)
print(resultado)
```
</details>

Note que a função anônima recebe um parâmetro, que é o valor do produto. A função calcula o valor de cada parcela e retorna uma mensagem, que é atribuída à variável _resultado_. Por fim, a variável _resultado_ é exibida na página.

# [Avançar - Funções callback](../04_callback/README.md)

## [Voltar - Funções](../README.md)

**`Algumas funções nativas do JavaScript que valem ser mencionadas aqui, quais podem ser úteis em algum momento da vida do programador:`**
[88funcoes.html](../88funcoes.html)