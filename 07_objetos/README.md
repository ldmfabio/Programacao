# Objetos

Nesta seção, serão abordados conceitos relacionados com a manipulação de objetos em JavaScript. Este assunto é muito importante, pois, em JavaScript, tudo é um objeto, e será muito útil para a compreensão de outros assuntos, como funções, arrays, etc. Há uma ligação muito forte entre objetos e arrays, e isso será abordado mais adiante.

Como sabemos, um array pode ser uma simples lista de nomes, ou uma lista de objetos, e um objeto pode conter arrays, ou outros objetos, e assim por diante. Portanto, é muito importante compreender bem este assunto.

## Objetos

Em JavaScript, um objeto é uma coleção de pares chave/valor. A chave é uma string, e o valor pode ser qualquer tipo de dado, inclusive outro objeto. O objeto é uma estrutura de dados muito flexível, e pode ser utilizado para representar praticamente qualquer coisa.

Aqui está um exemplo de um objeto simples:

```javascript
let pessoa = {
  nome: "João",
  idade: 25,
  altura: 1.80
};
```

Neste exemplo, temos um objeto chamado `pessoa`, que contém três pares chave/valor. A chave é uma string, e o valor pode ser um número, uma string, ou qualquer outro tipo de dado. O objeto é delimitado por chaves `{}` e os pares chave/valor são separados por vírgula. A chave e o valor são separados por dois pontos `:`.

## Acessando propriedades

Para acessar as propriedades de um objeto, utilizamos a notação de ponto `.` ou a notação de colchetes `[]`. Veja os exemplos:

```javascript
let pessoa = {
  nome: "João",
  idade: 25,
  altura: 1.80
};

console.log(pessoa.nome); // João
console.log(pessoa["idade"]); // 25
```

## Adicionando e removendo propriedades

Podemos adicionar ou remover propriedades de um objeto a qualquer momento. Veja os exemplos:

```javascript
let pessoa = {
  nome: "João",
  idade: 25,
  altura: 1.80
};

pessoa.peso = 80; // Adicionando a propriedade peso
console.log(pessoa); // { nome: 'João', idade: 25, altura: 1.8, peso: 80 }

delete pessoa.altura; // Removendo a propriedade altura
console.log(pessoa); // { nome: 'João', idade: 25, peso: 80 }
```

## Iterando sobre as propriedades

Podemos iterar sobre as propriedades de um objeto utilizando o laço `for...in`. Veja o exemplo:

```javascript
let pessoa = {
  nome: "João",
  idade: 25,
  altura: 1.80
};

for (let prop in pessoa) {
  console.log(prop + ": " + pessoa[prop]);
}
```

Neste exemplo, a variável `prop` irá conter o nome de cada propriedade do objeto, e `pessoa[prop]` irá conter o valor correspondente. O laço irá iterar sobre todas as propriedades do objeto.

## Objetos e funções

Em JavaScript, funções são objetos, e podem ser utilizadas como qualquer outro objeto. Isso significa que podemos adicionar propriedades e métodos a uma função, e podemos passá-la como argumento para outras funções, ou retorná-la como valor de uma função.

```javascript
function somar(a, b) {
  return a + b;
}

somar.nome = "Soma";
somar.descricao = "Função para somar dois números";

console.log(somar(5, 3)); // 8
console.log(somar.nome); // Soma
console.log(somar.descricao); // Função para somar dois números
```

Neste exemplo, a função `somar` recebeu duas propriedades: `nome` e `descricao`. Isso é possível porque funções são objetos, e objetos podem ter propriedades. Além disso, a função `somar` pode ser passada como argumento para outras funções, ou retornada como valor de uma função, como qualquer outro objeto. Isso é um conceito muito importante, por isso é necessário ter compreendido que funções são objetos, e podem ser utilizadas como qualquer outro objeto.

## Conclusão

Nesta seção, aprendemos sobre objetos em JavaScript. Aprendemos como criar, acessar, adicionar, remover e iterar sobre as propriedades de um objeto. Além disso, aprendemos que funções são objetos, e podem ser utilizadas como qualquer outro objeto.