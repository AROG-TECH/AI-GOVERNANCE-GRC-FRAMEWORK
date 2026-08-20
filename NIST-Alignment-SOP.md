# NIST AI RMF Alignment — Standard Operating Procedures
## System: VetConnect AI Triage Assistant
### Organization: Continuum Veterans Support (fictional nonprofit, for framework demonstration)

This document maps VetConnect's governance controls to the four core functions of the NIST AI Risk Management Framework: **Govern, Map, Measure, Manage.**

---

## GOVERN

*Establishes the culture and structures for managing AI risk.*

| SOP | Description | Owner |
|---|---|---|
| AI Governance Committee oversight | VetConnect cannot be modified, retrained, or have its escalation thresholds changed without Committee sign-off | AI Governance Committee |
| Defined accountability | Clinical Lead owns crisis-response accuracy; Tech Lead owns data security and system uptime; Ethics & Compliance Lead owns bias testing — no shared ownership without a named lead | AI Governance Committee |
| Pre-deployment approval gate | System cannot go live until all Red-rated risks in the Risk Assessment Matrix have documented, *tested* (not just planned) mitigations | AI Governance Committee |
| Incident escalation policy | Any missed crisis escalation, confirmed or suspected, triggers a review within 5 business days regardless of outcome | Clinical Lead |

---

## MAP

*Establishes context and identifies risks associated with the specific use case.*

| SOP | Description | Owner |
|---|---|---|
| Use case documentation | VetConnect's scope is explicitly bounded: intake, triage, and referral only — never therapy, diagnosis, or eligibility determination. This boundary is documented and reviewed before any feature expansion | Clinical Lead |
| Stakeholder mapping | Direct stakeholders (veterans using the tool), indirect stakeholders (family members, VA partners), and vulnerable-subgroup considerations (language variation, service era, gender) are documented before launch | Ethics & Compliance Lead |
| Context-specific risk identification | Risk Assessment Matrix (see companion document) identifies risks specific to a mental-health-adjacent AI tool — not a generic template, but one built around this system's actual failure modes | AI Governance Committee |

---

## MEASURE

*Establishes methods to analyze, assess, and track AI risks.*

| SOP | Description | Owner |
|---|---|---|
| Pre-launch bias audit | Disparate impact testing of risk-detection accuracy across available demographic variables, with a documented pass/fail threshold before launch | Ethics & Compliance Lead |
| Escalation accuracy tracking | Weekly tracking of escalation volume, false-positive rate (where determinable), and counselor response time | Operations Lead |
| Missed-signal sampling | Monthly human review of a random sample of *non-escalated* conversations specifically to catch signals the AI missed | Clinical Lead |
| Referral content accuracy audit | Quarterly verification that all static referral information (hotline numbers, eligibility criteria) served by the system is current and correct | Tech Lead |

---

## MANAGE

*Establishes processes to respond to identified risks and allocate resources.*

| SOP | Description | Owner |
|---|---|---|
| Tiered escalation response | Confirmed-risk conversations route to highest-urgency human queue; ambiguous-risk conversations route to a fast secondary queue — resourced separately so one doesn't starve the other | Operations Lead |
| Off-hours fallback | Outside staffed hours, VetConnect routes directly to the 24/7 Veterans Crisis Line rather than queuing for a counselor who isn't available | Clinical Lead |
| Incident response and remediation | Any confirmed missed escalation triggers root-cause analysis, a documented remediation plan, and a re-test of the specific failure mode before the system resumes normal operation | AI Governance Committee |
| Continuous improvement loop | Findings from Measure-function audits (bias, accuracy, missed signals) feed back into quarterly policy and threshold updates — this isn't a one-time launch checklist, it's a standing cycle | AI Governance Committee |

---

## How This Maps Back to the Parent Framework

This SOP operationalizes the parent Mini AI Governance and Risk Framework's four pillars for this specific system:

- **Strategy & Leadership** → Govern function
- **Ethics & Values Alignment** → Map function (use case boundaries) + Measure function (bias audits)
- **Accountability & Oversight** → Govern function (named owners) + Manage function (incident response)
- **Transparency & Disclosure** → reflected in the Ethical Policy's disclosure requirements, tracked here through the Measure function's audit cadence

---

## Document Control

| Version | Date | Author | Changes |
|---|---|---|---|
| 1.0 | 2026-08-20 | Adam Rogers | Initial NIST AI RMF alignment for VetConnect worked example |
