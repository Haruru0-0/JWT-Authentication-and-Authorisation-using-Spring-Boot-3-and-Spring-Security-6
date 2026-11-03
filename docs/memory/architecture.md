# Architecture

See [[features-built]] for behaviour and [[gotchas]] for traps.

Stateless REST API. Java 17, Spring Boot 3.0.2, Spring Security 6, Spring Data JPA with PostgreSQL, jjwt 0.11.5, Lombok, Maven (wrapper included). Package root `src/main/java/com/example/security/`.

- `auth/`: `AuthenticationController` (register and authenticate), `AuthenticationService`, request and response DTOs.
- `config/`: `SecurityConfiguration` (stateless session; `/api/v1/auth/**` is public, every other request needs authentication), `JwtAuthenticationFilter` (reads `Authorization: Bearer <token>` on each request and sets the security context), `JwtService` (signs and parses tokens), `ApplicationConfig`.
- `user/`: `User`, `Role` (`USER` or `ADMIN`), `UserRepository`.
- `demo/DemoController`: a protected endpoint used to try the token.
- `src/main/resources/application.yml`: PostgreSQL at `localhost:5432/jwt_security`, Hibernate `ddl-auto: create-drop`.
