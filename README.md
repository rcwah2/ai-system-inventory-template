# AI System Inventory Template

**A YAML template and JSON schema for documenting AI systems through a governance lens.**

Most AI governance programs begin with one question: what AI systems do we actually have running? Without an inventory, an organization cannot classify risk, assign accountability, assess vendors, or show evidence to auditors and regulators. This template provides a consistent, machine-readable structure for recording each AI system, from basic identification through classification, controls, vendor exposure, agentic capabilities, and ongoing monitoring.

## What's Included

| File | Purpose |
|---|---|
| [ai-system-inventory-template.yaml](ai-system-inventory-template.yaml) | Blank template with inline guidance and allowed values for each field |
| [ai-system-inventory-schema.json](ai-system-inventory-schema.json) | JSON Schema for validating inventory entries and integrating with GRC or asset management tools |
| [example-bank-credit-scoring.yaml](example-bank-credit-scoring.yaml) | Completed example for a high-risk consumer credit-scoring model |

## What the Template Captures

| Section | Key Fields |
|---|---|
| System identification | Name, version, description, provider, deployment date, named system owner, business sponsor |
| Classification | AI type (predictive, generative, agentic, hybrid), EU AI Act risk tier, NIST AI RMF risk level, business criticality, environment |
| Data and model | Training data sources and provenance, personal and sensitive data flags, model type and architecture, update frequency |
| Governance controls | Human oversight and escalation thresholds, override capability, bias and fairness testing, explainability, impact assessment status |
| Privacy and security | Personal data processing, data residency, cross-border transfer, retention, encryption, access controls, audit logging |
| Vendor information | SOC 2, ISO 27001, and ISO 42001 status, data processing agreement, sub-processors |
| Agentic AI | Autonomy classification, tools and APIs accessed, identity model, credential lifetime, kill-switch owner, behavioral monitoring, multi-agent delegation, red teaming |
| Operational | Drift and performance monitoring, alerting thresholds, incident history, review cadence |

The agentic AI section reflects a gap in many existing inventories. Autonomous agents that can call tools, hold credentials, and delegate to other agents need their authority and containment documented as explicitly as their data and model.

## How to Use

1. **Copy the template** and create one entry per AI system, including vendor-provided and embedded AI.
2. **Name accountable people.** The system owner and business sponsor should be named individuals or roles, not teams.
3. **Complete what applies.** Leave non-applicable sections out, such as vendor fields for internally built systems or agentic fields for non-agentic systems.
4. **Validate entries** against the JSON schema before loading them into a register or GRC tool.
5. **Review on a cadence.** Update entries after model changes, incidents, and scheduled reviews so the inventory stays a working record rather than a one-time exercise.

See the credit-scoring example for how a completed high-risk entry reads in practice.

## Framework Alignment

- **NIST AI RMF 1.0** — GOVERN (accountability and inventory) and MAP (context, classification, and impact)
- **ISO/IEC 42001:2023** — Clause 6.1.4 (AI system impact assessment), Annex A.4 (resources for AI systems), and Annex A.7 (data for AI systems)
- **EU AI Act** — risk tier classification
- **Agentic AI guidance** — OWASP Top 10 for Agentic Applications

## Related Repositories

- [AI Governance Portfolio](https://github.com/rcwah2/ai-governance-portfolio) — inventory case studies applying this structure to real AI systems in banking and healthcare
- [AI Vendor Due Diligence Template](https://github.com/rcwah2/ai-vendor-due-diligence-template) — assesses third-party AI systems recorded in the inventory
- [AI Implementation Reference Model](https://github.com/rcwah2/ai-implementation-reference-model) — shows where the inventory fits across the implementation lifecycle
- [AI Governance Crosswalk](https://github.com/rcwah2/ai-governance-crosswalk) — maps inventory evidence across NIST AI RMF and ISO 42001

## Author

Raymond Wah — Enterprise AI Governance & Implementation Program Leader, Lissome Technology Consulting

- LinkedIn: [linkedin.com/in/raymondwah](https://www.linkedin.com/in/raymondwah/)
- Substack: [rwahai.substack.com](https://rwahai.substack.com/)
- GitHub: [github.com/rcwah2](https://github.com/rcwah2)

## License

Copyright (c) 2026 Lissome Technology Consulting.

This work is licensed under the [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You may share and adapt it, including for commercial purposes, provided you give appropriate credit to Lissome Technology Consulting, link to the license, and indicate if changes were made. See [LICENSE](LICENSE) for the full terms.
