# LLM Validation

This directory contains the resources used for semantic validation of ontology axioms using multiple Large Language Models (LLMs).

## Validation Setup

A set of 96 interpretable TBox axioms extracted from the cleaned ontology was independently evaluated by four LLMs:

* Qwen3-4B
* Llama 3.2-3B
* Phi-4-mini
* Gemma 3-4B

Each model evaluated the semantic plausibility of the same ontology axioms using a common validation protocol.

## Validation Configurations

Two prompt configurations are documented in the `prompts/` directory:

* Axiom Only — the formal ontology axiom is provided to the model.
* Axiom + Natural-Language Question — the formal axiom is provided together with its natural-language interpretation.

The validation task uses three predefined responses:

* YES
* NO
* UNCERTAIN

Responses outside these categories are retained separately and are not converted into semantic judgments.

## Contents

* `semantic_axioms_four_models.csv` — validation results produced by the four LLMs.

The individual model judgments are retained to support cross-LLM agreement analysis and the identification of semantic hotspots.

