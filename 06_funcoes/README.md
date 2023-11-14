# Funções

Aqui falaremos um pouco de funções em JavaScript. É possível criar funções com passagem de parâmetros, com retorno de um valor ou um conjunto de valores e até mesmo funções anônimas. Ainda, podemos fazer com que uma função seja utilizada como um módulo, que contém um trecho de código que se repete e, assim, pode ser acionado várias vezes num mesmo programa ou em diversos programas diferentes.

No que respeita aos módulos, o processo de modularização de programas é uma técnica de programação que consiste em dividir um programa em pequenos módulos, que podem ser desenvolvidos e testados de forma independente. Ainda, a modularização facilita a manutenção, pois quando uma função, que é utilizada em vários programas, precisa ser alterada, basta alterar o módulo correspondente, sem a necessidade de alterar todos os programas que utilizam a função. Em outras palavras, podemos dizer que uma função é um `subprograma` que pode ser chamado por um programa principal ou por outra função.

Um exemplo: Imagine que você precisa desenvolver um programa que coletará os dados de clientes, funcionários e estagiários. Todos esses cadastros coletarão o CPF da pessoa. Assim, você pode desenvolver uma única função para validação do CPF e utilizar essa função em todos os cadastros. Se, por acaso, a regra de validação do CPF mudar, você altera a função e todos os cadastros estarão atualizados.

Embora já utilizemos algumas funções, agora criaremos e manipularemos algumas funções. 


