# LLM Validation

This directory contains the resources used for semantic validation of ontology axioms using multiple Large Language Models (LLMs).

## Validation Dataset

The file `semantic_axioms_four_models.csv` contains the semantic validation results for the selected ontology axioms.

Each record contains:

* `axiom_id` — identifier of the validated axiom.
* `type` — type of ontology axiom, such as `subClassOf`, `domain`, or `range`.
* `subject` — subject of the ontology axiom.
* `subject_label_en` — English label of the subject.
* `subject_label_ar` — Arabic label of the subject.
* `relation` — semantic relation expressed by the axiom.
* `object` — object of the ontology axiom.
* `object_label_en` — English label of the object.
* `object_label_ar` — Arabic label of the object.
* `question` — natural-language interpretation of the axiom.
* `question_en` — English version of the question.
* `question_ar` — Arabic version of the question.
* `qwen3_4b_response` — semantic judgment produced by Qwen3-4B.
* `Llama3.2-3B` — semantic judgment produced by Llama 3.2-3B.
* `Phi-4-mini` — semantic judgment produced by Phi-4-mini.
* `Gemma 3-4B` — semantic judgment produced by Gemma 3-4B.

## Validation Task

Each LLM evaluates whether the semantic relationship expressed by an ontology axiom is conceptually plausible.

The predefined semantic judgments are:

* `YES` — the relationship is considered semantically plausible.
* `NO` — the relationship is considered semantically implausible.
* `UNCERTAIN` — the available information is insufficient for a reliable judgment.

The models independently evaluate the same ontology axioms.

## Example

For the axiom:

```text
AdministrativeDocument
rdfs:subClassOf
OfficialDocument
```

the corresponding natural-language question is:

```text
Is Administrative Document a type of Official Document?
```

The four model responses are retained in separate columns in the CSV.

## Purpose

The collected judgments are used to analyze:

* agreement and disagreement between independent LLM validators;
* semantic stability of ontology axioms;
* consensus across models;
* axioms exhibiting substantial disagreement, which are considered candidates for semantic hotspot analysis.

The validation results are retained at the individual model level to preserve the original independent judgments.
