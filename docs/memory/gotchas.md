# Gotchas

See [[architecture]].

- **`ddl-auto: create-drop` wipes the tables each time the app stops.** Users do not survive a restart.
- **Needs PostgreSQL first:** create a database named `jwt_security` and match the username and password in `application.yml` (the committed file has the author's local credentials; change them for your setup).
- **Run with `./mvnw spring-boot:run`** (Maven wrapper; no global Maven needed).
- **No automated tests beyond the default context-load test** (`SecurityApplicationTests`).
- **`graphify.exe` is blocked on this machine;** use `python -m graphify update .`.
