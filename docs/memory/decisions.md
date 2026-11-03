# Decisions

Reasons marked (inferred) were not stated by the author.

- **Tutorial-style project** (first commit "tutorial project"; a later pull request from `codetobuild/dev` fixed the bearer-token condition). It follows the common Spring Boot 3 / Security 6 JWT pattern.
- **Stateless sessions:** no server session, the token carries the identity (inferred from the security config).
- **Auth endpoints are open, everything else is protected.** See [[architecture]].
