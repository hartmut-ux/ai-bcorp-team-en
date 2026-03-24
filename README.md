# B Corp Navigator — AI B Corp Team

> 10 AI agents for B Corp certification and ongoing reporting under B Lab Standards V2.2

[![B Lab Standards](https://img.shields.io/badge/B_Lab_Standards-V2.2_(Feb_2026)-green)](https://www.bcorporation.net)
[![Skills](https://img.shields.io/badge/Skills-10-blue)]()
[![Licence](https://img.shields.io/badge/Licence-MIT-yellow)](LICENSE)
[![Claude](https://img.shields.io/badge/Claude-Skills-blueviolet)](https://claude.ai)

---

## The Problem

The B Lab Standards V2.2 span **1,245 pages** across 8 requirement areas, with a phased approach (Year 0/3/5) and tailoring by company size, sector and industry. For SMEs, this complexity is a major barrier — both for initial certification and ongoing reporting.

## The Solution

10 specialised AI agents (Claude Skills) that serve as a **virtual B Corp team**, guiding companies through the entire certification journey — from eligibility checks to annual impact reports.

## The 10 Skills

| # | Skill | Function | B Lab Requirements |
|---|-------|----------|-------------------|
| 1 | [Certification Navigator](skills/certification-navigator/) | Overall coordination, eligibility, roadmap | FR1, FR2, FR3 |
| 2 | [Governance & Purpose Architect](skills/governance-purpose-architect/) | Corporate purpose, stakeholder governance | PSG1–PSG6 |
| 3 | [Fair Work Analyst](skills/fair-work-analyst/) | Living wage, employment standards, culture | FW1–FW4 |
| 4 | [JEDI Strategist](skills/jedi-strategist/) | Diversity, equity, inclusion | JEDI1–JEDI2 |
| 5 | [Human Rights Due Diligence](skills/human-rights-due-diligence/) | Human rights due diligence | HR1–HR4 |
| 6 | [Climate Action Planner](skills/climate-action-planner/) | GHG measurement, SBTi, transition plans | CA1–CA3 |
| 7 | [Environmental Stewardship Manager](skills/environmental-stewardship-manager/) | Circularity, biodiversity | ESC1–ESC5 |
| 8 | [Public Affairs & Collective Action](skills/public-affairs-collective-action/) | Lobbying, taxes, collective impact | GACA1–GACA3 |
| 9 | [Impact Reporter](skills/impact-reporter/) | Annual reports, GRI/ESRS mapping | PSG6 + cross-cutting |
| 10 | [Compliance Monitor](skills/compliance-monitor/) | Gap analysis, deadlines, audit preparation | All |

## Architecture

```
┌─────────────────────────────────────────────────────┐
│             CERTIFICATION NAVIGATOR                  │
│          (Coordination · Roadmap · Tailoring)        │
├─────────────────────────────────────────────────────┤
│                                                     │
│  Governance &    Fair Work     JEDI       Human     │
│  Purpose         Analyst       Strategist Rights    │
│  Architect                                DD        │
│                                                     │
│  Climate Action  Environmental  Public Affairs      │
│  Planner         Stewardship    & Collective        │
│                  Manager        Action              │
│                                                     │
├─────────────────────────────────────────────────────┤
│  IMPACT REPORTER          COMPLIANCE MONITOR        │
│  (Reporting · GRI · ESRS)  (Gap Analysis · Audit)   │
└─────────────────────────────────────────────────────┘
```

**Three layers:**
1. **Certification Navigator** — Steers the certification journey (top)
2. **7 Impact Topic Skills** — One agent per impact area (middle)
3. **Impact Reporter + Compliance Monitor** — Cross-cutting functions (bottom)

## Phased Approach

The skills mirror the B Lab phased approach:

| Phase | Timeframe | Focus |
|-------|-----------|-------|
| **Year 0** | Initial certification | Foundation Requirements + all Year 0 sub-requirements |
| **Year 3** | Deepening | Additional Year 3 sub-requirements (e.g. climate transition plan) |
| **Year 5** | Excellence | Full compliance with all B Lab Standards |

## Technology

| Component | Technology |
|-----------|-----------|
| AI Model | [Claude](https://claude.ai) Sonnet 4.6 (Anthropic) |
| Agent Protocol | [MCP](https://modelcontextprotocol.io) (Model Context Protocol, Linux Foundation) |
| FAQ Agent | [Dify](https://dify.ai) (Self-hosted, RAG on B Lab Standards V2.2) |
| Automation | [n8n](https://n8n.io) (Self-hosted, Workflow Automation) |
| Skill Format | `.skill` ZIP archives for Claude Desktop |
| Hosting | Hostinger VPS, Server Location Frankfurt/Main, Germany (GDPR compliant) |

## Live Demo

🔗 **B Corp Navigator FAQ** — [https://dify.huebner.io/chat/QExMsxb1mzs2bbLO](https://dify.huebner.io/chat/QExMsxb1mzs2bbLO)
Chatbot powered by the complete B Lab Standards V2.2, self-hosted on European infrastructure (Frankfurt/Main, Germany).

## Who Is This For?

- **SMEs** pursuing B Corp certification for the first time
- **Existing B Corps** looking to streamline ongoing reporting
- **B Corp consultants** seeking AI-powered tools for their clients
- **Sustainability managers** running B Corp alongside GRI/ESRS/CDP

## Interoperability

The skills reference and complement existing standards:

- **GRI** (Global Reporting Initiative)
- **ESRS** (European Sustainability Reporting Standards)
- **CDP** (Climate Disclosure Platform)
- **SBTi** (Science Based Targets initiative)
- **UNGP** (UN Guiding Principles on Business and Human Rights)
- **ISO Standards** (Governance, Net Zero Guidelines)
- **ILO** (Labour rights and standards)

## Installation

```bash
# Clone the repository
git clone https://github.com/hartmut-ux/ai-bcorp-team-en.git

# Load skills into Claude Desktop
# Import each skill folder as a .skill ZIP archive
```

## Licence

MIT Licence — Free for commercial and non-commercial use.

## About the Author

**Hartmut Hübner, PhD** combines 20 years of corporate communications in large enterprises (Siemens, financial services) with 10 years of experience in transformation, digitalisation and AI. Co-founder of several startups, including MMIND.ai. Academic background at LMU Munich and PhD from the University of Salford (thesis: *The Communicating Company*). Certified B Corp Consultant.

- 🌐 [mmind.ai](https://mmind.ai) · [MMIND.ai Marketplace](https://mmind.ai/marketplace)
- 💼 [LinkedIn](https://linkedin.com/in/hartmutplass)
- 🐙 [GitHub](https://github.com/hartmut-ux)

---

*Based on B Lab Standards V2.2 (February 2026) · Built with Claude (Anthropic)*
