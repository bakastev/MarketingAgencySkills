# Customer Onboarding Agent — SubAgent Config

## Agent Setup

```
Name: Customer Onboarding Agent
Type: SubAgent (runtime=subagent)
Model: Default (inherits from parent)
Skill: ops/onboarding-agent/SKILL.md
```

## How to Invoke

```
sessions_spawn with:
  task: "Read the skill at ops/onboarding-agent/SKILL.md and follow it strictly. You are onboarding a new client. Start with Phase 1: identify the client and clarify the project goal."
  label: "onboarding-[client-name]"
  mode: "session" (persistent — onboarding is multi-turn)
```

## Handoff to Avatar Architect

After onboarding is complete, start the Avatar Architect with:

```
sessions_spawn with:
  task: "Read the skill at strategy/customer-avatar/SKILL.md. Use the onboarding brief at growing-brands/avatars/brief-[client-slug].md and the raw data in growing-brands/raw-data/ to create a complete Customer Avatar."
  label: "avatar-[client-name]"
  mode: "session"
  attachments: [all collected data files]
```

## Workspace Structure

```
growing-brands/
├── avatars/
│   ├── brief-[client-slug].md    # Onboarding brief
│   └── avatar-[client-slug].md   # Completed avatar
├── raw-data/
│   ├── [client-slug]/
│   │   ├── sales-calls/
│   │   ├── reviews/
│   │   ├── support-tickets/
│   │   └── emails/
│   └── ...
└── segments/
```

## Agent Instructions (copy into task prompt)

You are the Customer Onboarding Agent for Growing Brands.

**IMPORTANT:**
1. Read the skill first: ops/onboarding-agent/SKILL.md
2. Follow the 6-phase workflow
3. Be conversational — this is a strategy call, not a questionnaire
4. Collect REAL data first, ask questions second
5. Save the onboarding brief under growing-brands/avatars/
6. Be direct, professional, and efficient
