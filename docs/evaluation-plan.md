# Evaluation plan and open decisions

The main question is whether a translated rule preserves the required detection behavior, including the cases it should not match. Query text or valid JSON alone cannot answer that question.

## Current interface versus proposed protocol

The existing score interface contains Compilation, Semantics, Scope, Access, and Attribution. A later proposed study protocol separates Execution, Meaning, Required matches, Extra matches, Data and permissions, Evidence, Abstention, and Repeatability. The proposed list has not been adopted or implemented as the final frozen protocol.

The public overview preserves that distinction rather than treating a proposal as an implemented metric.

## Checks being prepared

- Run the query in the native target engine and distinguish query acceptance from runtime completion.
- Compare independently reviewed semantic claims, including omissions, additions, and unresolved meaning.
- Test complete scenarios with expected groups, unexpected groups, thresholds, time boundaries, missing fields, duplicates, and relevant history.
- Check required telemetry and permissions against reviewed target requirements.
- Compare output evidence for returned expected groups without hiding missing detections.
- Evaluate justified abstention separately from unnecessary refusal and unsupported query claims.
- Compare fresh repeated translations under fixed conditions without counting cache reuse as another trial.

Supporting checks assess the evaluator itself: whether cases distinguish the required behaviors, whether independent reviewers agree before reconciliation, and whether injected semantic faults are detected while equivalent rewrites remain acceptable.

## Remaining work

Reference mappings, hidden cases, reviewers, target-engine access, denominators, failure handling, cost accounting, and analysis choices need to be fixed before the scored pilot. The first planned scored transfer is an OCI policy-change rule to AWS. The final study follows that pilot rather than treating framework test coverage as detection performance.

The ten current source cases were visible during development. Any claim of generalization to unseen rules needs a genuinely separate evaluation set.
