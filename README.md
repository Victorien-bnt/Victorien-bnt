<div align="center">

# Victorien Binant

**Applied AI Engineer · Founder of [Artisan'IA](https://artisan-ia.fr)**

I build and run production AI agents and business software for small companies. <br/>
Four business applications live with real users · everything I ship, I also operate.

[![Status](https://img.shields.io/badge/status-open_to_roles_in_Paris-2ea44f?style=flat-square)](mailto:binant.victorien@gmail.com)
[![Location](https://img.shields.io/badge/based_in-France_(CET)-1d4885?style=flat-square)](#)
[![Website](https://img.shields.io/badge/website-artisan--ia.fr-1d4885?style=flat-square)](https://artisan-ia.fr)
[![LinkedIn](https://img.shields.io/badge/linkedin-victorienbinant-0a66c2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/victorienbinant/)
[![Email](https://img.shields.io/badge/email-binant.victorien%40gmail.com-d14836?style=flat-square&logo=gmail&logoColor=white)](mailto:binant.victorien@gmail.com)

</div>

---

## 👋 In one paragraph

Engineer by training (ICAM Lille, MEng 2025), builder by practice. I run Artisan'IA, an independent practice serving artisans, food producers and small businesses in northern France. I take a business problem from framing to production and then I keep it running: I design the workflow with the client, write the application, deploy it on servers I administer myself, and I am the one they call when something breaks at 7am. Roughly half my work is LLM-based — document understanding, conversational agents over company data, automation of tasks people used to do by hand — and the other half is the plain software engineering that makes those useful: APIs, databases, interfaces, infrastructure.

I am currently looking for an **AI / GenAI Engineer position in Paris**, to do this at a larger scale and inside a team.

---

## 🚢 What I have shipped

| Project | What it does | Stage | Stack |
|---|---|:---:|---|
| **La Belle d'Armancourt** | Business ERP for an agricultural employers' group + supplier-invoice OCR pipeline with LLM extraction + conversational RAG agent over finance, treasury, HR and operations data | 🟢 Live | Python · FastAPI · Next.js · PostgreSQL · pgvector · Claude · OpenAI |
| **Mam'zelle Popinette** | Marketing site + business ERP + click-and-collect store + hours tracking, four systems that talk to each other | 🟢 Live | Node.js · TypeScript · PostgreSQL · Docker · n8n · Stripe |
| **CCE EDHEC** | Registration platform sized for 2,000 regatta participants: connection pooling, Redis cache, indexing, rate limiting | 🟢 Live | Next.js · PostgreSQL · Redis · Stripe |
| **Solar Billing** | Autonomous monthly billing pipeline, from the energy meter to the PDF invoice and its delivery | 🟢 Live | Python · Proxmox LXC · Docker · cron |
| **Vincesascie** | Offline-first PWA for forestry: 6 cubing methods, 9 packing strategies, 22 species, works in the forest with no signal | 🟢 Live | TypeScript · Service Workers |
| **Com au Quotidien** | Website and local SEO for a video studio | 🟢 Live | Static HTML · Tailwind |
| *Reusable agent library* | The parts of client work worth factoring out: invoice OCR, conversational data agent, automated dunning, billing scaffolds | 🟡 In dev | Python · Claude Agent SDK · n8n |

Case studies with scope, stack and trade-offs → **[artisan-ia.fr/realisations.html](https://artisan-ia.fr/realisations.html)**

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

**Pattern I keep shipping**: most recurring business processes decompose into 3–5 small AI primitives that a non-technical operator can chain themselves. The hard part is not the model. The hard part is designing the interface between primitives so the seams are obvious and the failure modes are loud.

---

## 🛠 Stack I ship with

**AI & agents** — Anthropic API · OpenAI API · Mistral · Gemini · Claude Code *(daily driver)* · Cursor · Claude Agent SDK · RAG pipelines · pgvector · LlamaCloud OCR · Cohere Rerank · structured outputs · prompt engineering

**Languages & runtimes** — Python · TypeScript · JavaScript · Node.js · SQL · Bash

**Web & data** — FastAPI · Next.js · React · Tailwind · PostgreSQL · Redis · Supabase · REST APIs

**Infrastructure I run myself** — six Debian servers in production (VPS + Proxmox hypervisor) · Docker & docker-compose · nginx reverse proxy & TLS · ufw · hardened SSH · backups · monitoring · incident recovery

**Integrations shipped against in production** — Stripe · Enable Banking (PSD2) · Factur-X / EN 16931 e-invoicing · Pennylane · SumUp · Cal.com · OVH · Home Assistant · Google Drive · WhatsApp Business · Telegram · n8n

---

## 🎯 How I work

**1. Smallest useful thing this week.** I would rather ship a thin slice the operator uses on Monday than the perfect system next quarter. Most of my client systems started as one small tool and grew from there.

**2. Build for the operator, not the engineer.** If the person who runs the business cannot extend or compose the tool, I have built the wrong thing. Half of every engagement is interface design.

**3. Loud failure modes.** AI systems that silently degrade are worse than ones that crash. Every pipeline I ship has explicit confidence thresholds, escalation paths and human review queues for the cases that should not be automated.

**4. Own the stack end-to-end.** Code, infrastructure, deployment, support. I would rather understand the full path than depend on a vendor I cannot debug.

---

## 🔭 Currently exploring

- **Evaluation for production LLM features** — moving from gut-check to measurable regression coverage on every prompt change: faithfulness, retrieval quality, cost and latency budgets.
- **Agent orchestration frameworks** — I currently call provider SDKs directly; I am working through LangGraph and LlamaIndex to see what they buy over hand-rolled orchestration.
- **Infrastructure as Code** — my deployments are bash and git today, which works at six servers and would not at sixty. Learning Ansible and Terraform.
- **Open source** — packaging the reusable parts of my client work into tools the community can actually use.

---

## 📈 Stats

<div align="center">

![Victorien's GitHub stats](https://github-readme-stats.vercel.app/api?username=Victorien-bnt&theme=transparent&hide_border=true&include_all_commits=true&count_private=true&hide=issues&show_icons=true&card_width=420)

![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Victorien-bnt&theme=transparent&hide_border=true&layout=compact&hide=html,css&langs_count=8&card_width=420)

</div>

> Most of my work lives in private client repositories. The contribution graph on my profile reflects that volume; the public repositories here are a small sample.

---

<div align="center">

### Open to AI / GenAI Engineer roles in Paris.

If you are building AI features that real people depend on, [I would love to talk](mailto:binant.victorien@gmail.com).

[![Email](https://img.shields.io/badge/binant.victorien%40gmail.com-d14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:binant.victorien@gmail.com)
[![Website](https://img.shields.io/badge/artisan--ia.fr-1d4885?style=for-the-badge&logo=safari&logoColor=white)](https://artisan-ia.fr)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/victorienbinant/)

</div>
