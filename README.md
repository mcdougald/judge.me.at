<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="judge.me.at landing page" width="880">
  </picture>
</p>

<h1 align="center">judge.me.at</h1>

<p align="center"><strong>AI-assisted case workspaces for law practices.</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/status-in%20development-171717?style=flat-square" alt="Status: in development">
  <img src="https://img.shields.io/badge/license-source--available-404040?style=flat-square" alt="License: source-available">
  <img src="https://img.shields.io/badge/part%20of-me.at-737373?style=flat-square" alt="Part of me.at">
</p>

<p align="center">
  <a href="#features">Features</a> ·
  <a href="#how-it-works">How it works</a> ·
  <a href="#built-with">Built with</a>
</p>

A small practice cannot afford an AI tool that leaks privileged documents or cites a case that does not exist. I built judge.me.at to keep a practice's matters and documents organised, find the relevant documents and court records for a question, and review a case file with you. It joins public court-record integrations with a firm's own files behind privilege, PII, provenance and rate-budget safeguards. Every citation it shows must be checked against a real opinion first, and one that cannot be confirmed is quarantined and marked, never presented as verified.

> **Status:** in development. The matter dashboard works today, and the AI features have not yet run against a connected model. Nothing here is legal advice.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/overview-dark.svg">
    <img src=".github/assets/overview.svg" alt="judge.me.at at a glance: a wall around each matter, privilege stays out, citations must verify, bound to the record" width="880">
  </picture>
</p>

## Why judge.me.at

| The usual AI legal assistant | judge.me.at |
| --- | --- |
| Shows citations as it generated them | Quarantines any citation it cannot verify |
| Reads every document you upload | Keeps privileged text out unless an attorney names it for the run |
| Answers from general knowledge | Drafts only from passages retrieved from the matter, or refuses |
| Computes deadlines from procedural rules | Uses only court-supplied or user-entered dates |

## Features

- **A matter dashboard, behind sign-in**: firms, clients, matters, calendar dates and a document archive searchable by words and tags.
- **A wall around each matter**: a matter is readable only by the people on its access list, and archive search applies that list inside the query.
- **Privilege-aware documents**: a privileged document's text never reaches the search index, and stays out of any AI run unless an attorney names it for that run.
- **Citation checking with quarantine**: citations are extracted from generated text and must verify before they render as verified, tested against deliberately fake citations.
- **Deadlines from the court or from you**: a calendar date is court-supplied or user-entered. Computing one from a procedural rule is refused.
- **Opinion search, scoped to a matter**: case law search runs inside a matter the caller may read, against a daily request budget.
- **Answers bound to the record**: drafts (chronology, outline, summary, timeline) must rest on passages retrieved from the matter, and refuse rather than guess.

## How it works

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/flow-dark.svg">
    <img src=".github/assets/flow.svg" alt="How judge.me.at works: open, retrieve, draft, verify, mark" width="880">
  </picture>
</p>

Everything starts inside a matter, readable only by the people on its access list. A question retrieves passages from that matter, with privileged text left out unless an attorney names it, and a draft must rest on those passages or refuse. Every citation in the draft is then checked against a real opinion, and any that cannot be confirmed is quarantined and marked rather than shown as verified.

## Built with

<p>
  <img src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js 16">
  <img src="https://img.shields.io/badge/React-19-171717?style=flat-square&logo=react&logoColor=white" alt="React 19">
  <img src="https://img.shields.io/badge/TypeScript-5-262626?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind%20CSS-4-404040?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS 4">
  <img src="https://img.shields.io/badge/Drizzle-Postgres-525252?style=flat-square&logo=drizzle&logoColor=white" alt="Drizzle ORM and Postgres">
</p>

- Next.js 16 (App Router), React 19, TypeScript
- Tailwind CSS 4
- oRPC for the typed API
- Drizzle ORM + Postgres
- Better Auth (the shared me.at account)

## Part of the me.at family

judge.me.at is one of my [`*.me.at`](https://me.at) apps. They share one design system, account, and app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

Source-available. See [LICENSE](LICENSE).
