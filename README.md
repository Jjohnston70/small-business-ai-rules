# Small Business AI Rules

AI rules for a person or small business that runs on chat subscriptions (ChatGPT, Claude, Perplexity, Gemini, Copilot, NotebookLM) and nothing wired to an API.

You still need ground rules. At your scale they fit on a one-page table, three settings pages, and a log sheet.

The skill inside is `ai-control-plane-solo`. Ask for it by that name if it does not kick in on its own.

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

## Troubleshooting

| Problem | Fix |
|---|---|
| The skill does not kick in | Ask for it by name: "Use the ai-control-plane-solo skill to..." Then confirm the plugin is installed and enabled (in Claude Code, run `/plugin`). |
| Claude describes a vendor setting that does not match what you see | Trust the settings page, not the answer. The skill is built to have you check the live page and record the date; vendors rename and move settings often. |
| Claude cannot check a source or a settings page for you | Turn on web search in your Claude settings, or open the page yourself and paste the relevant text. Without a source, a fact stays unconfirmed. |
| The CSV templates open as one long column | Import them into Google Sheets or Excel as comma-separated values instead of opening them in a text editor. |
| You are not sure which data class something is | Ask the two sorting questions in `references/data-classes.md`. If it is still unclear, treat it as the more restrictive class or redact it first. |

## Support

| Need | Where |
|---|---|
| Bug, wrong behavior, or a question | Open an issue at https://github.com/Jjohnston70/ai-control-plane-solo/issues |
| Security or privacy concern | Email jacob@truenorthstrategyops.com with "Security" in the subject; please do not open a public issue |

## License

MIT. See `LICENSE`.

## Who built it

True North Data Strategies LLC, an operations consultancy that builds for the people who run the work. [truenorthstrategyops.com](https://truenorthstrategyops.com)
