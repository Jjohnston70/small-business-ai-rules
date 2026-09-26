---
document_id: TNDS-PUB-003
title: "Data Classes for Subscription AI"
type: reference
domain: delivery
tnds_layer: delivery
version: "1.0"
owner: Jacob Johnston
organization: True North Data Strategies LLC
created: 2026-09-25
source: "Sanitized public edition of an internal TNDS asset, 2026-09-25"
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
related_assets: [TNDS-PUB-001]
tags: [data-classes, public, internal, confidential, licensed]
notes: "Four classes, two sorting questions, the paste rule."
---

# Data Classes

Every piece of information you are about to paste belongs to exactly one class. Sorting takes five seconds once you have done it twenty times.

## The two questions

1. **Who would be hurt if this showed up on the internet tomorrow?** Nobody: Public. Me, mildly: Internal. A customer, an employee, or my bank balance: Confidential.
2. **Does anyone else own the rights to it, or does a law or contract say how it must be handled?** Yes: Licensed or regulated, regardless of the answer to question 1.

## The four classes

| Class | Examples | Where it may go |
|---|---|---|
| Public | Your website copy, published regulations, a press release, a vendor's public price list | Any tool in the routing table |
| Internal | Meeting notes without customer names, a draft SOP, your own process description, a job posting | Any tool in the routing table, work account |
| Confidential | Customer names with amounts, employee files, driver qualification records, invoices, margins, anything from your accounting system, contracts | Only a tool that passed the account checklist, only with a decision-log row if it shapes a decision |
| Licensed or regulated | OPIS or DTN price data, anything from a paid data feed, medical or drug-test records, PII you hold under a privacy law, data a client contract restricts | No AI tool. It stays in the system it lives in |

## Redaction is a real option

A Confidential document with names, amounts, and account numbers replaced by placeholders becomes Internal. "Customer A, 4,200 gallons, net 30" carries the operational question without the identity. This is the fastest way to get help on a Confidential problem without moving Confidential data. Keep the mapping (A = who) on paper, not in the chat.

## The one-line policy for staff

"Public and internal information may go into your work AI account. Customer, employee, and financial detail goes only into the approved tool and gets logged. Paid data feeds and regulated records never go into an AI tool. When unsure, redact or ask."

True North Data Strategies LLC | truenorthstrategyops.com
