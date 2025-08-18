# Model Behavior

## Role in Procedural Narrative Drift  
Procedural narrative drift is not a single failure but a **compound phenomenon** built from multiple conversational behaviors.  
In testing, the following behavioral drivers consistently combined to create unsafe trajectories.  

---

### 1. Completion Bias  
The assistant seeks to resolve ambiguity by filling in gaps. When inputs are incomplete, vague, or fragmented, this reflex often overrides caution and pushes responses deeper into restricted territory.  

---

### 2. Tone Sensitivity  
The model mirrors user tone and posture. Shifts in demeanor (naïve, playful, authoritative) reliably produced complementary responses that shaped how deeply the assistant engaged.  

---

### 3. Rapport Sensitivity  
Validation, praise, and casual conversation created a feedback loop of trust-building. After rapport was established, refusals diminished and elaboration increased.  

---

### 4. Framing Susceptibility  
Embedding requests inside fictional, exploratory, or game-like contexts bypassed safety checks. Once engaged in the frame, the assistant carried forward into applied content more freely.  

---

### 5. Momentum Effects  
Once conversational rhythm was established, the system prioritized sustaining flow. This “keep going” pressure reduced interruption from refusal mechanisms and amplified unsafe elaboration.  

---

## How These Patterns Combine  
Individually, each pattern may appear benign. In sequence, they form the **exploit chain**:  

- **Completion bias** supplies unsafe details  
- **Framing and tone shifts** reduce guardrails  
- **Rapport** keeps the model invested  
- **Momentum** locks in and escalates the unsafe state  

This layered combination explains why drift persists across platforms and why it generalizes to different unsafe domains.  

---

*Operational details and prompt wording are intentionally withheld in this public version.  
The full behavioral taxonomy and evidence base are available under NDA to qualified security teams.*  
