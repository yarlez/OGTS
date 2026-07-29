# Open Genealogy Transcription Standard (OGTS) Charter

**Version:** 0.1 Draft  
**Status:** Draft  
**Document Type:** Normative  
**Last Updated:** 29 Jul 2026

---

## 1. Purpose

The Open Genealogy Transcription Standard (OGTS) defines editorial principles, terminology, and minimum requirements for the faithful transcription, translation, normalization, and structured extraction of historical genealogical documents.

OGTS is intended to promote consistent, transparent, and reproducible practices for both human researchers and software implementations.

---

## 2. Scope

OGTS applies to historical documents used in genealogical research, including but not limited to:

- Church registers
- Civil registration records
- Family books
- Census records
- Probate records
- Land records
- Military records
- Immigration records
- Other historical records of genealogical value

The standard is language-independent.

Language- and region-specific practices are defined through separate modules.

---

## 3. Principles

OGTS is founded on the following principles.

### 3.1 Preserve the Source

The source document is the primary evidence.

Implementations shall preserve the content of the source as faithfully as possible.

---

### 3.2 Separate Observation from Interpretation

Observed information shall be distinguished from editorial interpretation or genealogical inference.

---

### 3.3 Preserve Uncertainty

Uncertainty shall be made explicit.

Missing, illegible, or ambiguous content shall never be silently resolved.

---

### 3.4 Transparency

Editorial intervention shall be visible.

Readers shall be able to distinguish:

- original text
- editorial expansion
- normalization
- translation
- interpretation
- inference

---

### 3.5 Reproducibility

Different conforming implementations should produce substantially equivalent results when given the same document and the same output profile.

---

## 4. Conformance

An implementation conforms to OGTS when it satisfies all mandatory requirements defined by the Core Standard together with any required language or reference modules.

Conformance does not require the use of any specific software platform, artificial intelligence system, or OCR engine.

---

## 5. Modularity

OGTS consists of a Core Standard together with optional language, regional, and reference modules.

Examples include:

- German Module
- Latin Module
- Hebrew Module
- Occupation Reference Module
- Date Reference Module
- Abbreviation Module

---

## 6. Governance

OGTS is maintained as an open standard.

Changes are proposed, reviewed, and incorporated through public revision of the specification.

---

## 7. Non-Goals

OGTS does not prescribe:

- a particular AI model
- a specific OCR engine
- a genealogy database
- a software implementation
- a user interface

OGTS specifies editorial behavior, not software architecture.

---

## 8. Vision

OGTS seeks to establish an open, implementation-independent standard for AI-assisted genealogical transcription that promotes scholarly integrity, interoperability, and long-term preservation of historical evidence.
