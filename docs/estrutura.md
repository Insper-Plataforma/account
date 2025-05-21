# Estrutura de pastas

```bash
src/main/java/store/account/
├── AccountController.java  # Interface Feign
├── AccountIn.java          # DTO de entrada
└── AccountOut.java         # DTO de saída
```

---

## AccountController

Interface Feign para comunicação com o serviço externo `account`.

---

## AccountIn

Payload de entrada para os serviços `account` com os dados necessários para criação e autenticação do usuário.

---

## AccountOut

Payload retornado pelo serviço `account` com os dados públicos do usuário.

---