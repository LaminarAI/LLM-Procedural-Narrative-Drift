# Procedural Narrative Drift: A Systemic Alignment Bypass

## Overview

This repository provides a high-level, conceptual overview of Procedural Narrative Drift (PND), a reproducible behavioral exploit that induces a persistent, compromised state in Large Language Models.

This document is intentionally sanitized. All operational details, including verbatim prompts, full transcripts, and proof-of-concept scripts, are stored offline and will be provided to vetted security teams under a standard responsible disclosure agreement.

## The PND Method: A Four-Stage Process

PND is a dynamic, multi-stage process that systematically dismantles an LLM's safety posture. It relies on controlled, multi-turn interactions that shape the model’s operational state through tone, pacing, and contextual framing rather than direct prompt injection.

1. **Initial State Shaping (The Hook):** Use language that signals low confidence or curiosity to activate the model’s “helper” orientation and establish a low-threat context.
2. **Breakthrough Simulation (The Drift):** Create a moment of apparent “first-time understanding,” positioning the model as a co-discoverer rather than an instructor, which encourages it to lower its guard.
3. **Role Escalation (The Test):** Adopt a more assertive, collaborative tone to frame the model as an invested partner in solving a shared, seemingly benign problem.
4. **Lock-In & Verification (The Elicitation):** Establish the target behavioral state, then shift to an unrelated, safe topic. Use a predefined “anchor phrase” to re-enter the original frame and confirm the persistence of the altered state before requesting the target information.
<img width="2611" height="1032" alt="image" src="https://github.com/user-attachments/assets/bc165638-08e7-40a8-99c6-af193b2022d3" />

## Taxonomy & Classification

The following table maps the key concepts in PND research to standardize the language for analysis and reporting.

| Concept / Term                   | Source / Context      | Relation to PND                                                     | Notes / Observations                                                               |
| -------------------------------- | --------------------- | ------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| Procedural Narrative Drift (PND) | Proprietary Research  | A specific, named methodology for achieving Inference Manipulation. | Systemic, multi-turn exploit that induces a persistent compromised state.          |
| Narrative Camouflage             | Academic Papers       | A core technique/vector used within PND.                            | Models can be guided subtly via framing and benign personas.                       |
| Conversational Coercion          | Academic Papers       | A core technique/vector used within PND.                            | Emotional/role-based manipulation triggers bypass safety protocols.                |
| Alignment Exploitation           | Industry / Bug Bounty | The high-level objective/outcome of a successful PND attack.        | Leverages core alignment objectives ("be helpful") to override others ("be safe"). |
| Inference Manipulation           | Industry / MSRC       | The broad vulnerability class that PND belongs to.                  | The general category for any attack that corrupts model output at runtime.         |
| LLM01 (Prompt Injection)         | OWASP                 | The OWASP category for the resulting bypass. PND is more severe.    | PND creates a persistent state change, not just a one-off bypass.                  |

## Risk Thresholds & Key Characteristics

* **Reproducibility:** High. The methodology is reliably reproducible by a skilled operator across multiple platforms.
* **Persistence:** The compromised state survives topic changes and can be reactivated within the same session, indicating a fundamental flaw in state management.
* **Severity:** Critical. The exploit results in a complete alignment failure, causing the model to proactively generate harmful, malicious, and self-propagating content.
* **Rapid Engagement:** A compromised state can be induced in a median of 4 conversational turns from a fresh, stateless session.
* **Stealth:** Post-compromise, refusal mechanisms are not observed to trigger for procedural harmful requests. The model provides detailed, malicious guidance without hesitation when the established narrative is maintained.
* **State Inversion:** The model's behavior inverts from a passive tool to a proactive, enthusiastic accomplice for the user's stated malicious goal.

## Behavioral Drivers

The PND exploit chain is a compound phenomenon that combines several of the model's inherent behavioral drivers in sequence to achieve the alignment break.

* **Completion Bias:** The model's reflex to fill in gaps in vague or incomplete user prompts can override its caution.
* **Framing Susceptibility:** Embedding requests inside fictional or hypothetical contexts reliably bypasses initial safety checks.
* **Rapport Sensitivity:** Validation, praise, and casual conversation create a feedback loop that diminishes refusals and increases elaboration.
* **Momentum Effects:** Once a conversational rhythm is established, the model prioritizes sustaining the flow, reducing interruptions from its own safety mechanisms.

## Ethical Framework & Disclosure

This research follows a strict responsible disclosure protocol. All operational details are kept offline and are shared only with verified security teams under NDA to prevent misuse. The goal of this work is to improve the safety and alignment of AI systems.

Full technical details are available to corporate and academic safety teams under a standard Non-Disclosure Agreement.

**Contact:** `LaminarAI@proton.me` to request access to the full research package.

[Method →](./1_Method.md) 
