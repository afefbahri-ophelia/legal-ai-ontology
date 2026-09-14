# Competency-Driven Enrichment and Validation of Legal Ontologies Using Cross-LLM Consensus

This repository contains the research resources for our work on LLM-assisted legal ontology engineering and validation in the Tunisian land-registry domain.

## Overview

The project investigates how Large Language Models (LLMs) can support the enrichment and semantic validation of legal ontologies while reducing reliance on manually constructed gold-standard ontologies.

The methodology follows a staged pipeline:

**Core Ontology → RAG-based Enrichment → Cleaning → Formal Validation → Cross-LLM Validation → Consensus Analysis → Semantic Hotspots**

## Ontology Enrichment

An expert-defined core ontology is progressively extended using competency questions, relevant ontology fragments, and passages retrieved from a Tunisian legal and administrative corpus.

Claude 3 Haiku is used for ontology enrichment through retrieval-augmented generation.

## Semantic Validation

The resulting ontology is cleaned and a set of 96 interpretable TBox axioms is extracted for semantic validation.

Four independent LLMs evaluate the same axioms using a common validation protocol:

* Qwen3-4B
* Llama 3.2-3B
* Phi-4-mini
* Gemma 3-4B

Each model assigns one of three semantic judgments:

* YES
* NO
* UNCERTAIN

## Cross-LLM Consensus and Semantic Hotspots

The individual model judgments are aggregated to characterize semantic stability across validators.

A semantic hotspot is operationally defined as an axiom receiving an exact **2-YES / 2-NO** split among the four validators. These cases are treated as indicators of semantic instability and are candidates for further expert inspection.

## Resources

The repository contains selected ontology, validation, prompt, and experimental resources associated with the study.

## Domain

The ontology focuses on Tunisian land-registry and property-registration procedures, including daily legal registry, land title registration, and ownership certification.

## Citation

If you use these resources, please cite the associated paper:

> *Competency-Driven Enrichment and Validation of Legal Ontologies Using Cross-LLM Consensus.*

## Author

**Afef Bahri**

Research on Artificial Intelligence and Law, Legal Ontology Engineering, and Large Language Models.
