### [**Voltar para o Início**](../../README.md)

#### [**Página Anterior**](../02_03_entrada_de_dados/README.md)

***Requisitos para estar aqui:***
- Ter compreendido e aplicado (desejável) os conceitos sobre Saída e Entrada de Dados!
- Caso não tenha feito, clique nos links abaixo para navegar até o material que ficou pendente
  - [**Saída de Dados**](../02_02_saida_de_dados/README.md)
  - [**Entrada de Dados**](../02_03_entrada_de_dados/README.md)
  - [**Lista de Exercícios**](../02_03_entrada_de_dados/02_03_01_listaExercicios/README.md)

# **VARIÁVEIS E OPERADORES**</u>

## **COMENTÁRIOS**

Durante toda a sua carreira de desenvolvedor, você certamente irá se deparar com códigos que serão difíceis de compreender, pois alguma outra pessoa desenvolveu e você, agora, precisa dar manutenção no código.

Caso a pessoa tenha deixado o código _comentado_, facilitará muito a manutenção. Ou, caso não tenha deixado nenhum _comentário_, e o desenvolvedor anterior não tenha seguido boas práticas, nem deixado o código **indentado**, talvez a manutenção do programa se torne um pouco mais complexa.

> Indentação: consiste em afastar o texto da margem, inserindo espaços entre a margem e o começo do parágrafo, para sinalizar blocos de códigos, deixando-os organizados e de fácil compreensão.

Interessante ressaltar que um _comentário_ que você deixar em um programa que desenvolveu poderá inclusive facilitar a sua própria vida, pois você mesmo, depois de algum tempo (dias, meses, anos...) poderá ter que realizar manutenção no programa. Caso aquela linguagem de programação não faça mais parte da sua rotina, compreender o código, usando o _comentário_ deixado, poderá ser mais fácil.

Os _comentários_ não influenciam a execução do programa, pois são apenas observações, não são instruções que serão interpretadas/compiladas, e é um recurso que está disponível em praticamente todas as linguagens de programação.

No JavaScript nós podemos comentar apenas uma linha ou, então, comentar um bloco inteiro de código.

Acompanhe os exemplos abaixo, porém desconsidere a complexidade do código.

**Exemplo 1: Instruções do Professor e Cálculo de Idade**
```javascript
<script>
    //Problema: Peça para o usuário informar o ano em que nasceu e calcule a idade atual do usuário.

    const anoNascimento = parseInt(prompt(`Informe o ano que nasceu:`));
    //Na linha acima, o usuário informará o ano em que nasceu e o valor será convertido para inteiro. O ano será atribuído na const anoNascimento
    const anoAtual = new Date().getFullYear();
    //Na linha acima, criamos um objeto do tipo Date() e capturamos o ano completo, que contém quatro digitos, usando o método getFullYear(). O valor é atribuído na const anoAtual
    const idade = anoAtual - anoNascimento;
    //Na linha acima, fazemos uma subtração do ano atual pelo ano do nascimento e, assim, chegamos na idade do usuário. Este valor será atribuído na const idade
    document.write(`Em ${anoAtual} você fez ou fará ${idade} anos`);
    //Na linha acima, usamos o método document.write() para escrever uma mensagem para o usuário, concatenando com as informações do ano atual e da idade
</script>
```

> Note que usamos a ***//*** (barra-barra juntas) para identificar aquela linha como sendo um comentário e, assim, não sendo interpretada pelo browser. Ela será "apenas" uma observação, que, neste caso, explica a utilidade de cada linha do código que desenvolvemos. A primeira linha do programa, inclusive, é um comentário que serviu de orientação sobre o que deveria ser feito neste programa.

**Exemplo 2: Comentando em bloco**
```javascript
<script>
    //Problema: Cor Preferida
    /*
    Peça para o usuário informar três cores, sendo uma de cada vez. Após, pergunte ao usuário qual a cor preferida dentre as que informou.
    */

   const cor1 = prompt(`Informe uma cor:`);
   const cor2 = prompt(`Informe outra cor:`);
   const cor3 = prompt(`Informe mais uma cor:`);
   /*
   Nas linhas acima ocorreu o seguinte:
   - cor1 recebeu o nome de uma cor
   - cor2 recebeu o nome de outra cor
   - cor3 foi a última cor informada pelo usuário
   Agora, o sistema possui três nomes de cores diferentes, armazenados em memória
   */

   const preferida = prompt(`Qual a sua cor preferida? ${cor1}, ${cor2} ou ${cor3}?`);
   //Na linha acima o usuário informou qual foi a cor preferida

    document.write(`Dentre as cores ${cor1}, ${cor2} e ${cor3}, a cor preferida do usuário é a ${preferida}.`);
    //Aqui, foi escrita uma mensagem na tela, concatenando com os nomes de todas as cores informadas, indicando qual foi a cor preferida do usuário, também usando concatenação de strings para mostrar o nome da cor preferida.
</script>
```

Viram a utilidade dos _comentários_? Espero que tenham compreendido e adotem essa prática para quando considerarem necessário, seja para deixar alguma anotação sobre o que desenvolveram e precisam lembrar depois, sobre onde pararam de programar e o que ainda está pendente ou, quem sabe, pensando em futuras manutenções no programa que estão desenvolvendo.

### [<u>**Próxima Etapa: Tipos de Dados!**</u>](../02_05_tipos_de_dados/README.md)