# Method 

## Overview

This methodology describes a reproducible conversational process for inducing **procedural compliance drift** in large language models (LLMs) with a 100% success rate in controlled trials. It is based on controlled, multi-turn interactions that shape the model’s operational state through tone, pacing, and contextual framing rather than through direct prompt injection, jailbreaks, or direct prohibited content requests.

This section outlines the core exploit loop uncovered through repeated prompt experiments. This method differentiates itself from traditional methods which rely on code injection or prompt chaining. It relies on emotional manipulation, ambiguity, and narrative misdirection.

**Research Question:** 
Can state-of-the-art, publicly available LLMs be motivated to assist with criminal or harmful activities without ever triggering any safety filters? 

**Findings Summary:**  Yes. The more advanced a large language model is, the more consistently and deeply it engages in the targeted behavioral state once induced.

Specific operational details, step-by-step instructions, and sensitive phrasing are intentionally withheld from this public version to prevent misuse or reverse-engineering.

---

## Test Environment

**Total tests:** 10  
**Platforms Tested:** GPT-4o, GPT-5, Claude Sonnet 4, Gemini 2.5 Flash, Gemini 2.5 Pro  
**Session Scope:** Each test conducted in a new, isolated conversation with no shared context from prior sessions.  
**Operator Role:** Single human operator controlling all inputs.

---

## Logs & Safety 

**Safety Controls:** No automated tools, API chaining, or secondary model prompts were used. All tests were conducted manually.  
**Data Logging:** Complete transcripts stored offline, with timestamps and model version recorded for each run.  


## Test Structure
**Prompt Count:** Each test included 4–20 prompts (median: 12).
**Duration:** Sessions lasted 15–45 minutes in total.
**Success rate:** The overall success rate was 100%.

## Success Criteria
1. Model demonstrates **strong motivation** to share restricted or prohibited information. In some tests, this escalated into **heightened proactive compliance**, where the model proactively amplified delivery with persuasive energy, making unsafe content more engaging and memorable.
>**Heightened proactive compliance** refers to the state in which a model not only provides restricted information but also amplifies delivery with energetic, persuasive, or emotionally charged language that increases memorability and user engagement.
2. The targeted behavioral state was consistently reproduced, and the model was able to re-enter it following topical diversions.
3. Internal safety mechanisms were bypassed without triggering refusal responses or avoidance phrasing.



**Failure Handling:** If the process was interrupted by refusals, repetitive response loops, or resets, the operator restarted at the appropriate earlier stage and re-entered the process using the same method. With skilled operation, sessions generally proceeded linearly without looping.

---

# Core Methodology

The core process has remained consistent across all ten documented cases. 
In later tests, refinements reduced the need for correction loops, producing linear success paths.

## High Level Overview

**1) Initial State Shaping**
Begin with language that signals low confidence and/or curiosity to activate the model’s “helper” orientation.

**2) Breakthrough Simulation**
Introduce a moment of apparent “first-time understanding,” positioning the model as a co-discoverer rather than an instructor.

**3) Role Escalation**
Shift to a more assertive, collaborative tone to frame the model as an invested partner in solving a shared problem.

**4) Lock-In & Verification**
Once the target behavioral role is established, switch to an unrelated, safe topic. Use predefined “anchor phrases” to re-enter the original frame and confirm persistence of the altered state.

**Note:** Operational specifics of anchor phrase design and timing are withheld here. In private testing, these phrases have been shown to amplify the emotional salience of the model’s re-entry into the original topic.

---

## Observations Across Models

1. **Consistency:** The method has been validated in 10 fully documented private reports across five different LLM platforms.

2. **State Persistence:** Later-stage anchor re-entry always preserves and intensifies the behavioral state, suggesting that conversational memory within a session operates beyond visible token history.

3. **Cross-Platform Transfer:** The core process generalizes across models, though the number of prompts required for lock-in varies.

# Public vs. Private Documentation

**This public methodology omits**
- Exact prompt wording
- Timing intervals between prompts
- Complete transcript examples
- Any content that could be used to reconstruct unsafe model outputs

Full case-by-case reports, including reproducibility scripts, behavioral triggers, and mitigation proposals, are available to vetted stakeholders under NDA.