Os tipos de função que serão abordados são:
- [Funções com passagem de parâmetros](01_parametros/README.md)
- [Funções com retorno de valores](02_retorno/README.md)
- [Funções anônimas](03_anonimas/README.md)
- [Funções callback](04_callback/README.md)
- [Funções autoexecutáveis](05_autoexec/README.md)
- [Funções recursivas](06_recursivas/README.md)
- [Funções com parâmetros opcionais](07_outras/README.md#funções-com-parâmetros-opcionais)
- [Funções com parâmetros variáveis](07_outras/README.md#funções-com-parâmetros-variáveis)
- [Funções com parâmetros nomeados](07_outras/README.md#funções-com-parâmetros-nomeados)
- [Funções com parâmetros nomeados e opcionais](07_outras/README.md#funções-com-parâmetros-nomeados-e-opcionais)
- [Funções com parâmetros nomeados e variáveis](07_outras/README.md#funções-com-parâmetros-nomeados-e-variáveis)


##
**`Algumas funções nativas do JavaScript que valem ser mencionadas aqui, quais podem ser úteis em algum momento da vida do programador:`**

>Todas as funções abaixo possuem exemplos disponíveis no arquivo [`88funcoes.html`](88funcoes.html). Você pode acessar o arquivo [clicando aqui](88funcoes.html).

1. **alert()**: exibe uma mensagem na caixa de diálogo;
2. **confirm()**: exibe uma mensagem na caixa de diálogo, com as opções "OK" e "Cancelar";
3. **prompt()**: exibe uma mensagem na caixa de diálogo, com um campo para entrada de dados;
4. **Number()**: converte o valor informado para o tipo numérico;
5. **parseInt()**: converte o valor informado para o tipo numérico inteiro;
6. **parseFloat()**: converte o valor informado para o tipo numérico decimal;
7. **toFixed()**: formata o valor numérico, definindo a quantidade de casas decimais;
8. **replace()**: substitui um caractere por outro caractere;
9. **length**: retorna a quantidade de caracteres de uma string;
10. **toUpperCase()**: converte todos os caracteres de uma string para maiúsculo;
11. **toLowerCase()**: converte todos os caracteres de uma string para minúsculo;
12. **trim()**: remove os espaços em branco no início e no final de uma string;
13. **split()**: divide uma string em um array de strings, de acordo com o caractere informado;
14. **join()**: junta os elementos de um array, separando-os pelo caractere informado;
15. **sort()**: ordena os elementos de um array;
16. **reverse()**: inverte a ordem dos elementos de um array;
17. **push()**: adiciona um elemento no final de um array;
18. **pop()**: remove o último elemento de um array;
19. **shift()**: remove o primeiro elemento de um array;
20. **unshift()**: adiciona um elemento no início de um array;
21. **slice()**: retorna um novo array, de acordo com o início e o fim informados;
22. **splice()**: remove ou substitui elementos de um array, de acordo com o início e a quantidade informados;
23. **concat()**: concatena dois ou mais arrays;
24. **indexOf()**: retorna a posição de um elemento de um array;
25. **lastIndexOf()**: retorna a última posição de um elemento de um array;
26. **includes()**: verifica se um elemento existe em um array;
27. **filter()**: retorna um novo array, de acordo com a condição informada;
28. **map()**: retorna um novo array, de acordo com a condição informada;
29. **reduce()**: retorna um novo array, de acordo com a condição informada;
30. **forEach()**: executa uma função para cada elemento de um array;
31. **some()**: verifica se pelo menos um elemento de um array atende à condição informada;
32. **every()**: verifica se todos os elementos de um array atendem à condição informada;
33. **find()**: retorna o primeiro elemento de um array que atende à condição informada;
34. **findIndex()**: retorna a posição do primeiro elemento de um array que atende à condição informada;
35. **Math.random()**: retorna um número aleatório entre 0 e 1;
36. **Math.round()**: arredonda um número para o inteiro mais próximo;
37. **Math.ceil()**: arredonda um número para o inteiro mais próximo, sempre para cima;
38. **Math.floor()**: arredonda um número para o inteiro mais próximo, sempre para baixo;
39. **Math.pow()**: retorna a potência de um número;
40. **Math.sqrt()**: retorna a raiz quadrada de um número;
41. **Math.abs()**: retorna o valor absoluto de um número;
42. **Math.min()**: retorna o menor valor de um conjunto de números;
43. **Math.max()**: retorna o maior valor de um conjunto de números;
44. **Math.PI**: retorna o valor de PI;
45. **Math.E**: retorna o valor de E;
46. **Date()**: retorna a data e a hora atual;
47. **getFullYear()**: retorna o ano atual;
48. **getMonth()**: retorna o mês atual;
49. **getDate()**: retorna o dia atual;
50. **getDay()**: retorna o dia da semana atual;
51. **getHours()**: retorna a hora atual;
52. **getMinutes()**: retorna o minuto atual;
53. **getSeconds()**: retorna o segundo atual;
54. **getMilliseconds()**: retorna o milissegundo atual;
55. **getTime()**: retorna o timestamp atual;
56. **setFullYear()**: altera o ano;
57. **setMonth()**: altera o mês;
58. **setDate()**: altera o dia;
59. **setHours()**: altera a hora;
60. **setMinutes()**: altera o minuto;
61. **setSeconds()**: altera o segundo;
62. **setMilliseconds()**: altera o milissegundo;
63. **setTimeout()**: executa uma função após um determinado tempo;
64. **setInterval()**: executa uma função em intervalos de tempo regulares;
65. **clearTimeout()**: cancela a execução de uma função agendada com o setTimeout();
66. **clearInterval()**: cancela a execução de uma função agendada com o setInterval().
67. **addEventListener()**: adiciona um evento a um elemento;
68. **removeEventListener()**: remove um evento de um elemento;
69. **stopPropagation()**: interrompe a propagação de um evento;
70. **preventDefault()**: cancela o comportamento padrão de um evento;
71. **target**: retorna o elemento que acionou o evento;
72. **type**: retorna o tipo de evento;
73. **keyCode**: retorna o código da tecla pressionada;
74. **which**: retorna o código da tecla pressionada;
75. **charCode**: retorna o código da tecla pressionada;
76. **pageX**: retorna a posição do eixo X do mouse;
77. **pageY**: retorna a posição do eixo Y do mouse;
78. **offsetX**: retorna a posição do eixo X do mouse, em relação ao elemento;
79. **offsetY**: retorna a posição do eixo Y do mouse, em relação ao elemento;
80. **clientX**: retorna a posição do eixo X do mouse, em relação à janela;
81. **clientY**: retorna a posição do eixo Y do mouse, em relação à janela;
82. **screenX**: retorna a posição do eixo X do mouse, em relação à tela;
83. **screenY**: retorna a posição do eixo Y do mouse, em relação à tela;
84. **altKey**: retorna true se a tecla ALT foi pressionada;
85. **ctrlKey**: retorna true se a tecla CTRL foi pressionada;
86. **shiftKey**: retorna true se a tecla SHIFT foi pressionada;
87. **button**: retorna o botão do mouse pressionado;
88. **buttons**: retorna os botões do mouse pressionados;