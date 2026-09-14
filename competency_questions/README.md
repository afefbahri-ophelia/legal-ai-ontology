# Competency Questions

This directory contains the Arabic competency questions used to guide LLM-based ontology enrichment in the Tunisian land-registry domain.

The questions express domain-specific information needs and are used to identify concepts and relationships that should be added or refined in the ontology.

## Contents

* `competency_questions.txt` — Arabic competency questions used for ontology enrichment.

## Role in Ontology Enrichment

The competency questions are provided to the LLM together with:

* the relevant ontology fragment;
* retrieved Arabic legal passages from the Tunisian legal corpus.

The LLM uses this information to generate candidate ontology extensions in Turtle format, including relevant classes, properties, and bilingual labels.

The competency questions are experimental resources and are not encoded as ontology axioms.

