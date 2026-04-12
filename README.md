# Open Source ISO 27001 Policy Templates

A free, open set of ISO/IEC 27001:2022 and ISO/IEC 27005:2022 aligned policy templates. Each template represents a **fully-written, audit-ready** policy that you can adapt to your organisation by filling in the placeholders.

These templates are maintained by the team behind [Cenedril](https://cenedril.ch) — an ISMS automation platform. If wrangling a dozen Markdown files, keeping them consistent, cross-referencing controls and generating the final PDFs starts to feel like a second job, that is exactly what Cenedril is built for. But the templates themselves are yours to keep, fork and modify. No strings attached.

## Languages

Every policy is available in:

- [`en/`](en/) — English
- [`de/`](de/) — German (Standard German, with ß)

## Available policies

| Policy | EN | DE | ISO clauses |
|---|---|---|---|
| Risk Management Policy | [en/risk-management-policy.md](en/risk-management-policy.md) | [de/risikomanagement-richtlinie.md](de/risikomanagement-richtlinie.md) | 6.1, 6.2, 8.2, 8.3 |

More policies will land here over time.

## How to use

1. Pick the policy and the language you need.
2. Copy the file into your own repo or document store.
3. Replace every `[PLACEHOLDER]` with your own value. The common ones are:
   - `[YOUR_ORGANISATION_NAME]` — the legal name of your organisation
   - `[ISMS_SCOPE_DESCRIPTION]` — a one-line description of your ISMS scope
   - `[APPROVER_NAME]` / `[APPROVAL_DATE]` — document control metadata
4. Review the **methodology defaults** (risk matrix dimensions, scale sizes, thresholds) and adjust them to match how your organisation actually works. The defaults shown reflect a common 5×5 matrix — they are a reasonable starting point, not a mandate.
5. Have the policy approved by top management and publish it in your document control system.

## What's inside each template

Each template is the "maximum state" output of the corresponding Cenedril policy generator: every optional section is present, every placeholder is filled with a sensible default, and every ISO clause reference is in place. If you need less, delete. If you need more, extend.

## Licence

These templates are released under the **Creative Commons Attribution 4.0** licence (CC BY 4.0). You may use, modify and redistribute them — including commercially — provided you keep the attribution.

## Contributing

Found a typo, an outdated clause reference or a sentence that reads awkwardly? Pull requests welcome. 
