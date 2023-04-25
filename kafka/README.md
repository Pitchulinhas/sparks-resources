# Sparks - Apache Kafka

## Descrição

Apache Kafka usado no transporte das mensagens entre as APIs e os microsserviços do e-commerce Sparks.

## Configuração

### Variáveis de ambiente

As variáveis de ambiente abaixo devem ser definidas no arquivo _.env_ na raiz dessa pasta para que a aplicação funcione corretamente:

- ZOOKEEPER_PORT: Porta em que o Zookeeper será executado (ex: 2181);
- ZOOKEEPER_USERS: Logins dos usuários a serem criados no Zookeeper separados por vírgula para autenticação (ex: sparks);
- ZOOKEEPER_USERS_PASSWORDS: Senhas dos usuários definidos na variável ZOOKEEPER_USERS separadas por vírgula (ex: sparks20@ZK);
- ZOOKEEPER_USER: Login de algum usuário definido na variável ZOOKEEPER_USERS (ex: sparks);
- ZOOKEEPER_USER_PASSWORD: Senha correspondente do usuário definido na variável ZOOKEEPER_USER (ex: sparks20@ZK);
- KAFKA_PORT: Porta em que o Kafka será executado (ex: 9092);
- KAFKA_ZOOKEEPER_USER: Login do usuário no Zookeeper (algum usuário definido na variável ZOOKEEPER_USERS, ex: sparks);
- KAFKA_ZOOKEEPER_PASSWORD: Senha correspondente do usuário definido na variável KAFKA_ZOOKEEPER_USER (ex: sparks20@ZK).

**Você pode usar o arquivo _.env.example_ que está localizado na raiz desta pasta como exemplo**

## Execução

Para executar o Kafka e o Zookeeper basta executar o comando abaixo:

```bash
docker compose up -d
```
