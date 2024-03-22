# Workshop: Sistema de Gerenciamento de Usuários com MongoDB
Este projeto está sendo desenvolvido com conceitos básicos de persistência de dados utilizando o banco de dados NoSQL MongoDB. A API CRUD (Create, Read, Update, Delete) permite gerenciar usuários, possibilitando a criação, leitura, atualização e exclusão de seus registros.

## Tecnologias utilizadas
Java
Spring Boot
Spring Data MongoDB
Dependencia
MongoDB (banco de dados NoSQL)


## Estrutura do Sistema
O sistema é organizado em camadas para promover modularidade e manutenção:

- Domínio (domain): Define os objetos do modelo de dados, encapsulando lógica e atributos.
- Repositório (repository): Provê acesso e operações de persistência de dados no MongoDB.
- Serviço (services): Camada de negócio responsável pela manipulação de dados, utilizando métodos do repositório.
- Recursos (resources): Expõe endpoints REST para interação externa com o sistema.
- DTO (Data Transfer Object): Objetos simples utilizados para transferência de dados específicos entre camadas.
- Configuração (config): Inicializa o banco de dados e popula dados de exemplo.


## Classes principais
- User: Representa a entidade Usuário, com atributos para nome (name) e email.
- UserRepository: Interface que estende MongoRepository para operações com documentos User no MongoDB.
- UserService: Camada de serviço para manipular usuários, delegando operações ao UserRepository.
- UserResource: Classe responsável por expor endpoints REST para gerenciamento de usuários.
- UserDTO: Objeto DTO para transferir dados de usuário entre camadas, contendo apenas atributos necessários (id, name, email).