---
framework_version: 1.0.0
---

# Agent Guidelines: AI-Job-Hunting Framework

This workspace is structured to manage comprehensive **AI-Job-Hunting** activities, scraper tools, LaTeX CVs, cover letters, and interview preparation across multi-agent environments.

## Thin-Pointer Design (Single Source of Truth)

To prevent duplication and configuration drift across different AI agent frameworks (Claude Code, Google Antigravity, OpenAI Codex, Cursor, Gemini CLI, etc.), the **AI-Job-Hunting** workspace utilizes a unified thin-pointer architecture. All agent runtimes should load the canonical specifications and candidate profiles from the single sources of truth below:

1. **Personal Candidate Profile:**
   - The candidate profile, contact details, education, and target preferences are defined in [CLAUDE.md](CLAUDE.md) and the individual profile methodology files under [.claude/skills/job-application-assistant/](.claude/skills/job-application-assistant/) (specifically `01-*.md` through `09-*.md`).
2. **Canonical Workflow Specifications:**
   - The step-by-step instructions and triggers for AI-Job-Hunting tasks (setup, scrape, rank, apply, upskill, interview, notion-sync, gmail-sync) are defined in the [.claude/](.claude/) directory (specifically under `.claude/skills/` and `.claude/commands/`).
   - Do not duplicate these rules or specifications. Treat `.claude/` files as the single source of truth.
3. **Portal Search Skills:**
   - Job-portal search CLIs live under [.agents/skills/](.agents/skills/) in the portable Agent Skills format (with a `SKILL.md` per portal). Codex and Antigravity discover these automatically; the `/scrape` workflow in [.claude/skills/job-scraper/](.claude/skills/job-scraper/) orchestrates them across multi-market job search batches.

