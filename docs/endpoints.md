# Endpoints - Feign Interface `AccountController`

Todos os endpoints se referem ao microsserviço `account` com base URL: `http://account:8080`.

---

## POST `/account`

Criação de um novo usuário.

### Request
```json
{
  "name": "Ana Helena",
  "email": "ana@exemplo.com",
  "password": "senha123"
}
```

### Response
```json
{
  "id": "uuid",
  "name": "Ana Helena",
  "email": "ana@exemplo.com"
}
```

---

## GET `/account`

Retorna a lista de todos os usuários registrados.

### Response
```json
[
  {
    "id": "uuid",
    "name": "Lucas",
    "email": "lucas@exemplo.com"
  },
  ...
]
```

---

## POST `/account/login`

Autenticação de um usuário pelo email e senha.

### Request
```json
{
  "email": "ana@exemplo.com",
  "password": "senha123"
}
```

### Response
```json
{
  "id": "uuid",
  "name": "Ana Helena",
  "email": "ana@exemplo.com"
}
```

---

## GET `/account/whoami`

Retorna o usuário logado com base no cabeçalho id-account.

### Headers
```http
id-account: uuid
```

### Request
```json
{
  "id": "uuid",
  "name": "Ana Helena",
  "email": "ana@exemplo.com"
}
```

---

