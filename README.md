# ILAE-SSSOM

## Context & purpose

The International League Against Epilepsie (ILEA) has defined an [online diagnnostic manual](https://epilepsydiagnosis.org/) of epilepsies. The goal of [epilepsydiagnosis.org](https://epilepsydiagnosis.org) is to make available, in an easy to understand form, latest concepts relating to seizures and the epilepsies.

The concepts defined by ILEA, however, do not have a strict mapping to the most commonly used vocabularies in healthcare, most notably SNOMED CT. This repository aims to fill that gap by mapping the concepts defined on [epilepsydiagnosis.org](https://epilepsydiagnosis.org/) to SNOMED CT. This mapping is implemented in the [Simple Standard of Sharing Ontological Mappings (SSSOM)](https://mapping-commons.github.io/sssom/dev/) standard.

## Approach

We take the titles of the HTML pages in `kebab-case` as the concept identifiers since ILEA hasn't defined identifiers for the concepts in the diagnostic manual. Thus, `ilea:concept-title-in-kebab-case.html` resolves to the orginal URL. `ilea.sssom.tsv` contains the full mappings including the embedded metadata. The ILAE diagnostic manual URL is defined in the curie_map:

```
curie_map:
  ilea: https://epilepsydiagnosis.org/
  (...)
```

## Intended use

This mapping was created as part of a project to build an OMOP-based clinical data reposository for secondary use. Free text in the electronic medical records that refer to the ILAE diagnostic manual are linked to the OHDSI vocabularies in the ETL proces using common NLP and/or LLM-based tools.

## License

[Creative Commons Attribution 4.0] license: https://creativecommons.org/licenses/by/4.0/

