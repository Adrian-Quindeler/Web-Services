# Sistema de Gerenciamento de Usuários com API PostgreSQL
Esta API foi desenvolvida para gerenciar compras de clientes (utilizando vários produtos como exemplo). Ela oferece operações CRUD (Create, Read, Update, Delete) básicas para manipulação de dados de usuários e seus pedidos.

## Tecnologias utilizadas
Java
Spring Boot
Spring Data JPA
PostgreSQL (perfil de desenvolvimento)
H2 (banco de dados em memória para o perfil de teste)

## Perfis
O sistema possui dois perfis:

### Teste: 
Este perfil utiliza um banco de dados em memória (H2) para testes CRUD mais rápidos e ágeis. Os detalhes de configuração estão disponíveis em WebServices\src\main\resources\application-test.properties.

### Dev (Desenvolvimento): 
Este perfil está configurado para usar o PostgreSQL como banco de dados principal. Ele se conecta a um banco de dados chamado "springboot". Os detalhes de configuração estão disponíveis em WebServices\src\main\resources\application-dev.properties.

## Mudando o Perfil
Para alternar entre os perfis, é necessário modificar o seguinte:
A variável "spring.profiles.active em WebServices\src\main\resources\application.properties".
A anotação "@Profile()", encontrada em "WebServices\src\main\java\com\example\course\master\Main.java".

## Estrutura do Sistema
O sistema é organizado em camadas:

Entidades: Representam o modelo de dados (por exemplo, Usuário, Pedido, Produto).
Repositórios: Fornecem acesso à persistência de dados (usando JPA).
Serviços: Camada de lógica de negócios, encapsulando acesso e manipulação de dados.
Resources: Endpoints da API REST para interagir com o sistema.

## Tratamento de Erros
A API implementa tratamento de erros utilizando exceções personalizadas e um mecanismo centralizado para lidar com elas. Isso garante respostas padronizadas para erros comuns, facilitando a identificação e resolução de problemas. 
