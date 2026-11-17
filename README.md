# CSE 3107 — Computer Architecture Course Hub

A course-resource website for **CSE 3107: Computer Architecture (20 Series)**, inspired by Stanford’s CS143 course-site layout.

## What is implemented

A Django homepage with a course overview, lecture topics, textbook/slide links, resources and handouts. Some assignment and course-information links remain placeholders in the original page.

## Local setup

```powershell
python -m venv .venv
.venv\Scripts\python -m pip install -r requirements.txt
.venv\Scripts\python manage.py migrate
.venv\Scripts\python manage.py runserver
```

Open http://127.0.0.1:8000. On Linux/macOS, use `.venv/bin/python` in place of `.venv\Scripts\python`.

## Source map

- `core/views.py`: homepage view.
- `core/templates/core/home.html`: course page.
- `cse3107_website/`: project settings and URLs.
- `Procfile`: deployment process definition.

The existing dependency files are retained. `node_modules` is no longer tracked; use the package lockfile if the frontend tooling is needed. The Django homepage itself is rendered from the HTML template.

## Check

```bash
python manage.py check
```

Setup instructions describe the existing project; this documentation update did not upgrade dependencies or certify production readiness.
