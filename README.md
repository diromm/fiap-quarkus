# fiap-quarkus
Repositório para o trabalho final da matéria 1SCJRBB / quarkus 

Esse projeto é um exemplo de microsserviço que faz CRUD em uma tabela utilizando Quarkus e Panache. 

Foi criado um front end em Angular executando os end-points. 

## Documentação das tecnologias

1. [Quarkus](https://quarkus.io/about/)
	* Quarkus é um framework para java Cloud Native desenvolvido para aplicações java que vão executar na núvem e compatível com a arquitetura Servless. 

## Componentes

1. [Postgres container](./postgres-docker/docker-compose.yml)

* No dirretório Postgres-docker execute o docker-compose
```shell script
cd postgres-docker
docker-compose up -d
cd ..
```

* Para comodidade o ADMINER está exposto no seguinte endereço: http://localhost:8080 Com as seguintes credenciais. [docker-compose.yml](./postgres-docker/docker-compose.yml) 
* Selecione a DataBase **postgres** e o Esquema público. **public**
* Na Opção importar, importe o arquivo [create_tables.sql](postgres-docker\sql\create_tables.sql)


2. CRUD das tabelas.

No diretório drone-crud execute mvn quarkus:dev. O serviço de Crud irá responder em:

localhost:8095.

3. Aplicação web

Diretório: webApp/drones-web

executar npm install --legacy-peer-deps e logo em seguida npm start.

A aplicação vai responder em localhost:4200. 
