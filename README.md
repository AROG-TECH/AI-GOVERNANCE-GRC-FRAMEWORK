# AI-GOVERNANCE-GRC-FRAMEWORK
## AI Governance, Risk & Compliance Framework — with Applied Worked Example

## Overview

This repository contains two layers of work:

1. **A general-purpose AI Governance and Risk Framework** (`AI_GOVERNANCE_FRAMEWORK.md`), built for nonprofit organizations adopting AI tools. It covers governance pillars, a risk assessment methodology, an implementation roadmap, and compliance monitoring structures.
2. **A worked example applying that framework to a specific, high-stakes system**: an AI-powered crisis and mental health referral chatbot for a veteran-services nonprofit. The worked example is deliberately chosen to be a hard case — a system where getting governance wrong has real consequences — rather than a low-stakes example that would be easy to govern well by default.

The point of including both: a framework by itself shows you can organize what *should* be done. Applying it to a specific system — with actual risk scores, actual mitigations, and an actual launch-gate decision — shows the judgment involved in *doing* the work.

---

## Section 1: General Framework

`AI_GOVERNANCE_FRAMEWORK.md` — the "Mini AI Governance and Risk Framework for Nonprofits." Covers:
- Governance pillars (Strategy, Ethics, Accountability, Transparency)
- A Likelihood × Impact risk assessment methodology
- A 12-month phased implementation roadmap
- KPIs and a compliance checklist

This is the reusable template — intended to be adapted to any nonprofit's AI use case, not just the one below.

---

## Section 2: Worked Example — VetConnect AI Triage Assistant

A fictional AI chatbot used by a veteran-services nonprofit to provide initial mental health triage and route veterans to human counselors or crisis lines. Three documents apply the general framework to this specific system:

* **[AI-Ethical-Policy.md](./AI-Ethical-Policy.md)** — System-specific ethical policy: human-in-the-loop requirements, escalation protocol, prohibited uses, and accountability structure for VetConnect specifically.
* **[AI-Risk-Assessment-Matrix.md](./AI-Risk-Assessment-Matrix.md)** — A completed risk register with six identified risks (missed crisis escalation, data exposure, demographic bias, over-reliance, and others), each scored, mitigated, and assigned an owner — concluding with a launch-gate decision based on the framework's own Red/Yellow/Green rules.
* **[NIST-Alignment-SOP.md](./NIST-Alignment-SOP.md)** — Maps VetConnect's specific controls to the four NIST AI RMF functions (Govern, Map, Measure, Manage), and back to the general framework's four governance pillars.

**Why this use case:** A crisis-referral tool forces real trade-offs — for example, tuning the system to over-escalate (annoying but safe) rather than under-escalate (efficient but potentially catastrophic). Working through that trade-off, and documenting *why* the risk matrix comes out mostly Red rather than comfortably green, is the actual substance of GRC work — not just filling in a template.

---

## How to Use This Repository

- If you're adapting the **general framework** to your own organization's AI use case: start with `AI_GOVERNANCE_FRAMEWORK.md`, then use the three worked-example documents as a model for how to fill in your own risk assessment, policy, and NIST alignment.
- If you're evaluating this repository as a work sample: the worked example (Section 2) is the best indicator of applied judgment; the general framework (Section 1) is the best indicator of structural/organizational thinking.

---

© 2026 Adam Rogers. All rights reserved.
