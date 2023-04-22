# Sparks Kafka

## Descrição

Apache Kafka usado para o transporte das mensagens entre a API e o microsserviço do e-commerce "Sparks".

## Configuração

### Variáveis de ambiente

As variáveis de ambiente abaixo devem ser definidas no arquivo _.env_ na raiz do projeto para que a aplicação funcione corretamente:

- ZOOKEEPER_PORT: Porta em que o Zookeeper será executado na sua máquina. Por exemplo: 2181
- KAFKA_PORT: Porta em que o Kafka será executado na sua máquina. Por exemplo: 9092

**Você pode usar o arquivo **.env.example** que está localizado na raiz do projeto como exemplo**

### Rede

Para que o Kafka e o Zookeeper consigam se conectar entre si é necessário criar a rede _sparks-kafka-network_, para isso basta executar comando abaixo no seu terminal:

```bash
docker network create --driver bridge sparks-kafka-network
```

### Armazenamento

Para armazenar os dados do Kafka é necessário criar o volume _sparks-kafka-data_, para isso basta executar comando abaixo no seu terminal:

```bash
docker volume create sparks-kafka-data
```

## Execução

Para executar o Kafka e o Zookeeper basta executar o comanda abaixo na raiz do projeto:

```bash
docker compose up -d
```
