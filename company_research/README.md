# AI-Job-Hunting: Company Research Cache

This directory stores intelligence dossiers and cached research on target employers analyzed by the **AI-Job-Hunting** assistant.

## Purpose & Workflow Integration

During the application and interview workflows (`/apply` and `/interview`), AI-Job-Hunting conducts structured company research to enrich cover letters and interview talking points:

1. **Strategic Priorities**: Mission, core products, revenue models, key public engineering or business initiatives.
2. **Culture & Values**: Engineering culture, workplace norms, leadership principles, and team dynamics.
3. **News & Milestones**: Recent funding rounds, product launches, acquisitions, or industry shifts.
4. **Interview Intelligence**: Common interview questions, technical interview patterns, and thoughtful candidate questions for the interviewers.

## Cache File Conventions

Cached research files are named by company slug:
- `<company_slug>.json` (e.g., `novo-nordisk.json`, `maersk.json`)

Cached entries prevent redundant web searches across multiple applications and interview preparation sessions while keeping your context window focused. All cached `.json` files in this directory are git-ignored by default for privacy.
