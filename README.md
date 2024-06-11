# Book Eureka Server

Este é o servidor Eureka para o projeto Book API. Ele gerencia o registro e a descoberta de serviços.

## Instalação

### Pré-requisitos

- [Java 17+](https://adoptopenjdk.net/)
- [Gradle](https://gradle.org/)
- [Docker](https://www.docker.com/)

### Passos para Instalação

#### Método 1: Usando Java

1. Clone o repositório do servidor Eureka:
    ```sh
    git clone https://github.com/seu-usuario/book-eureka-server.git
    cd book-eureka-server
    ```

2. Compile e rode o servidor Eureka:
    ```sh
    ./gradlew bootRun
    ```

3. Após iniciar o servidor, você pode acessar o painel do Eureka no seguinte URL:
    ```
    http://localhost:8761
    ```

#### Método 2: Usando Docker

1. Crie a rede Docker:
    ```sh
    docker network create book-network
    ```

2. Construa a imagem Docker do servidor Eureka:
    ```sh
    docker build --tag book-eureka-server .
    ```

3. Rode o contêiner do servidor Eureka:
    ```sh
    docker run --name book-eureka-server -p 8761:8761 --network book-network book-eureka-server
    ```

4. Após iniciar o contêiner, você pode acessar o painel do Eureka no seguinte URL:
    ```
    http://localhost:8761
    ```


Fique à vontade para contribuir com este projeto.
