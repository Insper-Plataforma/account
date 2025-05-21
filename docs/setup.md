# Setup e dependências

Este módulo depende do seguinte:

- Spring Cloud OpenFeign
- Spring Boot
- Integração com o microsserviço `account` rodando na porta `8080`

---

## Como compilar

```bash
mvn clean install
```

---

## Como rodar

Este é um módulo de interface, portanto não roda isoladamente. Deve ser usado em um projeto que consome esta interface Feign.

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