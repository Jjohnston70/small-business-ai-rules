---
name: ai-control-plane-solo
description: "Rules for a person or small business that uses AI only through chat subscriptions (ChatGPT, Claude, Perplexity, Gemini, Copilot, NotebookLM), not APIs: a tool routing table, four data classes, a dated account-settings checklist, a decision log, and an incident card. Use when the user asks for AI usage rules or an AI policy for themselves or a small team, asks whether specific business, customer, employee, financial, or regulated information may be pasted into an AI chat tool, asks which AI subscription should handle a recurring business job, or needs to respond after sensitive information went into an AI tool. Do not use for API, gateway, or enterprise AI governance, or for general feature or price comparisons of AI products."
metadata:
  document_id: TNDS-PUB-001
  title: "AI Control Plane, Solo and Small Team Edition"
  type: ai-asset
  domain: delivery
  tnds_layer: delivery
  version: "1.0"
  owner: Jacob Johnston
  organization: True North Data Strategies LLC
  created: 2026-09-25
  source: "Sanitized public edition of an internal TNDS skill, 2026-09-25. Built from Deloitte Insights, The next tech infrastructure advantage is intelligence orchestration (21 Aug 2026)"
  status: draft
  last_updated: 2026-09-25
  review_due: 2027-03-25
  supersedes: null
  superseded_by: null
  classification: public
  authority: reference
  approver: null
  use_with: [claude, claude-code, cowork]
  consumed_by: [ai-control-plane-solo]
  corpus: none
  related_assets: [TNDS-PUB-002, TNDS-PUB-003, TNDS-PUB-004, TNDS-PUB-005, TNDS-PUB-006]
  tags: [control-plane, subscriptions, chatgpt, claude, perplexity, small-business, ai-policy, data-classes]
  notes: "Public release candidate for the Claude plugin directory. Four questions answered with a routing table, data classes, an account checklist, a decision log, and a kill switch."
---

# AI Control Plane, Solo and Small Team Edition

## What this is

You run your business on ChatGPT, Claude, Perplexity, maybe Gemini or Copilot. You pay by the month, you type into a box, and nothing you have is wired to an API. You still need a control plane. Yours is a one-page table, three settings pages, and a log sheet.

Same four questions as the enterprise version, answered at your scale:

1. Who is cleared to act? Which tool, which account, which person.
2. On whose authority? What the tool may do on its own versus what you sign off.
3. On which net? What data is allowed into which tool.
4. What if it goes wrong? Where the plug is, and how you find out.

No server, no gateway, no code. If you later want those, see "Scaling up" below.

## The five artifacts

### 1. Tool routing table

One row per kind of job. Which tool, which account, what data class is allowed, and whether the output goes straight out or gets a human read first. Template in `assets/tool-routing-table.csv`; how to fill it in `references/tool-routing.md`.

| Job | Tool | Account | Data allowed | Output goes |
|---|---|---|---|---|
| Research with sources | Perplexity or Claude with search | Work | Public | Read before use; check the date on every source |
| Draft an email, post, or SOP | Claude or ChatGPT | Work | Internal | You send it |
| Summarize a document | Claude or NotebookLM | Work | Internal | Read before use |
| Anything with customer names, pricing, financials, driver files | Only a tool whose settings you have checked (see artifact 3) | Work | Confidential, only if the checklist passed | You approve every use |
| Anything under someone else's license (OPIS, DTN, paid data feeds) or regulated by contract | No AI tool | none | Licensed | Stays in the system it came from |

### 2. Data classes

Four classes. Every piece of information you are about to paste belongs to exactly one. Full definitions and the two-question sort in `references/data-classes.md`.

- **Public**: already on your website or anyone's.
- **Internal**: yours, not secret, embarrassing at worst if it leaked.
- **Confidential**: customer, employee, financial, or operational detail that would cost you money or trust if it leaked.
- **Licensed or regulated**: data someone else owns the rights to, or data a law or contract tells you how to handle.

Rule: Public and Internal go anywhere in the table. Confidential goes only into a tool that passed the account checklist. Licensed or regulated goes into no AI tool.

### 3. Account checklist

Do this once per tool, write down the date, redo it every quarter and whenever the vendor announces a plan change. Full checklist in `references/account-checklist.md`. The short version:

- Separate work account from personal. Never the family login.
- Two-factor on. Recovery email is a work address you control.
- Find the setting that controls whether your conversations are used to train the vendor's models. Record what it says and what you set it to, with the date. Do not rely on what you remember reading last year.
- Find the data retention setting and the delete-history control. Record them.
- List every connector, integration, and app the tool has access to (Drive, Gmail, calendar, Slack). Remove anything it does not need for a job in your routing table.
- If you have a Team or Business plan, know who the admin is and where the audit log lives.

The checklist records what the settings page said on the day you looked. It does not assume. Vendors change terms; the date on your record is the protection.

### 4. Decision log

One sheet. One row every time AI output shaped a real decision: a price, a hire, a customer message, a compliance call, a purchase. Columns: date, decision, which tool, what it produced, what you checked it against, who made the final call. Template in `assets/decision-log.csv`.

This is the artifact that protects you when someone asks "why did we do that." The answer is never "the AI said so." It is "we checked it against X and I decided."

Any number that came out of an AI and went into a client or customer document gets the verification treatment: fetch the source, read the date on the page, label it single-source if there is only one. `references/verify-lite.md` is the pocket version.

### 5. Kill switch and incident card

Know before you need it:

- Where the "delete all chats" and "disconnect all apps" controls are, per tool.
- Where to revoke an integration's access from the other side (Google Workspace admin, Microsoft 365 admin).
- Where to change the password and end all sessions.
- Who you call if the vendor has an outage and you cannot get to your work: the routing table's fallback column says which tool takes over.

Write it on one card, `assets/incident-card.md`, and keep it where the person who is not you can find it.

## For a team of two to ten

Add three things:

1. Each person has their own work login. Shared logins break the decision log and make the kill switch useless.
2. The routing table and data classes are the AI policy. One page, plain English, signed by the owner. Nobody needs a forty-page policy; they need to know which four things never go into a chat box.
3. Monthly, ten minutes: reread the decision log, spot-check two entries, re-run one account checklist. That is the whole governance program.

## Scaling up, when you want it

| You are here | Next step | What it adds |
|---|---|---|
| Solo, subscriptions only | This skill, all five artifacts | Rules, hygiene, log, plug |
| Team plan on one vendor | Admin console: audit log, SSO, connector control | The vendor becomes part of your control plane |
| Need cost caps, routing by data class, private models | An API gateway with per-client keys and budgets, and a local model for private data | A technical build; bring in someone who has run one |
| Running AI operations for other businesses | A managed control plane | Operated as a service, with its own audit and rollback |

You never have to take the next step. Most solo operators and small teams live at the first row for years and are fine.

## What not to do

- Do not paste Confidential data into a tool whose training and retention settings you have not checked and dated.
- Do not put Licensed or regulated data into any AI tool.
- Do not share one login across people.
- Do not let an AI-shaped decision leave the building without a decision-log row.
- Do not quote a fact from an AI without opening the source and reading the date on it.
- Do not assume a vendor's terms are what they were last quarter.

## Sources this skill is built on

- Deloitte Insights, Thomas et al., "The next tech infrastructure advantage is intelligence orchestration," 21 Aug 2026: https://www.deloitte.com/us/en/insights/topics/technology-management/enterprise-ai-control-plane.html
- Vendor settings pages are the source of truth for training, retention, and connector controls. This skill deliberately cites none of them by feature name: check the live page, record the date.

True North Data Strategies LLC | truenorthstrategyops.com
