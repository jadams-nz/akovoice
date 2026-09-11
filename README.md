# AkoVoice

Open, multilingual oral assessment in TVET.

AkoVoice conducts competency-based assessment through natural voice dialogue (or text and learner voice in noisy environments), supporting formative learning, summative judgement, and assessment moderation in workplace or tertiary education settings.

## What AkoVoice is

AkoVoice is an open reference implementation using open licensed software, for conducting rubric-driven voice assessment of learners. It combines three interaction modes designed to support deployment across different languages, voice engines, and competency frameworks.

It is offered as a documented working example of using voice assessment, released openly for others to adapt or replicate. It is not a productised or SaaS platform.

## Three assessment modes

AkoVoice describes three modes of voice-based assessment. Socratic dialogue and observational assessment are long established, and moderation is standard practice in qualifications assurance.

### 1. Socratic mode: 1-to-1 dialogue

The agent conducts rubric-driven dialogue with a single learner. It asks open questions, and can probe incomplete or unclear responses, judges evidence against rubric descriptors. This mode supports both formative and summative assessments.

Use case: independent learner check-ins, self-paced competency verification, pre-assessment readiness.

Status: deployed and demonstrated.

### 2. Observer mode: silent assessment of authentic dialogue

The agent listens to natural dialogue either from the learner, or between an assessor and a learner, or between learners working on a task, without intervening. It assesses against rubric descriptors based on what it heard, preserving the authenticity of the human interaction.

Use case: workplace assessment, team-based competency and the objective is to be as unobtrusive as possible, running on a mobile device, thereby reducing any 'performance' behaviour from learners when they know they are being judged or observed (the Hawthorne effect), to provide as natural and authentic assessment as possible.

Status: testing in workshops from April 26, running as assessment in workshops from 9th June 2026.

### 3. Moderator mode: third-voice facilitation

The agent participates as a third voice in multi-party assessment between assessors for moderation, or between teachers for calibration. The objective is to surface inconsistencies or evidence decisions and produce a moderation record.

Use case: internal and external moderation, inter-assessor reliability, qualification-framework quality assurance.

Status: specified but not used.

## Problem

Competency-based assessment in TVET depends on direct human observation with an assessor present at the moment a learner demonstrates a skill, asking questions, probing understanding, forming a judgement. Consistent scaled one-to-one assessment is hard, and in low-resource contexts infrastructure may be limited. Voice is a natural medium for evidencing understanding in competency-based assessment. Learners can demonstrate understanding through conversation; assessors already elicit evidence through questioning. AkoVoice is built to show how voice can widen access to this kind of assessment.

## Design principles

Open methodology, engine-agnostic schema and controls for data residency and student control over their voice and assessment. The methodology, rubric schema, and assessment logic are open under CC BY 4.0. The current reference implementation uses an online optional and offline field kit (everything on one laptop), local open-weight models — Mistral 7B, Qwen3-4B, faster-whisper, Chatterbox — serving its own Wi-Fi/DNS so a class or cohort with phones works, with no internet.

The rubric schema is language-agnostic, and dialogue can run in any language the underlying engine supports. Demonstrated to date in English, Korean, and Mandarin.

Accessibility - AkoVoice can run with first-language responses (L1) to second-language (L2) questions for NESB learners, producing a report for the assessor in the assessors own (L1) language. The aim of this is to help gauge the level of domain knowledge of a learner, separate from a language fluency requirement.

Governance commitments. Informed consent (explicit, documented, revocable); data sovereignty; voice recordings are not used for model training or biometric profiling; and the right to human assessment. See METHODOLOGY.md.

## Repository contents

```
/rubric-schema      JSON schema and worked examples
METHODOLOGY.md      Methodology, modes, governance, theoretical grounding
README.md           This file
LICENSE             CC BY 4.0
```

## Status

Approach published April 2026 (v0.2). A working implementation using text questions and voice responses (observer) has been used with Auto and engineering trades cohorts at a New Zealand ITP running online and, since June 2026, fully offline on a single laptop with open-weight models. The schematic included in paper Sept '26.

Socratic mode has been demonstrated end-to-end in English, and Korean and Mandarin and has been tested in a limited setting;
Moderator mode is described and built but not used in production. This is not a productised platform.

## Licence

CC BY 4.0, Creative Commons Attribution 4.0 International. You are free to share and adapt this work for any purpose, provided appropriate credit is given to the author.

Copyright © 2026 Jonathan Adams

## AI assistance disclosure

AI assistance in AkoVoice was limited to drafting and structuring this README, the methodology document, and the rubric schema using Claude (Anthropic), 2026.

The conceptual design, the three-mode taxonomy, and all research and implementation decisions are the author's own. The three-mode framing draws on prior collaborative research on design thinking applied to AI in education (Adams, Cheyne & Burrell, 2024) and other work cited in METHODOLOGY.md.

## Citation

If referencing this work in academic contexts:

> Adams, J. (2026). AkoVoice: oral assessment in TVET (v0.2). https://github.com/jadams-nz/akovoice. CC BY 4.0.
