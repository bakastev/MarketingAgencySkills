# 🏢 Marketing Agency Skills

A collection of OpenAI/Agent-ready skill files for running a modern marketing agency with AI. Built by and for [Growing Brands](https://www.growing-brands.de).

## Structure

```
MarketingAgencySkills/
├── cmo/                          # Chief Marketing Officer (Orchestrator)
│   └── SKILL.md
├── ops/                          # Operations & Automation
│   └── onboarding-agent/         # 6-Phase Customer Onboarding ✅
├── strategy/                     # Strategy & Research
│   └── customer-avatar/          # Deep Customer Avatar Architect ✅
├── brand/                        # Branding
│   └── brand-architect/          # Evidence-Based Brand Strategy ✅
├── ads/                          # Paid Advertising
│   ├── ad-angles-hooks-architect/ # Ad Angles & Hooks Generator ✅
│   └── ads-strategist/
├── content/                      # Content Creation
│   └── vsl-architect/            # Video Sales Letter Architect ✅
├── seo/                          # Search Engine Optimization
│   ├── aio-geo-goldstandard/     # AIO / GEO / AEO page + markup QA ✅
│   └── seo-specialist/
├── sales/                        # Sales Enablement
│   ├── landing-page-creator/     # High-Ticket Landing Page Creator ✅
│   └── lead-magnet-creator/      # Lead Magnet Creator (10 Sections) ✅
├── social/                       # Social Media
├── analytics/                    # Analytics & Reporting
└── ops/                          # Operations & Automation
    └── ops-automation/
```

## How It Works

### The CMO (Orchestrator)

The `cmo/SKILL.md` is the top-level orchestrator. It receives requests, identifies which specialist skill to invoke, checks dependencies (e.g. no messaging without an avatar), and ensures consistency across all outputs.

**Agency Pipeline:** `Lead → Onboarding → Avatar → Brand → Angles & Hooks → VSL → Landing Page → Lead Magnet → Content → Ads → SEO → Analytics`

### Specialist Skills

Each skill is self-contained in its own folder with a `SKILL.md` file containing:

- **Purpose** — What the skill does
- **Core Principles** — Guiding rules
- **Workflow** — Step-by-step process
- **Output Format** — Structured output template
- **Guardrails** — What to avoid

### Current Skills

| Skill | Discipline | Status | Lines |
|---|---|---|---|
| **Customer Onboarding Agent** | Operations | ✅ Active | 186 |
| **Customer Avatar Architect** | Strategy/Research | ✅ Active | 459 |
| **Brand Architect** | Branding | ✅ Active | 590 |
| **Ad Angles & Hooks Architect** | Paid Media | ✅ Active | 285 |
| **VSL Architect** | Content | ✅ Active | 789 |
| **Landing Page Creator** | Sales | ✅ Active | 1,314 |
| **Lead Magnet Creator** | Sales | ✅ Active | 1,667 |
| **AIO / GEO / AEO Gold Standard** | SEO (AI visibility) | ✅ Active | 90 |
| Content Strategist | Content | 🔜 Planned | — |
| SEO Specialist | SEO | 🔜 Planned | — |
| Ads Strategist | Paid Media | 🔜 Planned | — |
| Social Media Manager | Social | 🔜 Planned | — |
| Analytics Lead | Analytics | 🔜 Planned | — |
| Sales Enablement | Sales | 🔜 Planned | — |
| Ops Automation | Operations | 🔜 Planned | — |

**Total active skill content: ~4,380 lines**

## Usage

These skills are designed to work with any agent framework that supports skill files (OpenClaw, Claude, GPT, etc.). Each `SKILL.md` can be used as a system prompt or imported into your agent's context.

1. Pick the skill you need
2. Provide the required inputs (customer data, brief, etc.)
3. The skill follows its workflow and produces structured output

## Contributing

Contributions welcome! Please:

1. Follow the existing folder structure
2. Each skill gets its own folder with a `SKILL.md`
3. Include purpose, principles, workflow, output format, and guardrails
4. Keep skills language-agnostic where possible
5. Submit a PR

## License

MIT — use freely, attribution appreciated.

---

*[Growing Brands](https://www.growing-brands.de) © 2026*
