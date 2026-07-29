# Open Genealogy Transcription Standard (OGTS)

The **Open Genealogy Transcription Standard (OGTS)** is an open, vendor-neutral specification for AI-assisted transcription, translation, and structured extraction of historical genealogical documents.

OGTS defines editorial principles, an evidence model, notation standards, output profiles, and conformance requirements that promote faithful transcription, transparent editorial practice, and reproducible results across AI systems and other software implementations.

## Goals

- Preserve the historical source as the primary evidence.
- Separate observation from interpretation.
- Promote transparent editorial practices.
- Support reproducible AI-assisted workflows.
- Provide a common standard that can be implemented by multiple AI platforms and genealogy tools.

## Project Status

**Current Status:** Draft (Version 0.1)

The initial governance foundation has been established through the [Project Charter](docs/charter.md), contribution guidance, and license. Governance remains intentionally minimal at this stage: formal maintainer roles, decision-making procedures, and approval workflows have not yet been defined. The Project Charter is currently the only normative technical specification.

The next major milestone is drafting the Core Standard at `docs/core-standard.md`.

## Repository Structure

Current repository contents:

```
CONTRIBUTING.md       Contribution and standards-development guidance
LICENSE.md            CC BY 4.0 license
README.md             Project overview and roadmap
docs/charter.md       Draft normative project charter
```

As the project develops, additional material is expected to be organized approximately as follows:

```
docs/               Core specification documents
modules/            Language and regional modules
references/         Reference modules and supporting material
examples/           Sample documents and expected outputs
tests/              Conformance tests
implementations/    Reference implementations of the standard
```

## Roadmap

The governance foundation for Version 0.1 includes:

- Project Charter
- Contribution guidelines
- CC BY 4.0 licensing

The next stages of Version 0.1 are expected to include:

- Core Standard
- Evidence Model
- Notation Standard
- Output Profiles
- Quality Assurance Framework
- German Language Module

Terminology will initially be defined within the Core Standard and may be extracted into a separate document later if its scope warrants independent treatment.

## Contributing

Contributions are welcome.

See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines and standards-development principles.

## License

The OGTS specification is licensed under the [Creative Commons Attribution 4.0 International License](LICENSE.md).
