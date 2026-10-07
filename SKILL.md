# DevNest Engineering Log

## Project Details

| Field | Value |
|---|---|
| Project | DevNest |
| Track | Full Stack |
| Level | Beginner–Intermediate |
| Started | 2026-10-07 |
| Shipped | Not yet |
| Repository | [DevNest](https://github.com/Peeyush1-lab/DevNest) |
| Live URL | Not deployed yet |

## 1. What this project is

DevNest is a developer community platform where developers can create
profiles, showcase GitHub repositories, publish posts, and connect
with other developers.

The planned application uses a React frontend, an Express REST API,
and a PostgreSQL database.

## 2. Problem it solves

DevNest brings developer portfolios and technical discussions into
one place. Developers can present their work, discover projects,
and follow people whose work interests them.

## 3. Architecture

### Planned components

| Component | Responsibility |
|---|---|
| React and Tailwind CSS | User interface |
| Node.js and Express | REST APIs and application logic |
| PostgreSQL | Persistent data and relationship constraints |
| Google OAuth | Google sign-in |
| GitHub REST API | Public repository integration |
| Cloudinary | Image storage and delivery |

### Planned data relationships

- A user has one profile.
- A user can create many posts.
- A user can write many comments.
- A post can have many comments and likes.
- A comment can have replies through a parent comment relationship.
- A follow connects one user to another user.
- A user can have multiple refresh sessions.

The database diagram and implementation details will be added
after the data model is finalised.

## 4. Key decisions and trade-offs

| Decision | Options considered | Choice | Reason | Trade-off |
|---|---|---|---|---|
| Database | PostgreSQL, MongoDB | PostgreSQL | The platform has structured relationships; foreign keys and unique constraints support data integrity | Schema changes require migrations, and related data may require joins |
| Application structure | Integrated framework, separate client and server | React client and Express server | Learn explicit REST API design and separate responsibilities | Two applications to configure and deploy |

These are planned choices, not completed implementations.

## 5. Skills demonstrated

Check each item after implementing it and adding supporting evidence.

- [ ] REST API design and HTTP status code discipline
  - Evidence: Not recorded yet.

- [ ] JWT access/refresh token flow and why refresh tokens exist
  - Evidence: Not recorded yet.

- [ ] Database schema design and indexing
  - Evidence: Not recorded yet.

- [ ] Third-party API integration and caching
  - Evidence: Not recorded yet.

- [ ] File upload pipelines and CDN delivery
  - Evidence: Not recorded yet.

- [ ] Environment configuration and deployment
  - Evidence: Not recorded yet.

## 6. Numbers I measured

Not recorded yet.

| Metric | Before | After | How I measured it |
|---|---|---|---|
| — | — | — | — |

Record actual results, test conditions, and measurement tools.

## 7. Things that broke and how I fixed them

Not recorded yet.

For each actual issue, document:

- Symptom:
- Cause:
- Fix:
- Lesson:

## 8. What I would do differently at 100x scale

Not recorded yet.

Revisit this section after implementing the application and
measuring its bottlenecks.

## 9. Interview answers I have rehearsed

### Why use refresh tokens instead of one long-lived JWT?
Where would I store each token, and why?

Answer: Not recorded yet.

### How would I investigate a slow feed query?
What index would I add, and how would I verify the improvement?

Answer: Not recorded yet.

### How would I change the data model if a user could follow
10 million people?

Answer: Not recorded yet.

## 10. Honest limitations

- The project is currently in the foundation and design stage.
- Core application features are not implemented yet.
- No live deployment is available.
- Tests and performance measurements are pending.

Update this section as the project progresses.

## 11. How to run it

Repository: https://github.com/Peeyush1-lab/DevNest

The application is not runnable yet.

Installation commands, environment variables, database setup,
and startup instructions will be added after scaffolding.

## 12. Credits

### Reference resources to explore

- [Project-Based Learning](https://github.com/practical-tutorials/project-based-learning)
- [App Ideas Collection](https://github.com/florinpop17/app-ideas)
- [RealWorld](https://github.com/gothinkster/realworld)
- [Public APIs](https://github.com/public-apis/public-apis)

### Resources actually used

Not recorded yet.

For each resource used, record what it helped with and any code
adapted from it. Preserve applicable licenses and attribution.