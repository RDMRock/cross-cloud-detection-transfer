# Experiment design

The current framework asks whether process assistance helps a small local model preserve detection meaning, and whether those effects also help a stronger model. The stronger-model comparison remains planned.

## Processes under comparison

| Process group | Current modes |
| --- | --- |
| Semantic intermediate representation (IR) | Off; IR only; source plus IR. |
| Documentation retrieval | Off; keyword; embedding; hybrid; hybrid plus model review. |
| Target logs | Off; development examples. |
| Candidate selection | Off; selection without lessons; selection with reviewed lessons. |
| Feedback | Off; critique; independently verified counterexamples. |

The mode product is `3 × 5 × 2 × 3 × 3 = 270` configurations. Stage ordering adds another dimension. Applying the framework's ordering constraints produces 884 valid ordered conditions per rule, model, and repeat. Those conditions share rules and caches and must not be presented as 884 independent research observations.

Preparation precedes generation. Selection and feedback follow generation, with either order allowed when both are enabled. Feedback permits one revision. In IR-only mode, documentation retrieval must follow IR extraction so the original source is not silently reintroduced.

## Preserve meaning before comparing outputs

The semantic contract covers action, entities/scope, predicates, Boolean logic, quantifiers, grouping, aggregation, thresholds, time windows, correlation/sequence, history, exclusions, missing-data behavior, and result evidence. Unknown or unsupported behavior remains explicit.

Schema acceptance establishes structure. It does not establish that the source meaning was extracted correctly, the target telemetry exists, or the target engine will execute the query correctly.

## Experiment controls

The framework records versions and artifact identities, separates development inputs from hidden evaluation material, preserves cached outcomes, and tracks attempted calls. A resumed cached request is not a fresh replicate. Audit findings and hidden answers must not enter generation or revision prompts.

Current translator preparation uses Qwen3 1.7B through local Ollama with thinking enabled. The selected sampling settings are recorded privately. Context/output limits, repeat counts, candidate counts, embedding model, and final protocol must be frozen as study decisions before results are compared. Starter defaults and the consumed smoke-test budget are not approvals for the full study.

This document describes the current framework and planned research. It does not change the private study's settings or approve additional model or cloud execution.
