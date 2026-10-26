# Morrow-database

The shared, public study material every Morrow user reads: the PrepForge
interview course under `course/` (System Design, DSA, Full-Stack, ML/GenAI,
behavioral), served as a docsify site.

Nothing personal lives here. A person's own profile, resume, answers, reports,
memory and research go in their private user repo (made from the
[Morrow-user](https://github.com/GuptaSoujanya/Morrow-user) template).

## How Morrow uses it

[Morrow](https://github.com/GuptaSoujanya/Morrow) clones this repo to
`database/` (or wherever `MORROW_DATABASE_DIR` in `.env` points) and reads
`database/course` through `COURSE_DIR`:

```bash
git clone https://github.com/GuptaSoujanya/Morrow-database.git database
# or let scripts/setup_user.sh do it together with your user repo
```

- The dashboard's **Study** section serves `course/` at `/course/` and tracks
  which modules you have read (that progress is written to your user repo, not
  here).
- `python3 -m pipeline` links the day's course modules into your learning notes.

Read the course on its own with `cd course && python3 serve.py 8000`.

## Contributing

Course content is Markdown with Mermaid diagrams and runnable code; see
`course/README.md`. Open a pull request against `main`.
