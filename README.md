# AI Resume Screening System
### Automated Hiring Pipeline — From Application to AI-Scored Report

> **Built once. Used forever.** — Built by [JeRoy | The Instructional Architect](https://linkedin.com/in/jerryogahroy)

---

## Overview

The AI Resume Screening System eliminates the bottleneck of manual CV review. It accepts job applications through a web form, extracts and processes each resume using AI, evaluates the candidate against a stored job description, and logs a structured hiring report — all without human involvement in the initial review stage.

**Category:** HR / Talent Acquisition
**Platform:** n8n + OpenAI + Google Drive + Gmail + Notion
**Size:** Large (8 tasks)
**Version:** v1.0

---

## The Problem

For most companies, the moment a job posting goes live, an inbox begins filling with PDF resumes — each requiring a recruiter to open, read, evaluate, and make a judgment call. At scale, this process is slow, inconsistent, and expensive.

---

## How It Works

| Step | Action |
|------|--------|
| Trigger | Applicant submits web form (name, email, phone, resume PDF) |
| Step 1 | Resume PDF uploaded to Google Drive |
| Step 2 | File downloaded back into workflow for processing |
| Step 3 | PDF text extracted from resume |
| Step 4 | Job description PDF fetched from Drive |
| Step 5 | Job description text extracted |
| Step 6 | GPT-4.1-mini evaluates candidate vs. job description |
| Step 7 | Confirmation email sent to applicant via Gmail |
| Step 8 | Structured report logged to Notion database |

**AI Output per candidate:** Strengths, Weaknesses, Risk Factor, Reward Factor, Overall Fit Rating (0–10), and Justification.

---

## Demo

📹 [Watch the Demo Video](https://drive.google.com/file/d/1scAMGQsG_PJRBQULIStiRAYiK2rIiEBB/view?usp=drive_link)

---

## Tools Required

| Tool | Purpose | Cost |
|------|---------|------|
| n8n | Workflow automation | Free / $20+/mo |
| OpenAI GPT-4.1-mini | AI evaluation | Pay-per-use (~$0.01–0.05/run) |
| Google Drive | Resume & JD storage | Free |
| Gmail | Applicant confirmation emails | Free |
| Notion | Applicant tracking database | Free / $8+/mo |

---

## Setup Requirements

- n8n instance (self-hosted or cloud)
- OpenAI API key with GPT-4.1-mini access
- Google Drive OAuth2 credentials in n8n
- Gmail OAuth2 credentials in n8n
- Notion API token + configured database with required properties
- Job description PDF uploaded to Google Drive (file ID configured in workflow)

---

## Deployment Time

| Scenario | Time |
|----------|------|
| Without customization | 2–4 hours |
| With customization | 2–5 days |

---

## Value Proposition

| Metric | Value |
|--------|-------|
| Manual screening time (50 apps) | ~5.8 hours |
| Automated screening time | < 60 seconds |
| Labor cost saved per role | ~$113 |
| Monthly savings (2 roles/month) | ~$226/month |

---

## Pricing

| Model | Price |
|-------|-------|
| Productized | $500–$800 |
| One-Time Project | $1,500–$3,000 |
| Retainer | $500–$800/month |

---

## Known Limitations

- Supports PDF resumes only (DOCX requires additional nodes)
- One job description per workflow instance
- OpenAI API usage billed per token at scale
- AI evaluation quality depends on clarity of the job description

---

## Repo Structure

```
ai-resume-screening-system/
├── workflow/        # n8n JSON workflow file
├── screenshots/     # Workflow screenshots
├── demo/            # Demo video link
└── README.md
```

---

## Version History

| Version | Notes |
|---------|-------|
| v1.0 | Initial release — Form, Drive, GPT-4.1-mini, Gmail, Notion |
| Planned | Multi-role routing, DOCX support, Slack alerts for high-fit candidates |

---

*Built by [JeRoy | The Instructional Architect](https://linkedin.com/in/jerryogahroy) — Complex in. Simple out.*
