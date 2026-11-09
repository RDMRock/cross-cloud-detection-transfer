# Verification and limits

Snapshot: November 8, 2026, America/Vancouver. The public overview was checked against the standalone private project's current-state handoff, migration receipt, test log, synthetic smoke-test receipt, rule provenance notes, and earlier AWS validation report.

The migration receipt records 188 passing tests and 884 fake-model ordered conditions, all with the status `needs_evaluation`. A completed-batch resume made no additional calls. Its test-log SHA-256 matched the saved log during this portfolio review. The [public JSON summary](../evidence/verification-summary.json) preserves selected fields without personal paths, model outputs, or private evaluation material.

During portfolio preparation, the current source was copied into an isolated scratch directory and its offline suite was rerun: **188 tests passed in 21.206 seconds**. No model or cloud calls were made. The full 884-condition grid was not rerun for this publication; its result comes from the verified migration record.

The single real local inference call returned the expected JSON for four invented records in about 24.7 seconds. It used 143 prompt tokens and 645 generated tokens according to the runtime counters. It was not a cloud translation or a measured study comparison.

The public summary describes internal evidence. A hash identifies the recorded log but does not make private evidence independently inspectable or prove that an evaluator is correct. The working implementation remains private, as requested for the collaborative research repository.

## Source and contribution boundaries

Ten study cases cover seven source clouds. Seven are saved publisher definitions, two are published examples, and one is a reconstructed condition. Those categories are retained in the private provenance record. No claim is made that every source is a complete executable rule or that target mappings have been validated.

The project is collaborative. Rory's portfolio emphasizes framework integration, experimental design, evidence handling, and validation preparation. Teammate IR work is subject to review and integration. AI assistance was used in research, implementation, review, and documentation. No sole-authorship or production-deployment claim is made.

Public research presentation follows the principle illustrated by [OTRF Security Datasets](https://github.com/OTRF/Security-Datasets) and [Splunk Security Content](https://github.com/splunk/security_content): explain the inputs and connect an analytic claim to validation evidence. These are reference projects, not dependencies or claimed affiliations.
