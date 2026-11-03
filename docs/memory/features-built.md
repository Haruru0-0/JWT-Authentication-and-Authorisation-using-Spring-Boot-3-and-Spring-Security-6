# Features built

Structure: [[architecture]].

- `POST /api/v1/auth/register` creates a user and returns a JWT.
- `POST /api/v1/auth/authenticate` checks credentials and returns a JWT.
- A filter validates the bearer token on every request; all other endpoints, including the demo controller, require a valid token.
- Users have a role (`USER` or `ADMIN`) for authorisation.
- README (added later) explains the stack and how to run it. GitHub Actions mirrors the repo to GitLab on every push.
