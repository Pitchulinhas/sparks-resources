# Sparks - SQL Server

## Descrição

SQL Server usado para a permanência dos dados de anti-fraude do e-commerce Sparks.

## Configuração

### Variáveis de ambiente

As variáveis de ambiente abaixo devem ser definidas no arquivo _.env_ na raiz do projeto para que a aplicação funcione corretamente:

- DB_PORT: Porta em que o SQL Server será executado (ex: 1433);
- DB_PASS: Senha do usuário default do banco de dados (ex: sparks20@SQL).

**Você pode usar o arquivo _.env.example_ que está localizado na raiz desta pasta como exemplo**

## Execução

Para executar o SQL Server basta executar o comando abaixo:

```bash
docker compose up -d
```
