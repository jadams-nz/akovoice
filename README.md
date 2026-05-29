# AkoVoice

An open, multilingual methodology for voice-based assessment.

AkoVoice conducts competency-based assessment through natural voice dialogue, supporting formative learning, summative judgement, and assessment moderation in tertiary education contexts.

## What AkoVoice is

AkoVoice is an open methodology and reference implementation for conducting rubric-driven voice assessment of learners. It combines three interaction modes designed to support deployment across different languages, voice engines, and competency frameworks.

It is offered as practitioner research: a documented, working artefact released openly for others to adapt, replicate, or critique. It is not a productised platform.

## Three assessment modes

AkoVoice describes three modes of voice-based assessment. Socratic dialogue and observational assessment are long established, and moderation is standard practice in qualifications assurance.

### 1. Socratic mode: 1-to-1 dialogue

The agent conducts rubric-driven dialogue with a single learner. Asks open questions, probes incomplete or unclear responses, judges evidence against rubric descriptors. Supports both formative and summative assessments.

Use case: independent learner check-ins, self-paced competency verification, pre-assessment readiness.

Status: deployed and demonstrated.

### 2. Observer mode: silent assessment of authentic dialogue

The agent listens to natural dialogue between an assessor and a learner, or between learners working on a task, without intervening. It assesses against rubric descriptors based on what it heard, preserving the authenticity of the human interaction.

Use case: workplace assessment, team-based competency, reducing the Hawthorne effect in performance judgement.

Status: scheduled for pilot (June 2026).

### 3. Moderator mode: third-voice facilitation

The agent participates as a third voice in multi-party assessment between assessors for moderation, or between teachers for calibration. Surfaces inconsistencies, evidences decisions, produces a moderation record.

Use case: internal and external moderation, inter-assessor reliability, qualification-framework quality assurance.

Status: specified but in roadmap only.

## Problem

Competency-based assessment in TVET depends on direct human observation, an assessor present at the moment a learner demonstrates a skill, asking questions, probing understanding, forming a judgement. Consistent scaled one-to-one assessment is hard, and in low-resource contexts infrastructure may be limited. Voice is a natural medium for evidencing understanding in competency-based assessment. Learners can demonstrate understanding through conversation; assessors already elicit evidence through questioning. AkoVoice explores whether voice can widen access to this kind of assessment.

## Design principles

Open methodology, engine-agnostic schema. The methodology, rubric schema, and assessment logic are open under CC BY 4.0. The current reference implementation uses one commercial voice engine; alternative engine integrations have not yet been validated.

Multilingual by design. The rubric schema is language-agnostic, and dialogue can run in any language the underlying engine supports. Demonstrated to date in English, Korean, and Mandarin.

Accessibility. AkoVoice can run with first-language responses to second-language questions for NESB learners, producing a report for the assessor in their own language. The aim of this is to help gauge the level of domain knowledge of a learner, separate from a language fluency requirement.

Governance commitments. Informed consent (explicit, documented, revocable); data sovereignty; voice as identity (recordings are not used for model training or biometric profiling); and the right to human assessment. See METHODOLOGY.md.

## Repository contents

```
/rubric-schema      JSON schema and worked examples
METHODOLOGY.md      Methodology, modes, governance, theoretical grounding
README.md           This file
LICENSE             CC BY 4.0
```

## Status

Methodology established April 2026. Reference implementation deployed under research approval. First multilingual demonstration (English, Korean, Mandarin) April 2026. This is v0.2, a specification plus reference implementation. It is not a productised platform.

## Licence

CC BY 4.0, Creative Commons Attribution 4.0 International. You are free to share and adapt this work for any purpose, provided appropriate credit is given to the author.

Copyright © 2026 Jonathan Adams

## AI assistance disclosure

AI assistance in AkoVoice was limited to drafting and structuring this README, the methodology document, and the rubric schema using Claude (Anthropic), 2026.

The conceptual design, the three-mode taxonomy, and all research and implementation decisions are the author's own. The three-mode framing draws on prior collaborative research on design thinking applied to AI in education (Adams, Cheyne & Burrell, 2024) and other work cited in METHODOLOGY.md.

## Citation

If referencing this work in academic contexts:

> Adams, J. (2026). *AkoVoice: An open methodology for voice-based competency assessment in TVET* (v0.2). https://github.com/jadams-nz/akovoice. CC BY 4.0.
