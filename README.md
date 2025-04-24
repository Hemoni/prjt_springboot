# Como Rodar o Projeto
### Dependencias

Java 17+ instalado

Maven instalado

MariaDB rodando (pode ser via XAMPP, Docker, etc.)

VS Code ou qualquer IDE Java

Postman ou Bruno (para testar)

### Crie o banco via MariaDB

CREATE DATABASE escola;

### Atualize o arquivo src/main/resources/application.properties com

spring.datasource.url=jdbc:mariadb://localhost:3306/escola
spring.datasource.username=root
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update

---

### Rode a Aplicação

mvn spring-boot:run

A API está disponível em http://localhost:8080

---

### Testando com Postman

GET /alunos → Lista alunos
POST /alunos → Cria aluno

```
{
  "nome": "João",
  "cursos": [{"id": 1}]
}
```

PUT /alunos/{id} → Atualiza aluno

DELETE /alunos/{id} → Deleta aluno

---

### Cursos

GET /cursos → Lista cursos
POST /cursos → Cria curso

{
  "nome": "Matemática"
}
