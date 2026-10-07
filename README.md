# DevNest

**Showcase. Share. Connect.**

DevNest is a developer social and portfolio platform where developers
can showcase their work, share technical posts, and connect with others.

> Status: Foundation and database design. The features below are planned.

## Planned Features

- Email/password registration and Google sign-in.
- JWT access tokens with rotating refresh tokens.
- Developer profiles with bio, skills, experience, education, and social links.
- GitHub public repository integration with response caching.
- Posts, likes, and nested comments.
- Follow/unfollow and a personalised feed.
- Cursor-based feed pagination.
- Image uploads with client-side compression.
- Full-text search across users and posts.
- Client-side and server-side input validation.
- Rate limiting on write endpoints.

## Planned Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React, Tailwind CSS |
| Backend | Node.js, Express |
| Database | PostgreSQL |
| Authentication | JWT, bcrypt, Google OAuth |
| Image storage | Cloudinary |
| Validation | Zod |
| Code quality | ESLint, Prettier |
| Frontend deployment | Vercel |
| Backend deployment | Render or Railway; final choice pending |

## Planned Repository Structure

- client/: React application.
- server/: Express REST API.
- README.md: Project overview and setup instructions.
- SKILL.md: Decisions, evidence, measurements, bugs, and interview preparation.
- .env.example files: Required configuration without secrets.

## Build Order

1. Design the data model and document the database choice.
2. Scaffold client and server; configure ESLint, Prettier, and environment examples.
3. Complete authentication: register, login, refresh, logout, bcrypt hashing,
   access-token middleware, and Google sign-in.
4. Build profile CRUD APIs, then frontend forms with validation on both sides.
5. Add posts, comments, and likes with cursor-based pagination.
6. Integrate the GitHub REST API and cache responses.
7. Add image uploads, search, and rate limiting.
8. Test authentication and at least two API routes, then deploy and add live links.

## Database Design

PostgreSQL was selected because profiles, posts, comments, likes, and
follows have structured relationships.

Foreign keys and unique constraints will enforce rules such as valid
references, one profile per user, and no duplicate likes or follows.

The trade-off is that schema changes require migrations and related
data may require joins.

## Pagination Plan

The feed will use cursor-based pagination.

Offset pagination skips a specified number of records. Large offsets
can require more database work, and new posts can shift page boundaries.

Cursor pagination continues after an ordered record. The planned feed
ordering uses created_at and id together to provide a deterministic
tie-breaker.

The implementation and measured query results will be documented
after the feed is built.

## Getting Started

```bash
git clone https://github.com/Peeyush1-lab/DevNest.git
cd DevNest
```

The application is not runnable yet. Installation, database setup,
environment variables, and startup commands will be added during
scaffolding.

## Testing and Performance

Automated tests and benchmarks have not been implemented yet.

Planned validation includes:

- Authentication lifecycle and protected routes.
- At least two additional API routes.
- Invalid input and unauthorised requests.
- Duplicate likes and follows.
- Feed ordering and pagination.
- Feed-query measurements before and after relevant indexing.

All published metrics will come from actual measurements.

## Deployment

Deployment is pending.

- Frontend: Vercel.
- Backend: Render or Railway.
- Live URL: To be added after deployment.

## Current Limitations

- Core application features are not implemented.
- No public demo is available yet.
- Security, performance, and scalability have not been verified.

## Engineering Log

See [SKILL.md](./SKILL.md) for architecture decisions, trade-offs,
implementation evidence, measured results, and lessons from actual bugs.

## References and Credits

### Reference resources to explore

- [Project-Based Learning](https://github.com/practical-tutorials/project-based-learning)
- [App Ideas Collection](https://github.com/florinpop17/app-ideas)
- [RealWorld](https://github.com/gothinkster/realworld)
- [Public APIs](https://github.com/public-apis/public-apis)

### Resources used during implementation

None recorded yet.

As development progresses, this section will identify resources used,
what they helped with, and any code adapted from them.