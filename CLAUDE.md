# JWT auth demo

Stateless REST API with registration, authentication and JWT-protected endpoints. Spring Boot 3.0.2, Spring Security 6, PostgreSQL. See `README.md`.

## Commands
- `./mvnw spring-boot:run`: start the API (needs PostgreSQL with a `jwt_security` database).
- `./mvnw test`: run the tests.

## Conventions
- Default branch is `main`. Commit messages are plain, with no `Co-Authored-By` trailer.
- Keep `/api/v1/auth/**` public and everything else authenticated unless told otherwise.

## Memory and code map
- At session start read `docs/memory/index.md`. Save durable decisions there as Markdown.
- `graphify-out/GRAPH_REPORT.md` summarizes code structure; refresh with `python -m graphify update .` (the `.exe` is blocked on this machine).
