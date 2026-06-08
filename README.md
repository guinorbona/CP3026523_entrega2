# Trabalho Final — Etapa 2

Trabalho para aula de Desenvolvimento Web3.

## Pré-requisitos

- Java 17+
- Maven 3.8+
- MySQL 8+
- Postman

## Configuração do banco de dados

Primeiro execute o script abaixo no MySQL:

```sql
CREATE DATABASE ms_user;
CREATE DATABASE ms_email;
```

## Como executar

Abra dois terminais e rode cada serviço separadamente:

```bash
# Terminal — User Service (porta 8081)
cd user-service
mvn spring-boot:run
```

## Endpoints — User Service

| Método | Endpoint | Acesso | Descrição |
|--------|----------|--------|-----------|
| POST | `/auth/request-code` | Público | Gera código aleatório de 6 dígitos |

### Gera código aleatório de 6 dígitos

```json
POST /users
{
  "email": "usuario@email.com",
}
```

Resposta:
```json
{
    "message": "Código enviado para o e-mail informado."
}
```

### Trecho do código do cache

```
CP3026523_entrega2/
└── user-service/
    └── src/main/java/com/example/userservice/
        └── service/CodigoCacheService
```
