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
O objetivo é fazer uma tela em que o usuário verá uma lista dos navers.
Para obter a listagem dos navers, faça uma [request](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods) utilizando a [fetch api](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) para o seguinte endpoint: [https://my-json-server.typicode.com/naveteam/fake-api/navers](https://my-json-server.typicode.com/naveteam/fake-api/navers).
Use [esse layout do figma](https://www.figma.com/file/2qJLqFk0DNCR89vZ1P3wMu/Teste-Fornt-End---Estagio?node-id=0%3A1) para se basear na hora de montar a tela.

# Desafio de back-end

## Navedex API

### O Sistema:

O sistema consiste em um banco de dados dos navers, possuindo informações como: nomes, datas de nascimento, cargos, tempo de empresa e projetos que participou.
datas de nascimento Banco de dados será estruturado por você, lembrando que é obrigatório as entidades de `navers` e `projetos` sendo relacionadas entre si de alguma maneira, deverá ser possível saber em quais projetos um naver está e vice-versa.

### O que deve ser entregue:

Deverá ser implementado uma API [node.js](https://nodejs.org) no padrão [`RESTful`](https://becode.com.br/o-que-e-api-rest-e-restful/#:~:text=REST%20significa%20Representational%20State%20Transfer,abstra%C3%A7%C3%A3o%20da%20arquitetura%20da%20Web.) que possibilite as funcionalidades descritas abaixo:

Junto a API, uma documentação de como testar o sistema é muito bem-vinda. Muitas vezes o README.md do projeto basta, porém também é interessante disponibizar documentação a partir de algum software para testar suas requests, recomendamos [postman](https://www.postman.com/) ou [insomnia](https://insomnia.rest/download/);

Tudo isso deve ser colocado em um repositório público do seu github.

### Funcionalidades
- Navers
    - (Index) Rota para listagem dos Navers.
        - Entregará como retorno um vetor com todos os navers, exemplo:
            ```
                [
                    {
                        id: 1, 
                        name: Fulano, 
                        birthdate: 1998-06-12, 
                        admission_date: 2020-06-12,
                        job_role: Desenvolvedor
                    },
                    {
                        id: 2, 
                        name: Ciclano, 
                        birthdate: 1998-06-12, 
                        admission_date: 2018-06-12, 
                        job_role: Desenvolvedor
                    }
                ]
            ```

    - (Show) Rota para detalhar informações de um único naver através de seu identificador
        - Além das informações do naver, trazer quais projetos este participou
        - Entregará como retorno um objeto contendo informações sobre o Naver, exemplo:
            ```
            {
                id: 1, 
                name: Fulano, 
                birthdate: 1998-06-12, 
                admission_date: 2020-06-12,, 
                job_role: Desenvolvedor
                projects: [
                    { 
                        id: 3, 
                        name: Projeto muito Bom
                    }
                ] 
            }
            ```

    - (Store) Rota de Criação de Naver
        - Recebe através do body da request os dados do naver e um vetor com os identificadores dos projetos que ele participa e cria um novo registro no banco de dados
            ```
                {
                    name: Fulano, 
                    birthdate: 1998-06-12, 
                    admission_date: 2020-06-12,
                    job_role: Desenvolvedor,
                    projects: [3]
                }
            ```
        - Entregará como retorno o objeto do usuário criado
            
        

- Projetos
    - (Index) Rota para listagem dos Projetos
        - Entregará como retorno um vetor com todos os projetos, exemplo:
            ```
                [
                    {
                        id: 3, 
                        name: Projeto muito Bom
                    },
                    {
                        id: 5, 
                        name: Projeto Realmente Bom
                    }
                ]
            ```

    - (Show) Rota para detalhar um projeto
        - Além das informações do projeto, trazer quais foram os navers que participaram
        - Entregará como retorno um objeto contendo informações sobre o projeto, exemplo:
            ```
                    {
                        id: 3, 
                        name: Projeto muito Bom,
                        navers: [
                            {
                                id: 1, 
                                name: Fulano, 
                                birthdate: 1998-06-12,
                                admission_date: 2020-06-12, 
                                job_role: Desenvolvedor
                            }
                        ]
                    }
            ```
        
    - (Store) Rota de Criação de Projeto
        - Recebe através do body da request os dados do projeto e um vetor com os identificadores dos navers que trabalham nele e cria um novo registro no banco de dados
            ```
                {
                    name: Projeto Bom,
                    navers: [1]
                }
            ```
        - Entregará como retorno o objeto do Projeto criado

## Observações

As respostas da API devem ser em formato JSON como nos exemplos acima.

Sugestão de bibliotecas para montar a api:

- Koa ou express
- Alguma biblioteca para abstrair a camada de dados que preferir.
  - Knex
  - Bookshelf
  - Objection
  - Mongoose

Prefira o uso de um banco de dados relacional (postgresql, mysql, ...), sendo seu uso não obrigatório.<br>
Para organizar a estrutura de seu projeto prefira o uso do padrão `MVC` sendo seu uso não obrigátório.<br>
Será observado organização de código, legibilidade e melhor uso dos recursos da linguagem javascript.

Se durante o processo de desenvolvimento não conseguiu fazer algo, explique qual o impedimento que encontrou e como tentou resolver em uma seção `Dificuldades` do seu README.md e nos submite até onde chegou :smile:

## (BONUS) Exercício de Banco de Dados
Dado a seguinte estrutura do banco
<br><br>
![banco](https://nave-challenges.s3.amazonaws.com/Back-End-Interniship/database-er.png)
- **E.B.1** Crie um script que delete e crie todas as tabelas.
- **E.B.2** Faça um script que limpe e crie dados nas tabelas.
- **E.B.3** Faça uma querie que traga todos os `navers` ordenados pelo seu tempo de empresa `admission_date`.
- **E.B.4** Faça uma querie que traga todos os `projetos` com seus respectivos `navers`.
- **E.B.5** Faça uma querie que traga todos os `projetos` com sua quantidade de `navers`.
