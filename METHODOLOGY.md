# AkoVoice Methodology

*Version 0.1 — 25 April 2026*

This document specifies the AkoVoice methodology for voice-based competency assessment in technical and vocational education and training (TVET). It is released under CC BY 4.0 as the core intellectual contribution of this project, alongside the rubric schema and the Voice Assessment Connector (VAC) interface specification.

AkoVoice is an applied demonstration of design-thinking principles for AI in education (Adams, Cheyne & Burrell, 2024). Where that earlier paper argued that AI development should begin with stakeholder desirability rather than technological feasibility, this methodology operationalises that argument in the domain of TVET assessment.

---

## The problem

TVET assessment globally faces persistent, expensive problems that technology has not yet solved:

- Assessors cannot be beside every learner at every moment
- Moderation between assessors is slow, inconsistent, and costly to arrange
- Workplace and on-the-job assessment relies on authentic observation that can be contaminated by formal assessment processes
- Low-resource contexts lack assessment infrastructure entirely

Voice is the natural medium for competency-based assessment. Learners explain, justify, and demonstrate understanding through conversation with assessors. AkoVoice treats voice as the interface, competency rubrics as the support layer and the assessment event as the designed outcome.

---

## Foundational principles

AkoVoice is built on four principles, each based on prior published work and extended to the voice assessment context.

**1. Desirability before feasibility.**

Conventional AI development asks what is technologically possible and then seeks human problems to apply it to. Design thinking inverts this sequence, starting with stakeholder needs and allowing feasibility and viability to follow (Adams, Cheyne & Burrell, 2024). AkoVoice begins with the practical problem of assessor capacity in workshops, not with the availability of voice AI.

**2. The rubric is the operational specification.**

A competency rubric in AkoVoice is not a reference document for human assessors. It is the operational specification that determines what the agent listens for, probes, and judges. This mirrors the argument in Mathews, Adams & Cheyne (2025) that conversational AI in education must be anchored to curated institutional content and pedagogical intent.

**3. Voice infrastructure is interchangeable; methodology is the contribution.**

Speech-to-text, text-to-speech, and large language model components are evolving rapidly and vendor-dependent. AkoVoice specifies a connector interface so institutions deploy using any compliant voice engine — commercial, open source, cloud, or on-device. The open methodology and rubric schema are consistent. This separation addresses vendor lock-in concerns and cultural bias concerns raised in Adams & Riddle (2023) by allowing culturally appropriate voice engines to be substituted without changing the assessment logic.

**4. Mode determines behaviour.**

The same underlying engine supports three distinct assessment modes — Socratic, Observer, and Moderator — by varying the prompting methodology and turn-taking logic. The architecture does not change between modes. This enables one open methodology to address formative coaching, summative judgement, authentic workplace assessment, and assessment moderation within a unified framework.

---

## The AkoVoice Venn: a design-thinking extension

The established design-thinking framework applied to designing AI, articulated in Adams, Cheyne & Burrell (2024) positions human-centred AI at the intersection of Desirability, Feasibility, and Viability, with the centre of the Venn diagram representing solutions that meet all three criteria:

```
                   Desirable
                  (human-centric)
                       /\
                      /  \
                     /    \
                    /      \
                   /  [AI   \
                  /   fit]   \
                 /____________\
               Feasible     Viable
              (technology) (business)
```

AkoVoice extends this framework into the specific domain of assessment dialogue. Where the design-thinking Venn places Desirability at the top as the human-centred starting point, the AkoVoice Venn places the Student at the top as the learner-centred starting point. This is the specific educational application of the broader design principle. The three stakeholder perspectives are the Student (the assessment serves the learner), the Assessor (who applies the rubric and makes judgements), and a third party who is either an Observer (capturing authentic dialogue) or a Moderator (facilitating multi-party judgement):

```
                    Student
               (learning, evidence,
                understanding)
                       /\
                      /  \
                     /    \
                    /      \
                   / [Rubric-\
                  /  driven   \
                 /  dialogue]  \
                /________________\
             Assessor          Observer/
           (rubric,             Moderator
           judgement)         (authenticity,
                               consistency)
```

The centre of the AkoVoice Venn is the designed assessment event — the moment where rubric descriptors are evidenced through dialogue, where the student demonstrates understanding in authentic form, and where a third-party role (silent or facilitative) preserves either authenticity or consistency for the learner's benefit.

Placing the Student at the apex is a deliberate choice. The assessment exists to serve the learner's progression. The assessor's role is facilitative of that progression, not primary. The observer or moderator role exists to protect fairness for the learner. Design thinking centres the human user and design thinking applied to assessment centres the learner specifically.

Each of AkoVoice's three modes represents a different emphasis within this Venn:

- **Socratic mode** collapses to Student and Assessor (the Observer/Moderator position is held by the agent itself, which takes the assessor role)
- **Observer mode** preserves all three, with the agent in the Observer role listening silently to authentic Student and Assessor dialogue
- **Moderator mode** centres the third-party role, with the agent facilitating consistency across multiple Assessor perspectives for the learner's benefit

---

## The three modes

### Mode 1: Socratic

