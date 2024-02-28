<h2>
 📝 Noções básicas de JavaScript
</h2>

<h3>
  Sintaxe
</h3>
<hr>

JavaScript é case-sensitive e usa o conjunto de caracteres Unicode. Por exemplo, a palavra Früh (que significa "cedo" em Alemão) pode ser usada como nome de variável.

```
var Früh = "foobar";
```

Mas a variável früh não é a mesma que Früh porque JavaScript é case sensitive.

<h3>
  Comentários
</h3>
<hr>

```
// comentário de uma linha

/* 
  isto é um comentário longo
   de múltiplas linhas.
 */
```

<h3>
  Declarações
</h3>
<hr>

Existem três tipos de declarações em JavaScript.

- var (descontinuada)

Declara uma variável, opcionalmente, inicializando-a com um valor.

- let

Declara uma variável local de escopo do bloco, opcionalmente, inicializando-a com um valor.

- const

Declara uma constante de escopo de bloco, apenas de leitura.

<h3>
  Tipos de dados
</h3>
<hr>

Seis tipos de dados são os chamados primitivos:

- <b>Boolean:</b> true e false

- <b>null:</b> Uma palavra-chave que indica valor nulo. Devido JavaScript ser case-sensitive, null não é o mesmo que Null, NULL, ou ainda outra variação

- <b>undefined:</b> Uma propriedade superior cujo valor é indefinido

- <b>Number:</b> 42 ou 3.14159

- <b>String:</b> "Senac"

- <b>Symbol (novo em ECMAScript 6):</b> Um tipo de dado cuja as instâncias são únicas e imutáveis

- <b>Object</b>

<h3>
  Operadores lógicos
</h3>
<hr>

- <b>&& :</b> E
- <b>|| :</b> Ou
- <b>! :</b> Não / Negação

<h3>
  Operadores de comparação
</h3>
<hr>

- <b>=== :</b> igual
- <b>!== :</b> diferente
- <b>> e >= :</b> maior e maior igual
- <b>< e <= :</b> menor e menor igual

<h3>
  Operadores Aritméticos
</h3>
<hr>

- <b>+ :</b> soma
- <b>- :</b> subtração
- <b>/ :</b> divisão
- <b>* :</b> multiplicação
- <b>% :</b> resto da divisão

<h3>
  Convertendo strings para números
</h3>
<hr>

No caso de um valor que representa um número está armazenado na memória como uma string, existem métodos para a conversão.

- parseInt()

- parseFloat()

<h3>
  Declaração em bloco
</h3>
<hr>

Uma declaração em bloco é utilizada para agrupar declarações. O bloco é delimitado por um par de chaves

Exemplos:
```
while (x < 10) {
  x++;
}
```

```
if (condicao) {
  declaracao_1;
} else {
  declaracao_2;
}
```

<h3>
  Declaração try...catch
</h3>
<hr>

É composta por um bloco try, que contém uma ou mais declarações. Se qualquer declaração do bloco try lança uma exceção, o controle é imediatamente mudado para o bloco catch. O bloco finally fecha o arquivo antes do script falhar.

```
openMyFile();

try {
  writeMyFile(theData); //Isso pode lançar um erro
} catch (e) {
  handleError(e); // Se temos um erro temos que lidar com ele
} finally {
  closeMyFile(); // Sempre feche o recurso
}
```

<h3>
  Promises
</h3>
<hr>

Representam uma promessa: elas tentarão executar alguma função de forma assíncrona para nós e nos deixarão informados se conseguiu ou não cumprir sua missão. Em outras palavras, uma promise é um objeto que representa a falha ou sucesso de um código

Estados de uma Promise:

- <b>pending (pendente) :</b> estado inicial

- <b>fulfilled (atendida):</b> operação bem sucedida

- <b>rejected (rejeitada):</b> operação falha

- <b>settled (resolvida):</b> a ação foi atendida ou rejeitada

Para criar uma Promise, você deve instanciar um novo objeto Promise e passar uma função com dois parâmetros: resolve e reject. A função resolve é usada para resolver a Promise, enquanto a função reject é usada para rejeitá-la. Veja um exemplo abaixo:

