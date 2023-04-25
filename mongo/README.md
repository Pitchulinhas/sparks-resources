# Sparks - MongoDB

## Descrição

MongoDB usado para a permanência dos dados de auditoria do e-commerce Sparks.

## Configuração

### Variáveis de ambiente

As variáveis de ambiente abaixo devem ser definidas no arquivo _.env_ na raiz do projeto para que a aplicação funcione corretamente:

- DB_PORT: Porta em que o MongoDB será executado (ex: 27017);
- DB_USER: Login do usuário root do banco de dados (ex: admin);
- DB_PASS: Senha do usuário root do banco de dados (ex: sparks20@MG).

**Você pode usar o arquivo _.env.example_ que está localizado na raiz desta pasta como exemplo**

## Execução

Para executar o MongoDB basta executar o comando abaixo:

```bash
docker compose up -d
```