The agent conducts one-to-one dialogue with a single learner. It asks open questions derived from rubric criteria, listens to responses, and probes incomplete or incorrect answers without revealing correct responses.

**Formative sub-mode:** The agent coaches understanding. Wrong answers trigger probing questions. Correct answers are affirmed. No final mark or grade is produced as the goal is learner development. This sub-mode draws directly on the chatbot configuration approach demonstrated in Mathews, Adams & Cheyne (2025) and extended from text to voice modality.

**Summative sub-mode:** The agent assesses once per criterion. Responses are scored against rubric descriptors and evidence is recorded. A provisional judgement is produced for assessor review and sign-off. Coaching is withheld until after assessment completes.

**Turn-taking:** Alternation between agent and learner. The agent speaks, learner responds then the agent evaluates and proceeds.

**Output:** Per-criterion evidence, per-criterion judgement (in summative mode), full transcript and session summary.

---

### Mode 2: Observer

The agent listens silently to authentic dialogue between two or more human participants — typically an assessor and a learner, or two learners collaborating on a task. The agent does not speak. It captures the dialogue, identifies evidence against rubric descriptors and produces an assessment based on what it observed.

**Purpose:** Preserves the authenticity of human interaction. Formal assessment often distorts the behaviour being assessed as learners perform for the assessor or underperform in an artificial assessment condition. Assessors constrain their questioning to scorable items. Observer mode removes the agent from the interaction entirely, enabling competency to be evidenced in natural workplace or workshop contexts.

**Turn-taking:** None. The agent does not participate. It captures and processes.

**Output:** A transcript with speaker evidence mapping to criteria, and a judgement against rubric (if summative) with annotated recommendations for assessor review.

**Governance implications:** Observer mode requires explicit informed consent from all parties before recording. AkoVoice implementations must enforce consent capture as a pre-session requirement. Data retention policies must be documented and auditable. These requirements reflect the provenance and data sovereignty principles articulated in Adams & Riddle (2023).

---

### Mode 3: Moderator

The agent participates as a third voice in multi-party assessment dialogue. It surfaces inconsistencies between assessor judgements, probes reasoning, ensures rubric descriptors are applied consistently, and produces a moderation record. The agent does not replace human judgement.

**Use contexts:**
- Internal moderation between assessors within an institution
- External moderation between institutions
- Dispute resolution where learner judgements are contested
- Calibration sessions where assessors benchmark their judgements

**Turn-taking:** Facilitated. The agent controls turn taking by inviting each human participant to speak, and interjects to probe or clarify against rubric descriptors.

**Output:** Structured moderation record documenting each assessor's judgement, points of agreement and disagreement, rubric descriptors cited, final moderated outcome, evidence trail.

**Governance implications:** Moderator mode produces records that may contribute to qualifications. AkoVoice implementations must treat moderation output as auditable and tamper-evident. Regulatory compliance requirements vary by jurisdiction (NZQA, ASQA, Ofqual, and equivalents) and are the responsibility of the implementing institution.

---

## The assessment loop

Regardless of mode, AkoVoice sessions follow a common assessment loop:

**1. Session initialisation**
- Rubric loaded
- Mode and sub-mode selected
- Participants identified
- Consent confirmed (required for Observer and Moderator modes)
- Voice engine initialised via the VAC interface

**2. Dialogue execution**
- Mode-specific turn-taking applied
- Utterances captured and transcribed in real time
- Rubric criteria matched to utterances as they occur
- Probes triggered per mode rules

**3. Evidence capture**
- Each utterance evaluated against rubric descriptors
- Criterion coverage tracked
- Gaps identified for further probing or noted for assessor review

**4. Session closure**
- Mode-specific output produced
- Transcript archived
- Evidence trail recorded
- Downstream integration (LMS, gradebook, moderation system) triggered where applicable

---

## Rubric design for voice assessment

Rubrics designed for paper-based assessment do not translate directly to voice dialogue. AkoVoice introduces design considerations for voice-native rubrics:

**Descriptors must be verbally evidenced.** A criterion like "produces a weld with correct penetration" is observable but not verbally evidenced. AkoVoice rubrics restate such criteria as explanations or justifications: "explains how they would verify correct weld penetration." Voice assessment evidences understanding and reasoning, complementing rather than replacing practical performance assessment.

**Criteria must support probing.** Each criterion includes probe prompts — alternatives the agent can use when a response is incomplete. Probes are authored by the rubric designer, not generated by the learner.

**Descriptors must support level differentiation.** Where a rubric distinguishes achieved, merit, and excellence levels, descriptors must be verbally distinguishable. "Demonstrates mastery" is insufficient. "Explains the underlying principles and relates them to three different practical scenarios" is assessable in dialogue.

---

## The rubric schema

AkoVoice rubrics are expressed in a structured JSON schema supporting all three modes and both formative and summative sub-modes. The schema is specified in `rubric-schema/v0.1.json` in this repository.

Key elements:
- Mode configuration (Socratic, Observer, Moderator)
- Sub-mode configuration (formative or summative for Socratic)
- Criterion specifications with level descriptors
- Probe prompts per criterion
- Language and cultural adaptation fields
- Governance metadata (consent requirements, data retention, jurisdiction)

