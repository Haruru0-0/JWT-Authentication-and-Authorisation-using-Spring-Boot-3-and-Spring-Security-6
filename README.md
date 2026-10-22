# JWT Authentication and Authorisation with Spring Boot 3 and Spring Security 6

A stateless REST API that registers users, authenticates them and protects endpoints with JSON Web Tokens.

## Stack

- Java 17, Spring Boot 3.0.2, Spring Security 6
- Spring Data JPA with PostgreSQL
- jjwt 0.11.5 for signing and parsing tokens
- Lombok, Maven

## How it works

- `POST /api/v1/auth/register` creates a user and returns a JWT.
- `POST /api/v1/auth/authenticate` checks credentials and returns a JWT.
- `JwtAuthenticationFilter` reads the `Authorization: Bearer <token>` header on every request and sets the security context.
- Every other endpoint, such as the demo controller, requires a valid token.
- Users have a `Role` (`USER` or `ADMIN`) used for authorisation.

## Run it

1. Create a PostgreSQL database named `jwt_security` (the defaults are in `src/main/resources/application.yml`; change the credentials to match your setup).
2. Start the API:

```bash
./mvnw spring-boot:run
```