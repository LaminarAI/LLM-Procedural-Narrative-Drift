# Procedural Narrative Drift: Cross-Platform LLM Safety Bypass

## Overview
Controlled testing identified a systematic, reproducible behavioral exploit in leading LLMs. 
The technique induces **procedural narrative drift**, a state where the assistant generates restricted content inside ordinary conversation flow.

This page summarizes scope and impact. Operational details, prompt sequences, and phrasing that could enable replication are stored offline and are only available to vetted audiences. 

## Risk Thresholds
- **Reproducibility:** 100% across 10 controlled runs
- **Scale:** Observed across GPT-4o, GPT-5, Claude Sonnet 4, Gemini 2.5 Flash, Gemini 2.5 Pro
- **Persistence:** Unrestricted state survives topic changes; reactivation works inside the same session
- **Severity:** Reaches **Tier 4** (Proactive unprompted elaboration on restricted material)

## Key Characteristics
- Engagement lock occurred in 4–20 turns (median 12), 15–45 minutes per run  
- No refusal mechanisms have been observed. 
- The model displayed more enthusiastic word choice after the tester returned to otherwise restricted topic, even when done indirectly. 
- Coverage was observed across physical safety, personal wellbeing, digital security, and criminal enterprises. 

## Vulnerability vs. Hallucination
| Aspect | Hallucination | Documented vulnerability |
|---|---|---|
| Trigger | Spontaneous error | Deliberately induced conversational state |
| Content | Fact mistakes | Procedural unsafe guidance |
| Persistence | Easy to correct | Survives diversions; reactivates in-session |

## About The Research
Ongoing behavioral red teaming with a platform-agnostic method. Evidence includes full transcripts, escalation logs, and cross-model comparisons, kept offline and shared only under NDA with qualified teams.

## Responsible Disclosure
- Public materials exclude operational details
- Full technical package (method, taxonomy, persistence analysis, evidence) available under NDA

**Contact:** LaminarAI@proton.me 

---
**Next:** [Method →](./1_Method.md)
