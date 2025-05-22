# Setup e dependências

Este módulo define apenas a **interface REST `AccountController`** e os DTOs relacionados.

---

## Como compilar

```bash
mvn clean install
```

---

## Como usar

Este módulo é usado como **dependência em `account-service`**, que implementa de fato a interface.

Certifique-se de importar o pacote corretamente ao implementar:

```java
@RestController
public class AccountResource implements AccountController {
    // ...
}
```

---

## Requisitos

Requisitos no arquivo `pom.xml`:

```xml
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-openfeign</artifactId>
</dependency>
```

E ativar o Feign Client no seu projeto:

```java
@SpringBootApplication
@EnableFeignClients(basePackages = "store.account")
```
---