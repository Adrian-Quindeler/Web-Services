# Workshop: Sistema de Gerenciamento de Usuários com MongoDB
Este projeto está sendo desenvolvido com conceitos básicos de persistência de dados utilizando o banco de dados NoSQL MongoDB. A API CRUD (Create, Read, Update, Delete) permite gerenciar usuários, possibilitando a criação, leitura, atualização e exclusão de seus registros.

## Tecnologias utilizadas
Java
Spring Boot
Spring Data MongoDB
Postman
MongoDB (banco de dados NoSQL)


## Estrutura do Sistema
O sistema consiste em uma API de uma rede social genérica com usuários, suas postagens e comentários, feito no sping tool suite com MongoDB e testado usando o Postman. Suas classes são divididas em:

- Domínio (domain): Define os objetos do modelo de dados.
- Repositório (repository): Provê acesso e operações de persistência de dados no MongoDB.
- Serviço (services): Camada de negócio responsável pela manipulação de dados, utilizando métodos do repositório.
- Recursos (resources): Expõe endpoints REST para interação externa com o sistema.
- DTO (Data Transfer Object): Objetos simples utilizados para transferência de dados específicos entre camadas.
- Configuração (config): Inicializa o banco de dados e popula dados de exemplo.

## Endpoints
### Consulta por Título de Postagem: 
Foi implementada duas opções de consulta por título da postagem no PostRepository. Uma delas utiliza a anotação @Query, a outra ultiliza um dos Query methods oferecidos pelo Spring Data, chamado "findByTitleContainingIgnoreCase";

### Consulta Avançada: 
Outra consulta personalizada no PostRepository foi criada para realizar uma busca avançada por título, corpo ou comentários da postagem, podendo também definir data mínima e data máxima de busca. Novamente, foi utilizada a anotação @Query para definir a lógica da consulta.

### Endpoints RESTful: 
Os métodos para acesso aos recursos (usuários, postagens) foram implementados nas classes de recursos (UserResource e PostResource) utilizando as anotações do Spring MVC (@RestController, @RequestMapping, @RequestParam, @PathVariable, etc.). Cada método corresponde a uma operação CRUD específica.

