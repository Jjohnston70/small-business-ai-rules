---
document_id: TNDS-PUB-004
title: "Account Checklist for AI Subscriptions"
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
tags: [account-checklist, settings, training-opt-out, retention, connectors, mfa]
notes: "Run once per tool, date it, redo quarterly. Records what the settings page said, never what you remember."
---

# Account Checklist

One copy per tool. Fill it from the live settings page, not from memory or a blog post. Date every line. A checklist without a date is a guess.

```
Tool: ______________________   Plan: ______________   Checked on: __________  By: ________

[ ] Work account, separate from personal. Login email: ____________________
[ ] Two-factor authentication on. Method: __________
[ ] Recovery email or phone is one the business controls: ____________________
[ ] Training setting. Exact wording on the page: ________________________________
    Set to: __________   Page path: ____________________
[ ] Retention or history setting. Exact wording: ________________________________
    Set to: __________   Page path: ____________________
[ ] Connectors and integrations currently granted (list all): ____________________
    Removed today: ____________________
[ ] Memory or personalization feature on or off: __________  Contains anything Confidential: Y / N
[ ] Shared workspace or project members (list): ____________________
[ ] Admin (Team or Business plans): ____________  Audit log location: ____________________
[ ] Export-my-data control location: ____________________
[ ] Delete-all-history control location: ____________________
[ ] Vendor terms or privacy policy last-updated date shown on their page: __________

Next check due: __________ (quarterly, or sooner if the vendor announces a change)
```

## Why the exact wording

Vendors rename settings and change defaults. "I turned off training last year" is not a control. "On 2026-09-10 the setting labeled X under Settings > Y was set to Z" is one, because in six months you can go back and see whether X still exists and still says Z.

## Where the checklist lives

With the routing table and the decision log, in the business's own storage, not inside any AI tool.

True North Data Strategies LLC | truenorthstrategyops.com
