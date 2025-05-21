# Account Interface

Este módulo define a **interface Feign** para comunicação com o microsserviço `account-service`, responsável pelo gerenciamento de usuários.

---

## Objetivo

Facilitar a comunicação entre microsserviços por meio de chamadas REST encapsuladas, utilizando Feign Client, evitando duplicação de lógica HTTP.

---

## Pacote

- `store.account` - Pacote principal que contém a interface Feign e os objetos de entrada e saída.

---

## Estrutura dos arquivos

| Arquivo | Descrição |
|--------|-----------|
| `AccountController.java` | Interface Feign com os endpoints disponíveis do microsserviço de contas |
| `AccountIn.java` | Objeto de entrada para criação e login |
| `AccountOut.java` | Objeto de resposta contendo dados públicos do usuário |
