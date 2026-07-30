# Open Genealogy Transcription Standard (OGTS): Core Standard

**Version:** 0.1  
**Status:** Outline Draft  
**Document Type:** Planned Normative  
**Last Updated:** 29 Jul 2026

---

## Outline Status

This document currently defines the proposed architecture of the OGTS Core Standard. Section descriptions identify planned scope and relationships but do not yet establish conformance requirements.

Normative requirements will be drafted and reviewed after this outline is approved.

---

## 1. Introduction

### 1.1 Purpose

Define the common, implementation-independent requirements for faithful transcription, translation, normalization, and structured extraction of historical genealogical documents.

### 1.2 Scope

Identify the document types, transformations, outputs, and implementation classes governed by the Core Standard.

### 1.3 Non-Goals

Clarify that the Core Standard does not prescribe a particular AI model, OCR engine, software architecture, user interface, genealogy database, or research conclusion.

### 1.4 Relationship to the Charter

State that the Core Standard implements the principles and scope established by the [OGTS Charter](charter.md).

### 1.5 Document Architecture and Authority

Define the intended document hierarchy:

1. Charter
2. Core Standard
3. Normative companion specifications, including the Evidence Model, Notation Standard, and Quality Assurance Framework
4. Applicable normative language or regional modules and output profiles
5. Informative reference modules, examples, and implementation guidance

Informative material does not establish conformance requirements. An extension may add scoped requirements but may not silently contradict a higher-level normative document.

### 1.6 Companion-Specification Boundaries

Summarize the responsibilities delegated to companion specifications, modules, profiles, examples, and conformance tests before presenting Core requirements.

### 1.7 Notation and Profile Precedence

Establish that the Core Standard defines semantic obligations, the Notation Standard defines canonical notation, and output profiles define serialization or compatibility adaptations. Output profiles may not redefine the meaning of canonical notation.

---

## 2. Conformance

### 2.1 Conformance Subjects

Define two conformance subjects:

- a conforming implementation, which satisfies the capabilities and behavior required by the applicable normative documents
- a conforming output, which satisfies the content and representation requirements of an identified output profile

Workflow conformance will remain deferred until the Quality Assurance Framework defines review procedures and acceptance criteria.

### 2.2 Requirement Terminology

Define the intended use of **shall**, **shall not**, **should**, **should not**, and **may** in normative clauses.

### 2.3 Applicable Requirements

Define how the Core Standard, normative companion specifications, applicable language or regional modules, and declared output profiles combine to determine conformance requirements.

Informative reference modules do not establish conformance requirements.

### 2.4 Conformance Claims

Specify the version, modules, profiles, exceptions, and limitations that a conformance claim must identify.

---

## 3. Terms and Definitions

Define the terminology required by the Core Standard, including:

- source artifact
- source representation
- observation
- transcription
- diplomatic transcription
- transliteration
- editorial intervention
- normalization
- translation
- structured extraction
- transformation
- output
- assertion
- provenance
- uncertainty
- output profile
- module
- language module
- regional module
- reference module
- interpretation
- inference
- loss or degradation
- implementation
- conformance

Terminology will initially remain in the Core Standard and may be extracted later only if its scope warrants independent treatment.

---

## 4. Conceptual Model

### 4.1 Representations and Transformations

Define the foundational lineage:

1. source artifact
2. source representation
3. observation
4. source transcription

Define transliteration, normalization, translation, and structured extraction as separate, traceable transformations that may branch from one or more preceding representations. Do not impose a universal processing order unless an applicable profile requires one.

### 4.2 Separation of Representations

Require each transformation to remain distinguishable so that normalized, translated, or interpreted content cannot be mistaken for source text.

### 4.3 Provenance Across Transformations

Define how outputs retain links to the source representation and to preceding transformation stages.

### 4.4 Human and Automated Processing

Apply the same editorial requirements to human, OCR-assisted, AI-assisted, and hybrid workflows.

---

## 5. Source Fidelity and Provenance

Define minimum requirements for:

- source identification
- repository and collection information
- item-, page-, image-, or entry-level location
- access and capture information
- source-order preservation
- completeness and coverage statements
- missing, cropped, damaged, or unavailable content
- derivative and transformed representations

---

## 6. Transcription Requirements

### 6.1 Fidelity

Define how implementations preserve original spelling, capitalization, punctuation, abbreviations, symbols, and textual order.

### 6.2 Layout and Reading Order

Define how line breaks, columns, tables, marginalia, insertions, headers, footers, and other textual regions are represented.

### 6.3 Document Layers

Distinguish printed, handwritten, stamped, sealed, annotated, and later-added content when the distinction is observable and relevant.

### 6.4 Omissions and Untranscribed Content

Require explicit treatment of illegible, obscured, damaged, blank, excluded, or intentionally untranscribed content.

### 6.5 No Silent Correction

Prohibit unmarked correction, modernization, expansion, completion, or reconciliation within the source transcription.

---

## 7. Editorial Intervention and Uncertainty

Define general requirements for:

- uncertain readings
- alternative readings
- illegible or partially legible content
- supplied text
- editorial expansions
- deletions and insertions
- damage and loss
- abbreviations and symbols
- unresolved meaning

The Core Standard will define the required meaning of editorial states. The Notation Standard will define canonical notation. An output profile may adapt serialization for a target system but may not redefine the canonical meaning.

---

## 8. Normalization Requirements

### 8.1 Non-Destructive Normalization

Require normalized content to remain separate from the source transcription.

### 8.2 Permitted Normalization

