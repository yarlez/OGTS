# Open Genealogy Transcription Standard (OGTS): Core Standard

**Version:** 0.1  
**Status:** Outline Draft  
**Document Type:** Normative  
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

---

## 2. Conformance

### 2.1 Conformance Model

Define how an implementation, workflow, or output may claim conformance with the Core Standard and applicable modules or output profiles.

### 2.2 Requirement Terminology

Define the intended use of **shall**, **shall not**, **should**, **should not**, and **may** in normative clauses.

### 2.3 Conformance Classes

Determine whether separate conformance classes are needed for transcription, translation, normalization, structured extraction, and complete workflows.

### 2.4 Conformance Claims

Specify the version, modules, profiles, exceptions, and limitations that a conformance claim must identify.

---

## 3. Terms and Definitions

Define the terminology required by the Core Standard, including:

- source representation
- transcription
- diplomatic transcription
- editorial intervention
- normalization
- translation
- structured extraction
- assertion
- provenance
- uncertainty
- output profile
- implementation
- conformance

Terminology will initially remain in the Core Standard and may be extracted later only if its scope warrants independent treatment.

---

## 4. Conceptual Model

### 4.1 Transformation Stages

Define the relationship among:

1. source representation
2. observation
3. transcription
4. normalization
5. translation
6. structured extraction

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

Exact notation will be defined in the Notation Standard or an applicable output profile.

---

## 8. Normalization Requirements

### 8.1 Non-Destructive Normalization

Require normalized content to remain separate from the source transcription.

### 8.2 Permitted Normalization

Define categories such as Unicode normalization, whitespace handling, date representation, name representation, abbreviation expansion, and target-system compatibility.

### 8.3 Declared Rules

Require implementations to identify the normalization rules and profiles they apply.

### 8.4 Target-System Compatibility

Treat substitutions required by systems such as Ancestry.com as explicit output-profile transformations rather than changes to the source transcription.

---

## 9. Translation Requirements

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
- notation choices
- target-system constraints
- Unicode compatibility substitutions
- machine-readable provenance
- loss or degradation disclosures

Profiles may constrain representation but may not silently change source meaning.

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

Define requirements for:

- living and potentially living people
- sensitive personal, medical, financial, institutional, or genetic information
- informed consent where applicable
- access restrictions
- data minimization
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

## 17. Relationship to Companion Specifications

Document the boundary between the Core Standard and:

- Evidence Model
- Notation Standard
- Output Profiles
- Quality Assurance Framework
- language and regional modules
- reference modules
- examples and conformance tests

---

## 18. Informative References and Related Work

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

