# <u>**OPERADORES LÓGICOS**</u>

Anteriormente os exemplos citados baseavam-se em uma única condição, porém, em muitos casos, é necessário avaliar mais de uma condição para que uma ação seja executada. Para isso, utilizamos os operadores lógicos.

Os operadores lógicos são utilizados para combinar duas ou mais condições. Os operadores lógicos são: **and**, **or** e **not**.

| Operador | Símbolo | Descrição |
| :---: | :---: | :--- |
| **and** | **&&** | Retorna True se as duas condições forem verdadeiras |
| **or** | **\|\|** | Retorna True se uma das condições for verdadeira |
| **not** | **!=** | Inverte o resultado, retorna False se o resultado for verdadeiro |

Para melhor explicar os operadores lógicos, abordaremos exemplos utilizando a _Tabela Verdade_.

O uso da _Tabela Verdade_ demanda a definição de um cenário que considere ao menos dois fatores que influenciam na tomada de decisão e, por consequência, a(s) instrução(ões) a ser(em) executada(s) em decorrência da decisão tomada.

**Portanto, imaginemos o seguinte cenário...**

#

Utilizando o operador lógico **e**, podemos montar a _Tabela Verdade_ para o cenário em que o aluno será aprovado se tiver nota maior ou igual a 6 **_e_** frequência maior ou igual a 75%. Então a condição para montar a _Tabela Verdade_ é:

> **_Se_** o aluno **_tiver_** nota maior ou igual a 6 **_e_** frequência maior ou igual a 75%, **_então_** o aluno **_está_** aprovado.

Dado o cenário com as condições para a aprovação do aluno (tendo a aprovação como resultado verdadeiro), podemos montar a _Tabela Verdade_.

Vale ressaltar que a _Tabela Verdade_ é montada com base nas condições que influenciam na tomada de decisão, ou seja, as condições que, se verdadeiras, resultarão na execução da(s) instrução(ões) definida(s) no bloco de código.

As condições que influenciam na tomada de decisão são:

| Nota | Operador | Frequência |  | Aprovado |
| :---: | :---: | :---: | :---: | :---: |
| >= 6 | **E - &&** | >= 75% | *ENTÃO* | True |
| >= 6 | **E - &&** | < 75% | *ENTÃO* | False |
| < 6 | **E - &&** | >= 75% | *ENTÃO* | False |
| < 6 | **E - &&** | < 75% | *ENTÃO* | False |

___Traduzindo___ a _Tabela Verdade_ para valores booleanos, resultantes das condições estabelecidas, temos os seguintes dados:

| Nota | Operador | Frequência |  | Aprovado |
| :---: | :---: | :---: | :---: | :---: |
| True | **E - &&** | True | *ENTÃO* |True |
| True | **E - &&** | False | *ENTÃO* | False |
| False | **E - &&** | True | *ENTÃO* | False |
| False | **E - &&** | False | *ENTÃO* | False |


Ou seja, considerando que as instruções serão executadas apenas **_se_** a nota for maior ou igual a 6 **_e_** a frequência for maior ou igual a 75%, a única situação que atende a essas duas condições é a primeira linha da _Tabela Verdade_, portanto, o aluno será aprovado. Nas demais, o aluno não será aprovado e, portanto, o resultado será falso, sendo executadas as instruções definidas no bloco de código do **else**.

#

Agora, utilizando o operador lógico **or**, podemos montar a _Tabela Verdade_ para o cenário em que o aluno será aprovado se tiver nota maior ou igual a 6 na disciplina avaliada **_ou_** foi aprovado por média geral calculada em todas as disciplinas. Então a condição para montar a _Tabela Verdade_ é:

| Nota | Operador | Média Geral |  | Aprovado |
| :---: | :---: | :---: | :---: | :---: |
| >= 6 | **OU - \|\|** | >= 6 | *ENTÃO* | True |
| >= 6 | **OU - \|\|** | < 6 | *ENTÃO* | True |
| < 6 | **OU - \|\|** | >= 6 | *ENTÃO* | True |
| < 6 | **OU - \|\|** | < 6 | *ENTÃO* | False |

___Traduzindo___ a _Tabela Verdade_ para valores booleanos, resultantes das condições estabelecidas, temos os seguintes dados:

| Nota | Operador | Média Geral |  | Aprovado |
| :---: | :---: | :---: | :---: | :---: |
| True | **OU - \|\|** | True | *ENTÃO* | True |
| True | **OU - \|\|** | False | *ENTÃO* | True |
| False | **OU - \|\|** | True | *ENTÃO* | True |
| False | **OU - \|\|** | False | *ENTÃO* | False |

Ou seja, considerando que as instruções serão executadas **_se_** a nota for maior ou igual a 6 **_ou_** a média geral for maior ou igual a 6, as três primeiras linhas da _Tabela Verdade_ atendem a essas condições, portanto, o aluno será aprovado. Na última linha, o aluno não será aprovado e, portanto, o resultado será falso, sendo executadas as instruções definidas no bloco de código do **else**. O aluno não foi aprovado pois não atendeu a nenhuma das condições estabelecidas, não atingindo nota 6 na disciplina e também não atingiu Média Geral 6, que eram as duas possibilidades para conseguir obter a aprovação.

#

Por fim, utilizando o operador lógico **not**, podemos montar a _Tabela Verdade_ para o cenário em que o aluno será aprovado se não tiver nota menor que 6 na disciplina avaliada. Então a condição para montar a _Tabela Verdade_ é:

| Nota | Operador |  | Aprovado |
| :---: | :---: | :---: | :---: |
| < 6 | **NOT - !=** | *ENTÃO* | True |
| >= 6 | **NOT - !=** | *ENTÃO* | False |

___Traduzindo___ a _Tabela Verdade_ para valores booleanos, resultantes das condições estabelecidas, temos os seguintes dados:

| Nota | Operador |  | Aprovado |
| :---: | :---: | :---: | :---: |
| False | **NOT - !=** | *ENTÃO* | True |
| True | **NOT - !=** | *ENTÃO* | False |

<br>
<br>
<br>

# **Praticando...**

Vamos então agora colocar em prática o conteúdo abordado até aqui. Como sugestão, fica a lista de exercícios com 18 problemas para serem resolvidos, [**que está disponível clicando aqui**](../03_01_02_listaExercicios/README.md).

#