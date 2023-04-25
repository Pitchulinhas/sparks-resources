# Sparks Kafka

## Descrição

Apache Kafka usado para o transporte das mensagens entre as APIs e os microsserviços do e-commerce Sparks.

## Configuração

### Variáveis de ambiente

As variáveis de ambiente abaixo devem ser definidas no arquivo _.env_ na raiz do projeto para que a aplicação funcione corretamente:

- ZOOKEEPER_PORT: Porta em que o Zookeeper será executado. Por exemplo: 2181
- ZOOKEEPER_USERS: Logins dos usuários a serem criados no Zookeeper separados por vírgula para autenticação (ex: sparks)
- ZOOKEEPER_USERS_PASSWORDS: Senhas dos usuários definidos na variável ZOOKEEPER_USERS separadas por vírgula (ex: sparks20@ZK)
- ZOOKEEPER_USER: Login de algum usuário definido na variável ZOOKEEPER_USERS (ex: sparks)
- ZOOKEEPER_USER_PASSWORD: Senha correspondente do usuário definido na variável ZOOKEEPER_USER (ex: sparks20@ZK)
- KAFKA_PORT: Porta em que o Kafka será executado. Por exemplo: 9092
- KAFKA_ZOOKEEPER_USER: Login do usuário no Zookeeper (algum usuário definido na variável ZOOKEEPER_USERS, ex: sparks)
- KAFKA_ZOOKEEPER_PASSWORD: Senha correspondente do usuário definido na variável KAFKA_ZOOKEEPER_USER (ex: sparks20@ZK)

**Você pode usar o arquivo **.env.example** que está localizado na raiz do projeto como exemplo**

### Rede

Para que o Kafka e o Zookeeper consigam se conectar entre si é necessário criar a rede _sparks-kafka-network_, para isso basta executar comando abaixo no seu terminal:

```bash
docker network create --driver bridge sparks-kafka-network
```

### Armazenamento

**Zookeeper**

Para armazenar os dados do Zookeeper é necessário criar o volume _sparks-zookeeper-data_, para isso basta executar comando abaixo no seu terminal:

```bash
docker volume create sparks-zookeeper-data
```

**Kafka**

Para armazenar os dados do Kafka é necessário criar o volume _sparks-kafka-data_, para isso basta executar comando abaixo no seu terminal:

```bash
docker volume create sparks-kafka-data
```

## Execução

Para executar o Kafka e o Zookeeper basta executar o comando abaixo:

```bash
docker compose up -d
```
