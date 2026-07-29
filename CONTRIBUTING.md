# Contributing to the Open Genealogy Transcription Standard (OGTS)

Thank you for your interest in contributing to the Open Genealogy Transcription Standard (OGTS).

OGTS is an open, vendor-neutral specification for the transcription, translation, normalization, and structured extraction of historical genealogical documents. The project seeks to establish clear editorial standards that can be implemented by researchers, software developers, OCR systems, and AI platforms.

## Guiding Principle

Contributors should remember that OGTS is a **standard**, not an implementation.

The purpose of the project is to define **what conforming implementations must do**, rather than how a particular software application or AI model should operate.

---

# Core Values

All contributions should support the following principles:

- Preserve the historical source as the primary evidence.
- Separate observation from interpretation.
- Make editorial decisions transparent.
- Preserve uncertainty.
- Promote reproducible results.
- Remain implementation-independent whenever possible.

---

# Normative vs. Informative Documents

OGTS distinguishes between two classes of documents.

## Normative Documents

Normative documents define requirements that conforming implementations must satisfy.

Examples include:

- Charter
- Core Standard
- Evidence Model
- Notation Standard
- Output Profiles

Normative language should use terms such as:

- **shall**
- **shall not**
- **should**
- **should not**
- **may**

These terms are used intentionally to indicate the strength of a requirement.

## Informative Documents

Informative documents explain, illustrate, or provide background.

Examples include:

- Examples
- Design Notes
- Historical Background
- Tutorials
- Implementation Guidance

Informative documents do not establish conformance requirements.

---

# Before Proposing a Change

Ask the following questions:

1. Does this improve the standard?
2. Is the proposal implementation-independent?
3. Does it preserve the Charter?
4. Can the requirement be tested?
5. Would multiple independent implementations reach substantially similar results?

If the answer to any of these questions is "no," the proposal may need refinement.

---

# Language Modules

Language-specific rules belong in language modules rather than the Core Standard.

For example:

- German
- Latin
- Hebrew
- Dutch
- Polish

The Core Standard should remain language-independent whenever practical.

---

# Reference Modules

Reference material that supports implementations without changing the Core Standard should be placed in reference modules.

Examples include:

- Occupation lists
- Abbreviation tables
- Unicode mappings
- Date conventions

---

# Editorial Philosophy

OGTS favors explicit editorial practice over silent correction.

Implementations should avoid silently:

- correcting spelling
- modernizing language
- expanding abbreviations
- resolving ambiguity
- inferring relationships

Whenever editorial intervention occurs, it should be made visible to the reader.

---

# Versioning

Normative documents include version and status information.

Typical statuses include:

- Draft
- Review
- Approved
- Superseded

---

# Current Governance Scope

The initial governance foundation consists of the Project Charter, contribution guidance, and license.

Governance remains intentionally minimal at this stage. OGTS has not yet defined formal maintainer roles, decision-making procedures, or an approval workflow. The guidance in this document should not be interpreted as a formal approval system.

---

# Discussion

Constructive discussion is encouraged.

Disagreements should focus on evidence, editorial practice, reproducibility, and the goals of the standard rather than the behavior of any specific AI system or software platform.

---

# Code of Conduct

All contributors are expected to engage respectfully and professionally.

The goal of OGTS is collaborative development of an open standard that benefits the genealogy community.
