<div align="center">

# Victorien Binant

**Applied AI Engineer · Founder of [Artisan'IA](https://artisan-ia.fr)**

I ship production AI agents and modular Claude Skills for non-technical operators. <br/>
Seven products live · two in active development · zero clients still on Excel.

[![Status](https://img.shields.io/badge/status-open_to_remote_roles-2ea44f?style=flat-square)](mailto:binant.victorien@gmail.com)
[![Location](https://img.shields.io/badge/based_in-France_(CET)-1d4885?style=flat-square)](#)
[![Website](https://img.shields.io/badge/website-artisan--ia.fr-1d4885?style=flat-square)](https://artisan-ia.fr)
[![LinkedIn](https://img.shields.io/badge/linkedin-victorienbinant-0a66c2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/victorienbinant/)
[![Email](https://img.shields.io/badge/email-binant.victorien%40gmail.com-d14836?style=flat-square&logo=gmail&logoColor=white)](mailto:binant.victorien@gmail.com)

</div>

---

## 👋 In one paragraph

Engineer by training (ICAM Lille, MEng 2025), builder by practice. I run Artisan'IA, an independent AI consultancy serving artisans, food producers, and SMBs across northern France. Half my week is shipping autonomous agents and document-understanding pipelines; the other half is making those primitives small enough that the operator, not their IT department, owns the workflow. I work mostly inside [Claude Code](https://docs.claude.com/en/docs/claude-code), I ship through GitHub Actions, and I deploy on a VPS I can SSH into.

---

## 🚢 What I'm currently building

| Project | What it does | Stage | Stack |
|---|---|:---:|---|
| **[La Belle d'Armancourt](https://artisan-ia.fr/realisations/la-belle-armancourt.html)** | 11-tab pilot ERP + supplier-invoice OCR (LLM, ~99% on 893 docs) + conversational RAG agent over finance / treasury / HR / ops | 🟢 Live | Python · Next.js · Postgres · Claude · OpenAI · LangChain |
| **[Mam'zelle Popinette](https://artisan-ia.fr/realisations/mamzelle-popinette.html)** | Marketing site + 19-tab metier ERP + click-and-collect store, three systems that talk to each other | 🟢 Live | Node.js · n8n · Stripe · Pennylane |
| **[CCE EDHEC](https://artisan-ia.fr/realisations/cce-edhec.html)** | Inscription platform sized for 2,000 concurrent regatta participants | 🟢 Live | Next.js · Postgres · Stripe |
| **[Vincesascie](https://artisan-ia.fr/realisations/vincesascie.html)** | Offline-first PWA: 6 cubing methods, 9 packing strategies, 22 species, used in the forest with zero signal | 🟢 Live | TypeScript · Service Workers |
| **[Solar Billing](https://artisan-ia.fr/realisations/solar-billing.html)** | Fully autonomous monthly billing pipeline (Home Assistant meter → PDF → SMTP) | 🟢 Live | Python · cron · smtplib |
| **[Com au Quotidien](https://artisan-ia.fr/realisations/com-au-quotidien.html)** | Web refresh + local SEO for a video-craft studio | 🟢 Live | Static HTML · Tailwind |
| **[Gluten-Free.fr](https://artisan-ia.fr/realisations/gluten-free.html)** | Editorial media + Amazon affiliation, drafts validated in one tap via Telegram | 🟢 Live | Next.js · Claude · Telegram Bot API |
| *Internal Skills library* | Reusable Claude Skills factored out of client work: invoice OCR, conversational data agent, automated dunning, monthly billing scaffolds | 🟡 In dev | Claude Skills · n8n |
| *Multi-agent ops layer* | Orchestrating multiple agents across systems of record (CRM, accounting, payroll) with structured handoffs | 🟡 In dev | Claude Agent SDK · LangGraph |

Every case study has a public writeup with scope, stack, trade-offs, and what I would do differently → **[artisan-ia.fr/realisations](https://artisan-ia.fr/realisations.html)**

---

## 🧠 How I think about systems

```mermaid
flowchart LR
    subgraph SoR["Systems of record"]
        direction TB
        A1[Accounting]
        A2[Banking]
        A3[CRM]
        A4[Payroll]
        A5[Drive / Email]
    end

    subgraph Skills["Composable AI primitives"]
        direction TB
        S1[Document<br/>understanding]
        S2[Conversational<br/>RAG agent]
        S3[Autonomous<br/>action agent]
        S4[Reporting<br/>pipeline]
    end

    subgraph Users["Non-technical operator"]
        direction TB
        U1[Chains primitives<br/>into workflows]
        U2[Without filing<br/>engineering tickets]
    end

    SoR --> Skills --> Users

    classDef sor fill:#fff,stroke:#1d4885,stroke-width:1.5px,color:#1d4885
    classDef skills fill:#1d4885,stroke:#1d4885,color:#fff
    classDef users fill:#fff,stroke:#444,stroke-width:1.5px,color:#222
    class A1,A2,A3,A4,A5 sor
    class S1,S2,S3,S4 skills
    class U1,U2 users
```

**Pattern I keep shipping**: every recurring business process can be decomposed into 3–5 small AI primitives that a non-technical operator can chain themselves. The hard part is not the model. The hard part is designing the interface between primitives so the seams are obvious and the failure modes are loud.

---

## 🛠 Stack I ship with

**AI & agents** — Claude API · OpenAI API · Claude Code *(daily driver)* · Cursor · Claude Skills · Claude Agent SDK · RAG · LangChain · LangGraph · structured outputs · vector stores · evaluation pipelines

**Languages & runtimes** — Python · TypeScript · JavaScript · Node.js · SQL · Bash

**Web & data** — Next.js · React · Tailwind · PostgreSQL · Supabase · REST · GraphQL · Playwright

**Workflow & ops** — n8n · GitHub Actions · Docker · Nginx · VPS · cron · webhooks · SMTP

**Integrations shipped against in production** — Cal.com · Pennylane · Sumup · OVH · Home Assistant · Google Drive · WhatsApp Business · Telegram

---

## 🎯 How I work

**1. Smallest useful thing this week.** I would rather ship a thin slice that the operator uses on Monday than the perfect system in Q3. Most of my client systems started as one Claude Skill and grew from there.

**2. Build for the operator, not the engineer.** If the person who runs the business cannot extend or compose the tool, I have built the wrong thing. Half of every client engagement is interface design.

**3. Loud failure modes.** AI systems that silently degrade are worse than ones that crash. Every pipeline I ship has explicit confidence thresholds, escalation paths, and human review queues for the cases that should not be automated.

**4. Own the stack end-to-end.** Code, infra, deployment, observability, customer support. I would rather understand the full path than rely on a vendor I cannot debug.

---

## 🔭 Currently exploring

- **Claude Agent SDK** — patterns for multi-step agents that coordinate across SaaS systems of record without losing the audit trail.
- **Skill composition** — how do non-technical users author and chain Claude Skills when they have never seen YAML in their life?
- **Eval pipelines for prod LLM features** — moving from gut-check to measurable regression coverage on every prompt change.
- **Open-source contributions** — packaging the reusable parts of my client work into Skills the community can use.

---

## 📈 Stats

<div align="center">

![Victorien's GitHub stats](https://github-readme-stats.vercel.app/api?username=Victorien-bnt&theme=transparent&hide_border=true&include_all_commits=true&count_private=false&hide=issues&show_icons=true&card_width=420)
![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Victorien-bnt&theme=transparent&hide_border=true&layout=compact&hide=html,css&langs_count=8&card_width=420)

</div>

---

<div align="center">

### Open to remote Applied AI / AI Engineering roles, US or EU.

If you are building AI-native operating layers for non-technical teams, [I would love to talk](mailto:binant.victorien@gmail.com).

[![Email](https://img.shields.io/badge/binant.victorien%40gmail.com-d14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:binant.victorien@gmail.com)
[![Website](https://img.shields.io/badge/artisan--ia.fr-1d4885?style=for-the-badge&logo=safari&logoColor=white)](https://artisan-ia.fr)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/victorienbinant/)

</div>
