# Job Search Tracker

A full-time job search tracker: application pipeline, status breakdown chart, and an AI assist tab that tailors resume bullets and a cover letter from a dropped-in resume PDF and a job posting link.

## Stack
- Single-file static app (`index.html`) — no build step
- [Supabase](https://supabase.com) (Postgres) for storage — applications and resume text are stored in the `job_tracker_applications` and `job_tracker_resume` tables
- [pdf.js](https://mozilla.github.io/pdf.js/) for client-side PDF text extraction
- Claude API (with web search) for tailoring resume bullets and cover letters

## Running it
Just open `index.html` in a browser, or serve the folder statically (e.g. GitHub Pages).

## Data
This app has no login — it uses a public Supabase anon key with permissive row-level-security policies, intended for single-user personal use. Don't reuse these tables for anything containing other people's data.