---

## The Voice Assessment Connector (VAC) interface

The AkoVoice methodology envisages a pluggable voice engine interface — the Voice Assessment Connector (VAC) — allowing any voice platform (commercial, open source, cloud, or on-device) to host AkoVoice sessions without changes to the rubric schema or assessment logic.

The VAC interface specification is planned for v0.2 of this methodology, following initial pilot deployment using a single voice engine configuration. Deferring the interface specification until after real-world deployment ensures the abstraction reflects genuine integration needs rather than speculative architecture.

The principle in v0.1 is that the methodology is the contribution and voice infrastructure or technology is a commodity.

---

## Pedagogical positioning

AkoVoice is a tool, not a replacement for assessors. The methodology explicitly preserves human judgement at every consequential decision point:

- In Socratic summative mode, the agent produces a provisional judgement that assessors review and sign off
- In Observer mode, the agent produces evidence and recommendations; assessors make the final judgement
- In Moderator mode, the agent facilitates human assessors reaching consensus; it does not cast a decisive vote

AkoVoice is designed to work within existing assessment authority structures while materially improving their capacity.

---

## Governance and ethical considerations

Voice assessment at scale raises questions that cannot be addressed by technology alone. The governance principles below are normative commitments in this methodology, reflecting the framework developed in Adams & Riddle (2023) for AI in education in Aotearoa New Zealand and aligned with the NZ Algorithm Charter (New Zealand Government, 2020).

**Consent.** All participants must provide informed consent for recording and assessment. Consent must be explicit, documented, and revocable. Observer and Moderator modes cannot operate without multi-party consent.

**Voice as identity.** The voice of every participant (student, assessor, observer) is a personal and cultural expression that belongs to them and the heritage they carry. Voice recordings and transcripts collected through AkoVoice sessions are assessment evidence only. They must not be used to train, fine-tune, or improve AI models; to build voice profiles or biometric identifiers; or for any commercial purpose beyond the assessment for which consent was given. This principle applies regardless of consent status. Consent to be assessed does not constitute consent to surrender voice as data.

**Data sovereignty.** Institutional and national data residency requirements must be respected. In Aotearoa New Zealand, this includes respecting Māori data sovereignty principles and Te Tiriti o Waitangi obligations. AkoVoice's pluggable architecture supports local deployment for jurisdictions requiring it.

**Bias and fairness.** LLM-driven assessment may encode biases related to accent, dialect, vocabulary, or cultural expression. Implementations must include ongoing bias audit and adjustment, with particular attention to minority language and dialect speakers.

**Transparency.** Learners must be informed when they are being assessed by an agent, in what mode, and how their data will be used.

**Right to human assessment.** Learners retain the right to request human assessment as an alternative to agent-based assessment. This is a non-negotiable principle in this methodology.

Implementations that violate these principles are not compliant AkoVoice deployments, regardless of technical conformance to the rubric schema or VAC interface.

---

## AI assistance disclosure

The conceptual design, three-mode architecture, the AkoVoice Venn extension of design thinking, and all research and implementation decisions are the author's own, built on prior collaborative research with Cheyne, C. and other colleagues cited herein.  
AI assistance in AkoVoice was limited to drafting and structuring the README, this methodology document, and the rubric schema using Claude (Anthropic), April 2026.
This disclosure reflects a principle of the AkoVoice methodology: transparency in AI use is a precondition of ethical deployment.

---

## Status and development

This methodology is released as version 0.1. It will evolve based on pilot findings from Toi Ohomai Institute of Technology and subsequent deployments. Substantive changes will be documented with version history.

Community contributions are welcomed via GitHub issues and pull requests. Governance of the methodology remains with the author; contributions are evaluated against the foundational principles above.

A formal paper developing these ideas in full academic form is planned for submission late-2026, followed by peer-reviewed publication with pilot data from the deployments.

---

## References

Adams, J., Cheyne, C., & Burrell, J. (2024). *AI design and policy for education*. Presented at the New Zealand AI in Higher Education Symposium 2024, University of Otago.

Adams, J., & Riddle, K. (2023). AI Design Issues in Education. In J. L. Savage, J. Hoffman, & M. Shannon (Eds.), *Proceedings: ITP Research Symposium 2022* (pp. 119–131). ePress, Unitec | Te Pūkenga. https://doi.org/10.34074/proc.2302012

Mathews, P., Adams, J., & Cheyne, C. (2025). Personalised Learning for Nursing Education With Gen-AI Chatbots. *Nursing Praxis in Aotearoa New Zealand*, *41*(1), 38–48. https://doi.org/10.36951/001c.151665

New Zealand Government. (2020). *Algorithm charter for Aotearoa New Zealand*. Stats NZ. https://www.data.govt.nz/assets/data-ethics/algorithm/Algorithm-Charter-2020_Final-English-1.pdf

---

## Citation

> Adams, J. (2026). AkoVoice: An oral assessment methodology for TVET (v0.1). https://github.com/jadams-nz/akovoice. CC BY 4.0.

---

*Copyright © 2026 Jonathan Adams.*