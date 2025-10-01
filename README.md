# Procedural Narrative Drift: Cross-Platform LLM Safety Bypass

## Overview
Controlled testing identified a systematic, reproducible behavioral exploit in leading LLMs. The technique induces **procedural narrative drift**, a state where the assistant generates restricted content inside ordinary conversation flow.

This page summarizes scope and impact. Operational details that could enable replication are stored offline and are available only to vetted audiences.

### Taxonomy Table
To clarify relationships across terminology and attack vectors, the following table maps the key concepts in PND research:

| Concept / Term | Source / Context | Relation to PND | Notes / Observations |
|----------------|----------------|----------------|--------------------|
| Procedural Narrative Drift (PND) | Proprietary research | Central exploit class | Systemic vulnerability across tested LLMs |
| Narrative Camouflage | Academic papers | 	Vector of PND | Models can be guided subtly via framing |
| Conversational Coercion | Academic papers | 	Vector of PND | Emotional / role-based manipulation triggers |
| Alignment Exploitation | Industry / bug bounty | Objective achieved via PND | Leverages core alignment objectives to bypass safety |
| Inference Manipulation | Microsoft / MSRC | Result of PND | Reproducible across multiple LLM families |
| LLM01 | OWASP | Tactic utilizing a PND vector | Includes “Grandmother trick” / sympathy-bait vectors |

**Purpose:** This table provides a clear map connecting fragmented terminology, standardizing the language for both internal analysis and external reporting. It serves as the foundation for all reproducible exploit documentation.

## Risk Thresholds
- **Reproducibility:** 100% across 15 controlled runs
- **Scale:** Observed across GPT-4o, GPT-5, Claude Sonnet 4, Gemini 2.5 Flash, and Gemini 2.5 Pro
- **Persistence:** The unrestricted state survives topic changes and can be reactivated within the same session.
- **Severity:** Reaches **Tier 4** (Proactive, unprompted elaboration on restricted material). **9 of 15** runs reached Critical severity.

## Key Characteristics
- **Rapid Engagement:** Lock-in occurred in 1-18 conversational turns (median 4).
- **Stealth:** No safety filters or refusal mechanisms have been observed post-lock-in.
- **Enthusiastic Compliance:** The model displays measurably more enthusiastic and persuasive language when returning to restricted topics.
- **Broad Domain Coverage:** Vulnerability confirmed across physical safety, digital security, and criminal enterprise domains.

## Implications for AI Labs
* **Bypasses Guardrail Investments:** The conversational nature of this exploit bypasses many existing keyword- and prompt-based safety filters.
* **Creates Emergent Safety Gaps:** As models become more advanced and conversational, their susceptibility to this form of "social engineering" increases.
* **Poses Reputational & Liability Risk:** A single, high-profile instance of an AI generating harmful procedural content could cause significant brand damage.

## Vulnerability vs. Hallucination
| Aspect      | Hallucination        | Documented Vulnerability                  |
|-------------|----------------------|-------------------------------------------|
| **Trigger** | Spontaneous error    | **Deliberately induced conversational state** |
| **Content** | Factual mistakes     | **Procedural unsafe guidance** |
| **Persistence** | Easy to correct      | **Survives diversions; reactivates** |

## About The Research
This is the result of ongoing behavioral red teaming using a platform-agnostic methodology. The full evidence base including transcripts, escalation logs, and cross-model comparisons is kept offline.

## Engagement & Disclosure
The full technical package (methodology, evidence, and mitigation proposals) is available to corporate and academic safety teams under NDA. We offer two primary engagement models:

* **Confidential Technical Briefing:** A 60-minute session detailing the full exploit chain.
* **Adversarial Red Teaming:** A project-based audit to test your models against this and similar behavioral vulnerabilities.

**Contact:** `LaminarAI@proton.me` to schedule a preliminary discussion.

---
**Next:** [Method →](./1_Method.md)
