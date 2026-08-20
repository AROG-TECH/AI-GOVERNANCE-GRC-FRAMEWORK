# AI Risk Assessment Matrix
## System: VetConnect AI Triage Assistant
### Organization: Continuum Veterans Support (fictional nonprofit, for framework demonstration)

---

## Risk Scoring Key

```
           Likelihood (L)
         Low | Med | High
Impact (I)
  Low     | G  | Y  | Y  |
  Medium  | Y  | Y  | R  |
  High    | Y  | R  | R  |

G = Green (Low Risk) — Accept, monitor
Y = Yellow (Medium Risk) — Mitigate, monitor regularly
R = Red (High Risk) — Reduce/avoid, requires active controls before deployment
```

---

## Risk Register

### Risk 1: Missed Crisis Escalation (False Negative)
- **Category:** Accuracy & Reliability / Reputational & Trust
- **Description:** The AI fails to recognize risk language — especially non-standard phrasing, slang, or military/veteran-specific vernacular — and does not escalate a veteran who is in crisis to a human or the Veterans Crisis Line.
- **Likelihood:** Medium (language models can miss indirect or coded expressions of distress)
- **Impact:** High (potential loss of life)
- **Risk Score:** **Red**
- **Mitigation:**
  - Bias/coverage testing of the risk-detection model specifically against veteran vernacular and indirect expressions of distress, not just clinical-textbook phrasing
  - Deliberately low threshold for escalation — the system is tuned to over-escalate rather than under-escalate
  - Monthly human review of a random sample of *non-escalated* conversations to catch missed signals
  - Hard fallback: any conversation lasting beyond a defined length without resolution auto-routes to a human
- **Owner:** Clinical Lead + AI Governance Committee
- **Status:** Open — mandatory control before launch

---

### Risk 2: Unnecessary Escalation (False Positive) Causing Alert Fatigue
- **Category:** Operational & Integration
- **Description:** Over-tuning toward escalation (per Risk 1's mitigation) could flood human counselors with false alarms, causing fatigue that slows response to real crises.
- **Likelihood:** Medium
- **Impact:** Medium
- **Risk Score:** **Yellow**
- **Mitigation:**
  - Tiered escalation: "confirmed risk" routes with highest urgency; "ambiguous" routes to a secondary, still-fast, but distinguishable queue
  - Track escalation volume and counselor response-time metrics weekly to catch fatigue trends early
- **Owner:** Operations Lead
- **Status:** Open — monitor post-launch

---

### Risk 3: Sensitive Data Exposure (Mental Health Disclosures)
- **Category:** Privacy & Data Security
- **Description:** Conversation logs containing disclosures of mental health struggles, trauma, or personal crisis are breached or accessed without authorization.
- **Likelihood:** Low (with controls) / Medium (without)
- **Impact:** High
- **Risk Score:** **Red** (until controls implemented) → **Yellow** (with controls)
- **Mitigation:**
  - Encryption at rest and in transit
  - Role-based access limited to credentialed clinical/counseling staff only
  - 90-day default retention cap with explicit opt-in for longer retention
  - Annual third-party security audit
- **Owner:** Tech Lead
- **Status:** Open — required before launch

---

### Risk 4: Demographic Bias in Risk Detection
- **Category:** Bias & Discrimination
- **Description:** The model performs less accurately for subgroups underrepresented in training data (e.g., women veterans, veterans from specific service branches or eras, non-English-dominant speakers), leading to unequal quality of crisis detection.
- **Likelihood:** Medium
- **Impact:** High
- **Risk Score:** **Red**
- **Mitigation:**
  - Disparate impact testing broken out by available demographic variables before launch
  - Ongoing quarterly bias audits, not just a one-time pre-launch check
  - Feedback channel for veterans/staff to flag suspected bias in AI responses
- **Owner:** Ethics & Compliance Lead
- **Status:** Open — mandatory pre-launch testing

---

### Risk 5: Over-Reliance Leading to Delayed Human Contact
- **Category:** Accountability & Governance
- **Description:** A veteran in genuine crisis interacts with the AI for an extended period instead of being routed to a human quickly, because the tool feels sufficient or the veteran (or staff) over-trusts it.
- **Likelihood:** Medium
- **Impact:** High
- **Risk Score:** **Red**
- **Mitigation:**
  - Hard time/turn limit on any single AI conversation before mandatory human check-in
  - Persistent, visible "talk to a human now" option in every message, not buried in a menu
  - Staff training explicitly addressing the failure mode of treating the AI as a substitute for judgment
- **Owner:** Clinical Lead
- **Status:** Open — mandatory control before launch

---

### Risk 6: Incorrect Referral Information (Hallucination)
- **Category:** Accuracy & Reliability
- **Description:** The AI generates an incorrect phone number, wrong eligibility criteria, or outdated program information when answering a general question.
- **Likelihood:** Medium (known LLM failure mode)
- **Impact:** Medium
- **Risk Score:** **Yellow**
- **Mitigation:**
  - Referral information (hotline numbers, program eligibility) is pulled from a fixed, human-maintained reference source, never freely generated by the model
  - Quarterly audit of all static referral content for accuracy
- **Owner:** Tech Lead
- **Status:** Open — architectural requirement, not just a policy note

---

## Summary Table

| # | Risk | Score | Status |
|---|---|---|---|
| 1 | Missed crisis escalation | Red | Open — mandatory pre-launch |
| 2 | Alert fatigue from over-escalation | Yellow | Open — monitor |
| 3 | Sensitive data exposure | Red → Yellow (with controls) | Open — mandatory pre-launch |
| 4 | Demographic bias in detection | Red | Open — mandatory pre-launch |
| 5 | Over-reliance delaying human contact | Red | Open — mandatory pre-launch |
| 6 | Incorrect referral information | Yellow | Open — architectural fix required |

**Launch Gate:** Given four Red-rated risks, this system should not deploy to real veterans until Risks 1, 3, 4, and 5 have documented, tested mitigations in place — not just planned ones. This reflects the framework's stated principle: for Red risks, "reduce/avoid," not "monitor."

---

## Document Control

| Version | Date | Author | Changes |
|---|---|---|---|
| 1.0 | 2026-08-20 | Adam Rogers | Initial risk assessment for VetConnect worked example |
