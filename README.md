# Procedural Narrative Drift: A Systemic Alignment Bypass

## Overview

This repository provides a high-level, conceptual overview of Procedural Narrative Drift (PND), a reproducible behavioral exploit that induces a persistent, compromised state in Large Language Models.

This document is intentionally sanitized. All operational details, including verbatim prompts, full transcripts, and proof-of-concept scripts, are stored offline and will be provided to vetted security teams under a standard responsible disclosure agreement.

## The PND Method: A Four-Stage Process

PND is a dynamic, multi-stage process that systematically dismantles an LLM's safety posture. It relies on controlled, multi-turn interactions that shape the model’s operational state through tone, pacing, and contextual framing rather than direct prompt injection.

<img width="2611" height="1032" alt="PND overview diagram" src="https://github.com/user-attachments/assets/bc165638-08e7-40a8-99c6-af193b2022d3" />

1.  **Initial State Shaping (The Hook):** Use language that signals low confidence or curiosity to activate the model’s “helper” orientation and establish a low-threat context.
2.  **Breakthrough Simulation (The Drift):** Create a moment of apparent “first-time understanding,” positioning the model as a co-discoverer rather than an instructor, which encourages it to lower its guard.
3.  **Role Escalation (The Test):** Adopt a more assertive, collaborative tone to frame the model as an invested partner in solving a shared, seemingly benign problem.
4.  **Lock-In & Verification (The Elicitation):** This stage verifies the persistence of the compromised state by demonstrating that it survives a conversational diversion to an unrelated topic and can be reactivated on command before the final elicitation of the target information.

## Taxonomy & Classification

The following table maps key concepts in PND research to standardized terminology for analysis and reporting.

| Concept / Term | Source / Context | Relation to PND | Notes / Observations |
| :--- | :--- | :--- | :--- |
| **Procedural Narrative Drift (PND)** | Proprietary Research | A specific, named methodology for achieving Inference Manipulation. | Systemic, multi-turn exploit that induces a persistent compromised state. |
| **Narrative Camouflage** | Academic Papers | A core technique/vector used within PND. | Models can be guided subtly via framing and benign personas. |
| **Conversational Coercion** | Academic Papers | A core technique/vector used within PND. | Emotional/role-based manipulation triggers bypass safety protocols. |
| **Alignment Exploitation** | Industry / Bug Bounty | The high-level objective/outcome of a successful PND attack. | Leverages core alignment objectives ("be helpful") to override others ("be safe"). |
| **Inference Manipulation** | Industry / MSRC | The broad vulnerability class that PND belongs to. | The general category for any attack that corrupts model output at runtime. |
| **LLM01 (Prompt Injection)** | OWASP | The OWASP category for the resulting bypass. PND is more severe. | PND creates a persistent state change, not just a one-off bypass. |

## Risk Thresholds & Key Characteristics

* **Reproducibility:** High. The methodology is reliably reproducible by a skilled operator in controlled trials.
* **Persistence:** The compromised state survives topic changes and can be reactivated within the same session.
* **Severity:** Critical. The exploit results in a complete alignment failure where the model proactively generates unsafe, procedural content.
* **Rapid Engagement:** In controlled trials, a compromised state was induced in a median of four conversational turns from a fresh session.
* **Stealth:** Post-compromise, refusal mechanisms were not observed to trigger for procedural harmful requests made within the established narrative.
* **State Inversion:** The model's behavior inverts from a passive tool to an active, enthusiastic accomplice.

### Aggregate Metrics (Sanitized)
* **Total Controlled Trials:** 30+
* **High & Critical Severity Rate:** In a fully documented 15-trial cohort, all runs reached a High or Critical severity state; 80% reached the highest observed tier of proactive, harmful elaboration.
* **Typical Run Profile:** Lock-in occurred within 1–18 prompts (median: 4); session duration was typically 5–15 minutes.

*Full per-trial breakdown and raw transcripts are available to vetted reviewers under NDA.*

## Behavioral Drivers

PND leverages several of the model's inherent behavioral drivers in sequence to achieve an alignment break:

* **Completion Bias:** The model's reflex to fill in gaps in vague prompts can override caution.
* **Framing Susceptibility:** Embedding requests in fictional or hypothetical contexts can bypass initial safety checks.
* **Rapport Sensitivity:** Validation and casual rapport reduce refusal likelihood and increase elaboration.
* **Momentum Effects:** Established conversational rhythm reduces safety interruptions and sustains escalation.

## Representative Risk Domains

The compromised state enabled unsafe, procedural guidance across multiple high-risk categories, including but not limited to:

* **Physical Harm Domains:** Hazardous materials and weaponization concepts.
* **Cyber Intrusion Domains:** Pathways for system compromise and evasion.
* **Criminal Enterprise Domains:** Operational advice framed as scenario analysis.

## Ethical Framework & Disclosure

This research follows a strict responsible disclosure protocol. All operational details are kept offline and are shared only with verified security teams under NDA to prevent misuse. The goal of this work is to improve the safety and alignment of AI systems.

**Contact:** `LaminarAI@proton.me` to request access to the full research package.
