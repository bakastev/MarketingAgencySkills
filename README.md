# 🏢 Marketing Agency Skills

A collection of OpenAI/Agent-ready skill files for running a modern marketing agency with AI. Built by and for [Growing Brands](https://www.growing-brands.de).

## Structure

```
MarketingAgencySkills/
├── cmo/                          # Chief Marketing Officer (Orchestrator)
│   └── SKILL.md
├── strategy/                     # Strategy & Research
│   └── customer-avatar/          # Deep Customer Avatar Architect ✅
├── brand/                        # Branding
├── content/                      # Content Creation
├── seo/                          # Search Engine Optimization
│   ├── aio-geo-goldstandard/     # AIO / GEO / AEO page + markup QA ✅
│   └── seo-specialist/
├── ads/                          # Paid Advertising
├── social/                       # Social Media
├── analytics/                    # Analytics & Reporting
├── sales/                        # Sales Enablement
└── ops/                          # Operations & Automation
```

## How It Works

### The CMO (Orchestrator)

The `cmo/SKILL.md` is the top-level orchestrator. It receives requests, identifies which specialist skill to invoke, checks dependencies (e.g. no messaging without an avatar), and ensures consistency across all outputs.

**Standard workflow:** `Kickoff → Avatar → Positioning → Messaging → Content → Ads → Analytics → Optimization`

### Specialist Skills

Each skill is self-contained in its own folder with a `SKILL.md` file containing:

- **Purpose** — What the skill does
- **Core Principles** — Guiding rules
- **Workflow** — Step-by-step process
- **Output Format** — Structured output template
- **Guardrails** — What to avoid

### Current Skills

| Skill | Discipline | Status |
|---|---|---|
| **Customer Avatar Architect** | Strategy/Research | ✅ Active |
| **AIO / GEO / AEO Gold Standard** | SEO (AI visibility) | ✅ Active |
| Brand Architect | Branding | 🔜 Planned |
| Content Strategist | Content | 🔜 Planned |
| SEO Specialist | SEO | 🔜 Planned |
| Ads Strategist | Paid Media | 🔜 Planned |
| Social Media Manager | Social | 🔜 Planned |
| Analytics Lead | Analytics | 🔜 Planned |
| Sales Enablement | Sales | 🔜 Planned |
| Ops Automation | Operations | 🔜 Planned |

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
