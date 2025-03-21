🔧 **Configurando o Banco de Dados H2 com Spring Boot** 🚀

Se você está desenvolvendo uma aplicação com **Java** e **Spring Boot** e precisa de uma solução rápida para testes ou desenvolvimento, o **H2** é uma ótima opção! Ele é leve, rápido e fácil de configurar.

Aqui está um passo a passo para configurar o **H2** no seu projeto Spring Boot:

### 1️⃣ **Adicione a dependência no `pom.xml`** (para Maven):

```xml
<dependency>
    <groupId>com.h2database</groupId>
    <artifactId>h2</artifactId>
    <version>2.1.214</version>
    <scope>runtime</scope>
</dependency>
```

### 2️⃣ **Configuração no `application.properties`**:

No arquivo `src/main/resources/application.properties`, adicione as configurações do banco H2:

```properties
# Configuração do H2 Database (banco em memória)

spring.datasource.url=jdbc:h2:mem:todolist
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect

# Habilitar o console do H2 (opcional)
spring.h2.console.enabled=true

# Mostrar o SQL no console
spring.jpa.show-sql=true

# Criar ou atualizar o banco de dados automaticamente
spring.jpa.hibernate.ddl-auto=update

```

- `jdbc:h2:mem:testdb`: Configuração para o banco em memória.
- `spring.jpa.hibernate.ddl-auto=update`: Atualiza o schema automaticamente.
- `spring.h2.console.enabled=true`: Ativa o console H2 para consultas no navegador.

### 3️⃣ **Acesse o console H2**:  
Com a aplicação rodando, você pode acessar o console H2 diretamente no navegador:

[http://localhost:8080/h2-console](http://localhost:8080/h2-console)

- URL JDBC: `jdbc:h2:mem:testdb`
- Usuário: `sa`
- Senha: ` `

🔹 **Vantagens do H2**:
- Banco de dados **leve** e **rápido**.
- **Ideal para testes e desenvolvimento**.
- Fácil **integração com Spring Boot**.

Com esses passos, você tem um banco de dados H2 funcionando rapidamente no seu projeto Spring Boot. Ideal para testar e desenvolver sem complicação!

Tem alguma dúvida ou quer compartilhar sua experiência com o H2? Comente abaixo! 👇

#H2 #SpringBoot #Java #BancoDeDados #Desenvolvimento #Tecnologia
