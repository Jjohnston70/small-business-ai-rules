# AI Control Plane, Solo and Small Team Edition

AI rules for a person or small business that runs on chat subscriptions (ChatGPT, Claude, Perplexity, Gemini, Copilot, NotebookLM) and nothing wired to an API.

You still need a control plane. At your scale it is a one-page table, three settings pages, and a log sheet.

## What it answers

| Question | Answered by |
|---|---|
| Who is cleared to act? Which tool, which account, which person | Tool routing table |
| What may go into which tool? | Four data classes and the paste rule |
| Are the accounts locked down? | Account checklist, dated, redone quarterly |
| Why did we make that call? | Decision log, one row per AI-shaped decision |
| What if it goes wrong? | Kill switch and incident card |

## What is in the plugin

| File | What it is |
|---|---|
| `skills/ai-control-plane-solo/SKILL.md` | The skill: five artifacts, team add-ons, scaling path |
| `references/tool-routing.md` | How to fill the routing table, with a worked example for a fuel distributor |
| `references/data-classes.md` | Public, Internal, Confidential, Licensed or regulated, and the two sorting questions |
| `references/account-checklist.md` | The per-tool settings checklist |
| `references/verify-lite.md` | Four-step verification rule for any AI-supplied fact, plus a paste-in prompt |
| `assets/tool-routing-table.csv` | Routing table template |
| `assets/decision-log.csv` | Decision log template |
| `assets/incident-card.md` | Printable incident card |

## Install

Once it is listed in the Claude plugin directory: in Claude Code, open `/plugin` and find it under Discover; in the Claude app, add it from the directory.

## How to use it

Ask Claude things like "can I paste this into ChatGPT," "set up AI rules for my team," or "which AI should I use for this job." The skill walks you through the artifact you need.

## Principles

| Principle | In practice |
|---|---|
| Settings pages are the source of truth | Record the exact wording and the date you checked; vendors change terms |
| Licensed data never goes into AI | Paid data feeds and regulated records stay in the system they came from |
| AI informs, a person decides | Every AI-shaped decision gets a log row naming who made the final call |
| Redaction beats refusal | Replace names and amounts with placeholders and the problem becomes Internal |

## Source

Built on Deloitte Insights, "The next tech infrastructure advantage is intelligence orchestration," 21 August 2026, adapted for subscription-only operators.

## License

MIT. See `LICENSE`.

## Who built it

True North Data Strategies LLC, an operations consultancy that builds for the people who run the work. [truenorthstrategyops.com](https://truenorthstrategyops.com)
