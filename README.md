# Hi, I'm Matis

Computer science engineering student, interested in **backend engineering, reliability (SRE)
and cloud infrastructure**. I like building systems that are tested, observable and easy to
run with one command.

[LinkedIn](https://www.linkedin.com/in/matis-di-piazza-19a375250) · [Email](mailto:dipiazzamatis@gmail.com)

## Featured project

### [AI SRE Assistant](https://github.com/matisdpz/ai-sre-assistant)

[![CI](https://github.com/matisdpz/ai-sre-assistant/actions/workflows/ci.yml/badge.svg)](https://github.com/matisdpz/ai-sre-assistant/actions/workflows/ci.yml)

A small incident management platform: a simulator generates metrics and failure scenarios
for a distributed system, the backend detects incidents with deterministic rules, and a
React dashboard tracks them from detection to resolution (MTTA, MTTR). An optional AI
assistant (Google Gemini) suggests hypotheses on request, kept separate from the facts
computed from the data.

[![AI SRE Assistant dashboard](https://raw.githubusercontent.com/matisdpz/ai-sre-assistant/main/docs/screenshots/overview.png)](https://github.com/matisdpz/ai-sre-assistant)

- **Detection engine** written as pure functions (no I/O, no clock), unit tested in isolation
- **Safe under concurrency**: row locks plus a partial unique index, so the same incident is
  never opened twice
- **Idempotent ingest API** with batch transactions, and a simulator that retries with
  exponential backoff
- **Hand-written Alembic migrations** checked for drift in CI
- **Optional AI with no hard dependency**: provider interface, clear errors on quota or
  timeout, and the app works fully without a key
- **One command to run**: Docker Compose (PostgreSQL, migrations, API, simulator, nginx)
- **CI on GitHub Actions**: lint, unit and integration tests on PostgreSQL 17, type check,
  frontend tests and Docker builds

`Python` `FastAPI` `SQLAlchemy` `PostgreSQL` `Alembic` `pytest` `React` `TypeScript`
`Docker Compose` `GitHub Actions` `Gemini API`

## Skills

- **Languages:** Python, Java, C/C++, SQL, TypeScript
- **Backend:** FastAPI, Pydantic, SQLAlchemy, REST API design, PostgreSQL
- **Infrastructure:** Docker, Docker Compose, nginx, GitHub Actions, Linux
- **Practices:** automated testing, database migrations, structured logging, code review
- **Learning:** cloud infrastructure, AI/ML