Define categories such as Unicode normalization, whitespace handling, date representation, name representation, abbreviation expansion, and target-system compatibility.

Distinguish reversible typographic normalization from semantic transformations. Name representation, abbreviation expansion, and any other transformation that adds or changes meaning must remain explicitly marked and traceable to the source transcription.

### 8.3 Declared Rules

Require implementations to identify the normalization rules and profiles they apply.

### 8.4 Target-System Compatibility

Treat substitutions required by target systems with character or encoding constraints as explicit output-profile transformations rather than changes to the source transcription.

---

## 9. Transliteration and Translation Requirements

### 9.1 Transliteration

Define requirements for:

- separation of source-script transcription and transliteration
- identification of the transliteration system or declared conventions
- preservation of source-script content
- reversible mapping where the selected system permits it
- uncertainty and characters without direct equivalents

Language- and script-specific transliteration rules will remain in language modules.

### 9.2 Translation

Define requirements for:

- separation of transcription and translation
- documentary fidelity
- preservation of ambiguity
- names and place names
- technical, legal, religious, and occupational terms
- abbreviations and supplied expansions
- uncertain translations
- language changes and mixed-language documents

Language-specific translation rules will remain in language modules.

---

## 10. Structured Extraction Requirements

### 10.1 Source-Bounded Extraction

Define how extracted data remains traceable to the text or document feature that supports it.

### 10.2 Assertions and Inferences

Distinguish explicit statements from editorial interpretation and genealogical inference.

### 10.3 Uncertainty and Alternatives

Preserve uncertainty, conflicting values, and alternative interpretations in structured output.

### 10.4 Relationship to the Evidence Model

Establish the interface between source-bounded extraction and the later Evidence Model without duplicating detailed evidence-classification rules.

---

## 11. Output Profiles and Compatibility

Define how output profiles may specify:

- required fields and ordering
- plain text, Markdown, JSON, XML, or other serializations
- serialization choices consistent with the canonical Notation Standard
- target-system constraints
- Unicode compatibility substitutions
- machine-readable provenance
- loss or degradation disclosures

Profiles may constrain representation but may not silently change source meaning or redefine canonical notation.

---

## 12. Quality Assurance and Verification

Define minimum verification hooks for:

- source-to-transcription comparison
- completeness checks
- uncertainty review
- transformation traceability
- translation review
- structured-data validation
- profile validation
- error reporting and visible correction
- reproducibility testing

Detailed review procedures and acceptance criteria will be defined in the Quality Assurance Framework.

---

## 13. Privacy and Ethical Handling

### 13.1 Faithful Preservation

Define how a canonical transcription faithfully preserves source content, including sensitive content, without silent deletion or alteration.

### 13.2 Access and Disclosure

Define how access restrictions, redaction, data minimization, and publication-safe outputs remain separate from the canonical transcription and are explicitly identified as controlled derivatives.

### 13.3 Ethical Requirements

Define applicable requirements for:

- living and potentially living people
- sensitive personal, medical, financial, institutional, or genetic information
- informed consent where applicable
- respectful treatment of historically sensitive material
- disclosure of AI assistance and human responsibility

---

## 14. Professional Standards Alignment

### 14.1 Genealogical Proof Standard

Explain how OGTS outputs support research conducted in accordance with the Genealogical Proof Standard by preserving provenance, citations, uncertainty, conflicts, and the distinction between observation and interpretation.

### 14.2 Scope Boundary

State that the Genealogical Proof Standard evaluates a complete research process and that OGTS conformance alone does not establish that a genealogical conclusion meets that standard.

### 14.3 Ethics

Align applicable requirements with the ethical standards published by the Board for Certification of Genealogists, including accurate quotation, source identification, visible editorial intervention, substantiated claims, attribution, and privacy.

### 14.4 No Endorsement Claim

State that alignment does not imply certification, endorsement, or affiliation.

---

## 15. Modularity and Extensibility

### 15.1 Language and Regional Modules

Define how language- and region-specific rules extend the Core Standard without changing its general requirements.

### 15.2 Reference Modules

Define how informative resources such as abbreviation tables, occupation lists, date conventions, WGfF references, and Unicode mappings support implementations.

Reference modules are informative and do not establish conformance requirements.

### 15.3 Extension Rules

Define how extensions identify their scope, dependencies, status, and compatibility with the Core Standard.

---

## 16. Versioning and Change Control

Define:

- document versions and statuses
- compatibility expectations
- deprecation and supersession
- change documentation
- treatment of normative and informative revisions

Formal approval roles and workflows remain future governance work.

---

## 17. Informative References and Related Work

Planned informative references include:

- Board for Certification of Genealogists, *Genealogy Standards*
- [Board for Certification of Genealogists ethics and standards](https://bcgcertification.org/ethics-standards)
- Elizabeth Shown Mills, *Evidence Explained*
- [Steve Little's Open Genealogy transcription resources](https://github.com/DigitalArchivst/Open-Genealogy/tree/main/transcription)
- [Genealogical Research Assistant v9.2.0](https://github.com/DigitalArchivst/Open-Genealogy/tree/v9.2.0/skills/gra)

Related work may inform OGTS design but does not become a normative dependency. Requirements must be expressed in original, implementation-independent language with appropriate attribution and respect for applicable licenses.

---

## Appendix A. Planned GPS Crosswalk

Map OGTS requirements to the five elements of the Genealogical Proof Standard while identifying elements that remain outside the scope of transcription conformance.

---

## Appendix B. Planned Conformance Checklist

Provide an informative checklist linking each mandatory Core Standard requirement to a verification method and, where applicable, a conformance test.

