# AkoVoice - the approach

*v0.2, September 2026. CC BY 4.0. Jonathan Adams.*

## 1. Problem

Competency-based assessment in TVET depends on an assessor being present
when a learner demonstrates a skill — observing, questioning, probing,
judging. Assessor time at that moment is the bottleneck, and written
evidence captures little of the verbal reasoning that vocational work
actually involves. Voice is already how assessors elicit evidence.
AkoVoice asks whether structured voice dialogue, bounded by a rubric,
can widen access to that kind of assessment.

## 2. Voice or oral assessment modes

**Socratic.** The agent conducts a 1-to-1 dialogue with a learner: one
opening question per criterion and probes for incomplete answers,
no revealing of correct answers. Formative mode coaches without
grading and summative mode produces a suggested or provisional judgement for assessor
to mark or sign-off. 

**Observer.** The agent listens to a learner's authentic dialogue, or assessor and
learner, or learners together without intervening, and surfaces
evidence against the rubric from what it heard. Preserves the interaction to be as natural as possible. 

**Moderator.** The agent can be a third voice in multi-party assessment
or calibration, surfaces disagreement between assessors, and produces an
record of moderation.


## 3.  Two ways of running Socratic mode

*Structured.* An authored question bank with probes and it can run offline, useful for noisy environments.

*Live.* A real-time conversational agent bounded by the rubric. Online or offline modes. Live voice requires hardware with sufficient memory to run natural language dialogue.

Both consume the same rubric and feed the same judgement step.

## 4. Judgement

For each criterion the AI cites transcript turns, proposes a level against the rubric's own scheme (binary,
three-level etc), and records its reasoning.
An assessor reviews the evidence and can listen to the evidence and signs off. The AI never issues a final result.


## 5. Rubric schema

`rubric-schema/` holds the JSON Schema and worked examples. A rubric
declares its own judgement scheme, language, mode, jurisdiction and
governance fields. Text is Unicode NFC. The schema is versioned
independently of any implementation.

## 6. Governance

- Consent — explicit, documented, revocable.
- Data sovereignty — Māori data sovereignty (Te Mana Raraunga) and
  Te Tiriti o Waitangi obligations in Aotearoa; local equivalents elsewhere.
- Voice as identity — recordings are not used for model training or
  biometric profiling.
- Right to human assessment — required for any deployment.

## 7. Implementation note

The working implementation is deliberately conventional with commodity
hardware, open-weight models, swappable components so the approach
can be adopted, audited or re-implemented independently of any vendor,
including the author. It is described in the paper, the code is not
part of this release.

---

## References

Adams, J., Cheyne, C., & Burrell, J. (2024). *AI design and policy for education*. Presented at the New Zealand AI in Higher Education Symposium 2024, University of Otago.

Adams, J., & Riddle, K. (2023). AI Design Issues in Education. In J. L. Savage, J. Hoffman, & M. Shannon (Eds.), *Proceedings: ITP Research Symposium 2022* (pp. 119–131). ePress, Unitec | Te Pūkenga. https://doi.org/10.34074/proc.2302012

Mathews, P., Adams, J., & Cheyne, C. (2025). Personalised Learning for Nursing Education With Gen-AI Chatbots. *Nursing Praxis in Aotearoa New Zealand*, *41*(1), 38–48. https://doi.org/10.36951/001c.151665

New Zealand Government. (2020). *Algorithm charter for Aotearoa New Zealand*. Stats NZ. https://www.data.govt.nz/assets/data-ethics/algorithm/Algorithm-Charter-2020_Final-English-1.pdf

---

## Citation

> Adams, J. (2026). AkoVoice: oral assessment in TVET (v0.2). https://github.com/jadams-nz/akovoice. CC BY 4.0.

---

*Copyright © 2026 Jonathan Adams.*
