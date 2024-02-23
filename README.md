# Desafio Full Cycle Módulo Docker
## Desafio Nginx / Node

Nesse desafio você colocará em prática o que aprendemos em relação a utilização do nginx como proxy reverso. A idéia principal é que quando um usuário acesse o nginx, o mesmo fará uma chamada em nossa aplicação node.js. Essa aplicação por sua vez adicionará um registro em nosso banco de dados mysql, cadastrando um nome na tabela people.

O retorno da aplicação node.js para o nginx deverá ser:

Full Cycle Rocks!

- Lista de nomes cadastrada no banco de dados.

Gere o docker-compose de uma forma que basta apenas rodarmos: `docker-compose up -d` que tudo deverá estar funcionando e disponível na porta: 8080.

Suba tudo em um repositório e faça a entrega.

* A linguagem de programação para este desafio é Node/JavaScript.

# Executando o projeto / container

1. Primeiro você deve criar uma network para que os containers possam se comunicar entre si:

`docker network create app-node-network`

2. Agora basta executar o comando docker-compose para subir os containers:
  
`docker-compose up -d`

3. Agora basta acessar a aplicação em seu browser:

`http://localhost:8080`

Todas as vezes que você atualizar a página, um novo nome será adicionado ao banco de dados.
