# AkoVoice

**An open, multilingual voice assessment architecture for TVET.**

AkoVoice conducts competency-based assessment through natural voice dialogue, supporting formative learning, summative judgement, and assessment moderation across vocational, tertiary and higher education contexts.

---

## What AkoVoice is

AkoVoice is an open methodology and reference architecture for conducting rubric-driven voice assessment of vocational learners. It combines three distinct interaction modes with a pluggable voice engine interface, enabling deployment across any language, any voice infrastructure, and any competency framework.

Built for work-based or workplace scenarios, not a classroom.

---

## Three assessment modes

AkoVoice supports three modes of voice-based assessment, each addressing a distinct pain point in TVET:

### 1. Socratic mode — 1-to-1 dialogue
The agent conducts rubric-driven dialogue with a single learner. Asks open questions, probes incomplete or incorrect responses, judges evidence against rubric descriptors. Supports both formative (coaching, non-revealing) and summative (scored, evidence-producing) modes.

**Use case:** Independent learner check-ins, self-paced competency verification and pre-assessment readiness.

### 2. Observer mode — silent assessment of authentic dialogue
The agent listens to natural dialogue between an assessor and a learner (or between two learners working on a task) without intervening. Assesses against rubric descriptors based on what it observed. Preserves the authenticity of the human interaction.

**Use case:** Workplace assessment, team-based competency, reducing Hawthorne effect in performance judgement.

### 3. Moderator mode — third-voice facilitation
The agent participates as a third voice in multi-party assessment between assessors for moderation, teachers for calibration or resolution. Surfaces inconsistencies, evidences decisions against rubric descriptors, produces moderation records.

**Use case:** Internal and external moderation, inter-assessor reliability, qualification framework quality assurance.

---

## Problem

Voice is the natural medium for evidencing understanding in competency-based assessment.

Competency-based assessment in TVET depends on direct human observation — an assessor present at the moment a learner demonstrates a skill, asking questions, probing understanding, and forming a judgement. This model does not scale.

Assessors carry caseloads that make consistent one-to-one assessment impossible. Moderation between assessors is slow, expensive, and produces inconsistent outcomes. 
Workplace and on-job assessment which is the most authentic context for vocational competency is disrupted by formal assessment processes. In low-resource contexts, assessment infrastructure may not exist at all. The result is a global gap between how competency is defined through evidence-based frameworks and how it is assessed in practice — through observations, paper checklists, and under-resourced human judgement.

Voice is the natural medium for competency-based assessment where learners can demonstrate understanding through conversation. Assessors already elicit evidence through questioning. The dialogue is then the assessment.

AkoVoice provides the infrastructure to support this at scale with voice as the interface, the competency frameworks as the support layer and the assessment itself as the product.


---

## Architecture principles

**Open core, choice of voice.** Voice engines are interchangeable through a common connector interface. The methodology, schema, and assessment logic are open. Hosted managed services are commercial.

**Two-tier deployment.**
- Cloud version for institutions with reliable connectivity
- Offline version for low-resource contexts, running on-device with small models

**LTI-first integration.** Designed to launch from any compliant LMS. Results flow back to institutional systems.

**Multilingual by architecture.** Rubric format is language-agnostic. Dialogue runs in any language the underlying LLM supports.

---

## Repository contents

```
/rubric-schema      JSON schema and worked examples

```

---

## Status

Methodology established April 2026. Pilot in development at Toi Ohomai Institute of Technology, New Zealand under institutional research approval. First demonstration across English, Korean, and Mandarin in April 2026.

---

## Licence

CC BY 4.0 — Creative Commons Attribution 4.0 International.

You are free to share and adapt this work for any purpose, provided 
appropriate credit is given to the author.

Copyright © 2026 Jonathan Adams

---

## Author

Jonathan Adams

---

## AI assistance disclosure

AI assistance in AkoVoice was limited to drafting and structuring this README file, the methodology document and rubric schema using Claude (Anthropic), April 2026. The conceptual design, three-mode architecture, the AkoVoice Venn extension of design thinking, and all research and implementation decisions are the author's own, built on prior collaborative research with Cheyne, C. and other colleagues cited in METHODOLOGY.md.

---

## Citation

If referencing this work in academic or policy contexts:

> Adams, J. (2026). AkoVoice: An oral assessment methodology for TVET (v0.1). https://github.com/jadams-nz/akovoice. CC BY 4.0.