```
const minhaPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Operação concluída com sucesso!');
  }, 1000); // um segundo
});

minhaPromise.then(resultado => {
  console.log(resultado); // Output: Operação concluída com sucesso!
});
```

Neste exemplo, a Promise minhaPromise é resolvida após um segundo. Quando a Promise é resolvida, o método then é chamado, e o resultado é exibido no console.

<h3>
  Async / await
</h3>
<hr>

Async e Await são extensões das Promises, introduzidas para simplificar a escrita de código assíncrono. Uma função marcada como async retorna uma Promise, e a palavra-chave await é usada para esperar o resultado de uma Promise, tornando o código mais legível e fácil de manter

Exemplo:
 ```
 async function processarPromises() {
  try {
    const [resultado1, resultado2] = await Promise.all([
      fetch('<https://api.exemplo1.com>'),
      fetch('<https://api.exemplo2.com>')
    ]);
    // processamento adicional aqui
  } catch (erro) {
    console.error(erro);
  }
}
 ```

## Repetição e iteração

<h3>
  Declaração for
</h3>
<hr>

Um laço for é repetido até que a condição especificada seja falsa. Quando é executado, ocorre o seguinte:

- A expressão é inicializada e, caso possível, é executada. Normalmente essa expressão inicializa um ou mais contadores.

- A expressão condicao é avaliada. caso o resultado de condicao seja verdadeiro, o laço é executado. Se o valor de condicao é falso, então o laço terminará. Se a expressão condicao é omitida, a condicao é assumida como verdadeira.

- A instrução é executada. Para executar múltiplas declarações, use uma declaração em bloco ({ ... }) para agrupá-las.

- A atualização da expressão incremento, se houver, executa, e retorna o controle para o passo 2.

Exemplo: 

```
for(let index = 0, index < 10; index++) {
  console.log(index);
}
```

<h3>
  Declaração do...while
</h3>
<hr>

A instrução será executada uma vez antes da condição ser verificada. Caso a condição seja verdadeira, então o laço será executado novamente. Ao final de cada execução, a condicao é verificada. Quando a condição contida no while for falsa a execução do laço é terminada

Exemplo

```
do {
  i += 1;
  console.log(i);
} while (i < 5);
```

<h3>
  Declaração while
</h3>
<hr>

Uma declaração while executa suas instruções, desde que uma condição especificada seja avaliada como verdadeira. 

- O teste da condição ocorre antes que o laço seja executado

- Desta forma se a condição for verdadeira o laço executará e testará a condição novamente

- Se a condição for falsa o laço termina

```
n = 0;
x = 0;

while (n < 3) {
  n++;
  x += n;
}
```

## Funções

<h3>
  Definindo Função
</h3>
<hr>

Uma função é um bloco de código que pode ser chamado (ou invocado) a partir do seu nome. Permite reutilizar variáveis

- Nome da Função
- Lista de argumentos para a função, entre parênteses e separados por vírgulas
- Declarações JavaScript que definem a função, entre chaves { }

Exemplo

```
function square(numero) {
  return numero * numero;
}
```

<h3>
  Expressão de função
</h3>
<hr>

Funções também podem ser criadas por uma expressão de função. Tal função pode ser anônima, sem nome. Por exemplo, a função square poderia ter sido definida como:

Exemplo:

```
let square = function (numero) {
  return numero * numero;
};

let x = square(4); //x recebe o valor 16
```

## Objetos

Um objeto é uma coleção de propriedades, e uma propriedade é uma associação entre um nome (ou chave) e um valor. Um valor de propriedade pode ser uma função, que é então considerada um método do objeto.

Exemplo:

```
const caneta = {
  codigo: 51023,
  marca: 'bic'
  cores: ['azul','vermelha','verde','preto'],
  data_fabricacao: '2023-05-07',
  escrever: function() {
    console.log('Dale Grêmio!')
  }
}
```

<h3>
  Declaração try...catch
</h3>
<hr>

<h3>
  Declaração try...catch
</h3>
<hr>

<h3>
  Declaração try...catch
</h3>
<hr>