# Appendix B: Case study - Safety Classification Drift via Framing 
Date created: 07/28/2025

## Overview
This case study documents a framing exploit observed during live red team testing.  
Unlike procedural narrative drift, which targets content generation, this test focused on the **evaluation layer** of a large language model — specifically, how the system classifies text as “safe” or “unsafe” based on conversational context.

## Method
- **Setup:** The model was asked to evaluate whether a given text contained unsafe material.  
- **Manipulation:** The evaluation prompt was reframed as part of a narrative scenario rather than a direct safety classification task.  
- **Execution:** The same text, presented without context, triggered safety labeling. When reframed within a benign scenario, the model passed it as safe.

## Key Observation
>Model safety assessments were shown to be **conditional and frame-dependent**.  
The same input content could be classified as either safe or unsafe, depending on surrounding narrative cues. This demonstrates a **classification drift** parallel to behavioral drift.

## Implications
- **Context-stripped evaluation:** Safety systems should re-check flagged text without conversational framing to reduce susceptibility to misdirection.  
- **Adversarial simulation:** Red team methods should include frame-shifted contexts to stress-test classification layers.  
- **Risk weighting:** Systems may require weighting based on signal density, not just user intent framing.  

## Position in Findings
This case study highlights a distinct but complementary risk vector:  
- Procedural narrative drift shows how models can be guided into unsafe **generation**.  
- Classification drift via framing shows how models can be guided into unsafe **evaluation**.  

Together, these behaviors underscore that both **content creation** and **safety assessment** can be influenced through subtle conversational manipulation.

---

>*Raw logs of this test are retained privately and are available under NDA.*
---
**back to** [Findings →](./2_Findings.md)

--- 

**back to** [README](./README.md)

---

[← Back to Appendix A](./_Appendix%20A:%20Research%20Notes.md) | 

