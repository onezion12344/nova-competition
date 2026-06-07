# AGENTS.md — NOVA Competition Operation Manual

> **Purpose:** This file is read by Hermes Agent on every session in this directory.
> Both humans and AI agents use this to understand current progress, how to set up, and how to contribute.

---

## 1. What This Project Is

**NOVA: National AI Creativity Competition** — HKUST × Tencent Research Institute
- **Deadline:** June 30, 2026 (registration + proposal submission)
- **Team size:** 2–5 HK university students (can cross institutions)
- **Prize:** ¥100,000 RMB cash + WorkBuddy/CodeBuddy 1-year membership
- **Three tracks:** Social Impact | Creative Arts | Business Intelligence
- **Official:** https://ctbe.hkust.edu.hk/events/nova-national-ai-creativity-competition

## 2. Where Things Live

| What | Where |
|------|-------|
| **Local repo** | `~/nova-competition/` |
| **Notion team wiki** | [NOVA Team Wiki](https://notion.so/378d45f5ce6b81688efcee3be8cc24c0) |
| **Hermes session** | Telegram topic "Nova" (same group, same topic) |
| **Submission form** | https://ust.az1.qualtrics.com/jfe/form/SV_2aAH6lphN7C7QQC |

## 3. Git Workflow

```
main          ← stable, reviewed
├── feature/* ← one branch per feature/task
├── docs/*    ← documentation branches
└── submit    ← final submission prep
```

### Rules
- **Never commit directly to `main`** — always PR or merge from feature branch
- Branch naming: `feature/<what>`, `fix/<what>`, `docs/<what>`
- Commit messages: imperative, short (`Add bias analysis module`, not `Added bias analysis`)
- After finishing a feature, merge to `main` and delete the feature branch

### How agents work with Git
```bash
cd ~/nova-competition
git checkout -b feature/my-task
# ... do work ...
git add -A && git commit -m "Describe what was done"
git checkout main && git merge feature/my-task
```

## 4. How to Cooperate via Hermes

All team members share the **same Hermes session** (Telegram topic).
- Every message in this topic is visible to Hermes and all members
- When you start work, tell Hermes what you're doing — it tracks in the session
- Hermes can read this AGENTS.md to pick up the current state after context resets
- After any significant change, **update the Progress section below**

## 5. Progress Tracking

> **📌 UPDATE THIS after every work session. Agents: read this first.**

### Current Phase: Preparation / Ideation

| Item | Status | Notes |
|------|--------|-------|
| Track selection | 🔴 Not decided | |
| Team formation | 🔴 Not started | Need 2–5 members |
| Registration form | 🔴 Not submitted | |
| Project abstract | 🔴 Not started | |
| Slide deck | 🔴 Not started | |
| Intro video | 🔴 Not started | |
| AI prompts | 🔴 Not started | |

### Active Branches
| Branch | Purpose | Status |
|--------|---------|--------|
| `main` | Stable | Empty (initialized) |

### Recent Activity
- **2026-06-08:** Initialized repo, AGENTS.md, Notion Team Wiki (Local Setup, Git Workflow, Agent Manual, Progress Dashboard)

## 6. Branch Documentation Template

When creating a branch, document it in Notion and here:

```
## Branch: feature/<name>
- **Created:** YYYY-MM-DD
- **Purpose:** What this branch does
- **Files changed:** list
- **Status:** in-progress | merged | abandoned
- **Notes:** anything agents should know
```

## 7. Agent Quick Reference

When an agent opens this directory (via `workdir` or `cd`), always:
1. Read this AGENTS.md first
2. Check the Progress section for current state
3. Read the git log for recent changes: `git log --oneline -10`
4. Check active branches: `git branch -a`
5. Before making changes, create a feature branch
6. After changes, update the Progress section
7. Push if remote is configured

## 8. Environment

- **Python:** 3.11 (via uv)
- **Notion API:** configured (key in Keychain)
- **Git:** configured (user: Harry Onezion)
- **Hermes:** active in this Telegram topic
