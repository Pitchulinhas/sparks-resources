# Sparks - PostgreSQL

## Descrição

PostgreSQL usado para a permanência dos dados do e-commerce Sparks.

## Configuração

### Variáveis de ambiente

As variáveis de ambiente abaixo devem ser definidas no arquivo _.env_ na raiz do projeto para que a aplicação funcione corretamente:

- DB_PORT: Porta em que o PostgreSQL será executado (ex: 5432);
- DB_USER: Login do usuário default do banco de dados (ex: postgres);
- DB_PASS: Senha do usuário default do banco de dados (ex: sparks20@PG).

**Você pode usar o arquivo _.env.example_ que está localizado na raiz desta pasta como exemplo**

## Execução

Para executar o PostgreSQL basta executar o comando abaixo:

```bash
docker compose up -d
```
