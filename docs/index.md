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

| Arquivo                  | Descrição                                                               |
| ------------------------ | ----------------------------------------------------------------------- |
| `AccountController.java` | Interface Feign com os endpoints disponíveis do microsserviço de contas |
| `AccountIn.java`         | Objeto de entrada para criação e login                                  |
| `AccountOut.java`        | Objeto de resposta contendo dados públicos do usuário                   |

---

## Integração com Jenkins

Este projeto conta com um arquivo Jenkinsfile (na raiz do repositório) que define uma pipeline de integração contínua para compilar automaticamente o módulo sempre que houver alterações no repositório.

### Para que serve?

- Ao efetuar um push no repositório, o Jenkins detecta a mudança e executa esta pipeline.

- A etapa Build faz a compilação do projeto:

    1. Executa mvn clean install em modo batch (parâmetro -B), sem interação de usuário.

    2. Pulando os testes (-DskipTests), gera rapidamente o artefato (JAR) do módulo de interface.

- Caso a compilação falhe, o Jenkins sinaliza erro, impedindo que alterações com problemas sejam mescladas ou implantadas.

Dessa forma, a integração com Jenkins garante que o código da interface Feign esteja sempre compilando corretamente antes de ser utilizado por outros microsserviços.
