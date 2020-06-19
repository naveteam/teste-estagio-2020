# Teste para vaga de estagiário
## Instruções
- Utilizar **apenas JavaScript** puro para resolver o problema (**não é permitido o uso de jquery**);
- Tente sempre utilizar a abordagem ES6+ para resolver os exercícios;
- Os exercícios de lógica (E.1 à E.11) devem ser realizados no codesandbox, utilizando o template [que pode ser encontrado aqui](https://codesandbox.io/s/teste-estagio-template-mnqlh). Você deve adicionar o link do seu codesandbox no readme do repositório que vai ser entregue;
- **Entrega:** todas as soluções devem estar em um único repositório (github, gitlab, bitbucket, etc…) de forma **pública**;
- Neste repositório deve haver, na raiz, um README.md, com as instruções de execução do código desenvolvido;
- Estilo fica ao critério do candidato, e não é o foco principal do teste;
- Só será aceito o uso de bibliotecas de estilo e clientes HTTP (axios, fetch, etc);
- Caso não consiga resolver todos os exercícios, não tem problema, envie mesmo assim;
- Ao finalizar o teste, envie o link do seu repositório por e-mail para vagas@nave.rs.
## Desafio
### Resolver os seguintes exercícios
- **E.1** Crie uma função que recebe duas strings e retorna a de maior comprimento.
- **E.2** Dado a seguinte string `‘teste 1 de 2 string 3’`, substitua todas as ocorrências de números por `$`.
- **E.3** Dado o objeto `{4: ‘a’, 3: ‘e’, 1: ‘i’, 5: ‘s’}` substitua os números na frase `‘T35t3 d3 35t4g1o’` conforme a sua respectiva letra.
- **E.4** Utilizando a api da viacep (https://viacep.com.br/) e o seu cep como entrada imprima o seu endereço no formato `‘ENDERECO, NUMERO, CIDADE/ESTADO’`. Utilize a [fetch API]([https://developer.mozilla.org/pt-BR/docs/Web/API/Fetch_API](https://developer.mozilla.org/pt-BR/docs/Web/API/Fetch_API)) para realizar a requisição.
**Para os seguintes exercícios** considere o array de objetos:
```
[
    {id: 1, first_name: ‘Juca’, last_name: ‘Da Silva’, age: 42},
    {id: 2, first_name: ‘Daniel’, last_name: ‘Gonçalves’,  age: 21},
    {id: 3, first_name: ‘Matheus’, last_name: ‘Garcia’, age: 28},
    {id: 4, first_name: ‘Gabriel’, last_name: ‘Dorneles’,  age: 21}
]
```
- **E.5** Imprima uma mensagem de saudação com o nome completo para cada um dos objetos.
```
Ex.:
Olá, Fulano de tal!
Olá, Juca da silva!
...
```
- **E.6** Imprima a soma das idades (sugestão: utilizar o método [reduce]([https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)))
- **E.7** Encontre o primeiro objeto que possui uma pessoa com a idade menor que 25 e imprima seu nome. Caso não encontre, imprima que nenhum resultado foi encontrado.
- **E.8** Imprima todos os elementos em que a idade é menor que 30.
- **E.9** Ordene o array de forma decrescente por idade, em caso de empate o desempate é pelo id(em ordem crescente).

**Para o seguinte exercício**, considere os array de objetos:
```
const movies = [
	{ id: 1, name: 'Joker' },
	{ id: 2, name: 'Parasite' },
	{ id: 3, name: 'Avengers' },
	{ id: 4, name: 'Her' }
]
const actors = [
	{ id: 1, name: 'Cho Yeo-jeong', movie_ids: [2] },
	{ id: 2, name: 'Robert Downey Jr.', movie_ids: [3] },
	{ id: 3, name: 'Joaquin Phoenix', movie_ids: [1, 4] },
	{ id: 4, name: 'Scarlett Johansson', movie_ids: [3] }
]
```
- **E.10** Faça uma função que receba 2 parâmetros: um array de `movies` e um array de `actors`. A função deve retornar um array de `movies`, onde cada `movie` possui a propriedade `actors`, que sera um array com os nomes dos atores. Por ex:
```
[
  {
	id: 99,
	name: 'Lorem Ipsum',
	actors: ['John Doe', 'Jane Doe']
  }
]
```

# Exercício de front-end
## Desafio
O objetivo é fazer uma tela em que o usuário verá uma lista de postagens.
Cada postagem terá uma lista com seus referentes comentários.
Um post pode ter ou não comentário, dependendo do que vier da API.
## Documentação da API
- API RESTful
- URL: https://jsonplaceholder.typicode.com/
- Para fazer as requisições HTTP recomendamos o uso da biblioteca [axios](https://github.com/axios/axios) usando o seu link de cdn.
Exemplo de requisição:
```javascript
axios
  .get(“/posts”)
  .then(function (response) {
    // handle success
    console.log(response);
  })
  .catch(function (error) {
    // handle error
    console.log(error);
  })
  .then(function () {
    // always executed
  });
```
## Endpoints
GET `https://jsonplaceholder.typicode.com/posts` (busca a listagem de postagens)
GET `https://jsonplaceholder.typicode.com/comments` (busca a listagem de comentários)
## Observações
O que mais será levado em conta é o código JavaScript escrito no teste. Não será levado em consideração o código css. Ainda assim, esperamos uma tela com um minímo de estilo para diferenciar o que é postagem e o que é comentário.
Dica: Para saber quais os comentários de cada postagem, é necessário fazer a comparação do `id` que vem na postagem, com o campo `postId` que vem nos comentários. Sendo iguais, significa que aquele comentário é referente aquela postagem.
# Exercício de back-end
## Desafio
Deverá ser implementado uma API [node.js](https://nodejs.org) no padrão `RESTful` que possibilite a criação e listagem de posts e comentários.
Sendo que cada comentário devem pertencer a um post.
## Observações
Sugestão de bibliotecas para montar a api:
- Koa ou express
- Alguma biblioteca para abstrair a camada de dados que preferir.
  - Knex
  - Bookshelf
  - Sequelize
  - Mongoose
Prefira o uso de um banco de dados relacional (postgresql, mysql, ...), sendo seu uso não obrigatório.<br>
Para organizar a estrutura de seu projeto prefira o uso do padrão `MVC` sendo seu uso não obrigátio.<br>
Será observado organização de código, legibilidade e melhor uso dos recursos da linguagem javascript.
## (BONUS) Exercício de Banco de Dados
Dado a seguinte estrutura do banco
<br><br>
![banco](https://nave-challenges.s3.amazonaws.com/Back-End-Interniship/Screenshot.png)
- **E.B.1** Crie um script de criação das tabelas.
- **E.B.2** Faça um script para popular as tabelas.
- **E.B.3** Faça uma querie que traga todos os `posts` ordenados por `title`.
- **E.B.4** Faça uma querie que traga todos os `posts` com seus respectivos `comments`.
- **E.B.5** Faça uma querie que traga todos os `posts` com sua quantidade de `comments`.
