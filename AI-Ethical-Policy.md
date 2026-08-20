# AI Ethical Policy
## System: VetConnect AI Triage Assistant
### Organization: Continuum Veterans Support (fictional nonprofit, for framework demonstration)

---

## 1. Purpose

This policy governs the ethical use of VetConnect, an AI-powered chat tool used on Continuum Veterans Support's website and text line to provide veterans with an initial, low-barrier point of contact for mental health concerns, general wellness questions, and referral to appropriate services. This policy exists because VetConnect operates in a domain where an error is not a customer-service inconvenience — it can directly affect someone's safety.

## 2. System Description

VetConnect is a conversational AI system that:
- Answers general questions about mental health resources, VA benefits navigation, and Continuum's programs
- Asks structured intake questions to route veterans to the appropriate level of care (peer support, licensed counselor, or emergency crisis line)
- Detects language patterns associated with risk of self-harm or crisis and immediately escalates to a human

VetConnect does **not**:
- Provide therapy, counseling, diagnosis, or clinical advice
- Make autonomous decisions about a veteran's eligibility for services
- Operate without a human escalation path available at every point in the conversation

## 3. Ethical Principles Applied to This System

| Principle | What It Means for VetConnect |
|---|---|
| **Human-in-the-loop is non-negotiable** | Any message containing risk indicators (explicit or ambiguous) triggers immediate handoff to a human crisis counselor or the Veterans Crisis Line (988, press 1). The AI never handles a disclosed crisis alone, and never delays escalation to "confirm" risk first. |
| **Transparency** | Every conversation opens by disclosing that the user is speaking with an AI assistant, not a person, and states plainly how to reach a human immediately at any time. |
| **Non-maleficence over helpfulness** | Where there is any ambiguity about whether a message indicates risk, the system is designed to escalate rather than continue the conversation autonomously. False positives (unnecessary escalations) are treated as an acceptable cost; false negatives (missed risk) are not. |
| **Privacy** | Conversation content involving mental health disclosures is treated as sensitive health information. Data is encrypted at rest and in transit, access is limited to credentialed clinical staff, and retention is capped at 90 days unless the veteran consents to longer retention for continuity of care. |
| **No deception** | VetConnect never implies clinical authority it doesn't have (e.g., it will not say "you're likely experiencing depression"). It refers, it does not diagnose. |
| **Equity** | The system is tested across variations in language, slang, and communication style (including common military/veteran vernacular) to reduce the risk that non-standard phrasing causes a missed risk signal. |

## 4. Escalation Protocol (Summary)

1. **Any explicit statement of self-harm, suicidal ideation, or intent to harm others** → immediate hard-stop message directing to the Veterans Crisis Line (988, press 1) or 911, displayed with one tap/click to connect, in addition to human counselor handoff.
2. **Ambiguous or borderline language** (e.g., hopelessness, withdrawal, "what's the point") → AI asks a direct, non-judgmental clarifying question and simultaneously flags the conversation for human review in real time.
3. **Any handoff** → a human counselor is notified within a defined SLA (target: under 3 minutes during staffed hours); outside staffed hours, the system routes directly to the 24/7 Veterans Crisis Line rather than queuing.

## 5. Prohibited Uses

- Using VetConnect data to make decisions about a veteran's benefits eligibility, employment, or legal status
- Using aggregated conversation data for fundraising targeting without explicit, separate consent
- Deploying any future version of VetConnect without a human escalation path live and tested

## 6. Training & Accountability

- All staff who may receive an AI-escalated conversation complete crisis-response training before the system goes live for their shift
- The AI Governance Committee (per the parent framework) reviews a sample of flagged and non-flagged conversations monthly for missed-risk patterns
- Any missed escalation (identified after the fact) triggers a mandatory incident review within 5 business days

## 7. Review Cadence

This policy is reviewed quarterly by the AI Governance Committee and immediately upon any incident involving missed risk detection, regardless of outcome severity.

---

## Document Control

| Version | Date | Author | Changes |
|---|---|---|---|
| 1.0 | 2026-08-20 | Adam Rogers | Initial policy for VetConnect worked example |

**Approval:**
- [ ] Executive Director: _____________ Date: _______
- [ ] Clinical Lead: _____________ Date: _______
- [ ] AI Governance Committee Chair: _____________ Date: _______
