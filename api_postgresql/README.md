# API PostgreSQL

## Sistema de Gerenciamento de Usuários
Este Sistema foi desenvolvido para gerenciar compras de clientes (usando produtos variados como exemplo), o sistema oferece operações básicas de CRUD (Create, Read, Update, Delete) para manipulação de dados de usuários e seus pedidos. Ele foi criado utilizando Java com Spring Boot no Sprint Tool Suit. Nele existem dois perfis: Teste e Dev. 

### Perfil Teste
O perfil de teste é configurado para utilizar um banco de dados H2, que é uma base de dados em memória. Feito para permitir que as operações CRUD sejam testadas de forma agil. Informações disponíveis em "WebServices\src\main\resources\application-test.properties"

### Perfil Dev
O perfil de desenvolvimento (Dev) é configurado para utilizar o PostgreSQL como banco de dados. Ele se conecta a uma base de dados chamada "springboot". Informações disponíveis em "WebServices\src\main\resources\application-dev.properties"

### Mudar perfil
Para trocar entre os perfis é necessário mudar a variável "spring.profiles.active" no arquivo "WebServices\src\main\resources\application.properties" e também a anotação "@Profile()" no arquivo "WebServices\src\main\java\com\example\course\master\Main.java"