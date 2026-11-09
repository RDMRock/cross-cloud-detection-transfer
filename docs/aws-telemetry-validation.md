# Earlier AWS telemetry and query validation

On October 6, 2026, the project recorded three controlled Stratus Red Team exercises in a dedicated AWS lab. CloudTrail delivered events to CloudWatch Logs. The original saved queries were executed without changing their filters to fit the results.

| Exercise | Queried operation | Recorded result |
| --- | --- | --- |
| Individual S3 object deletion | `DeleteObject` | 51 matching rows for activity in a disposable bucket. |
| EBS snapshot sharing | `ModifySnapshotAttribute` | One matching row correlated with the share operation. |
| SSM command targeting three instances | `SendCommand` | One matching command event and three successful invocations. |

The record correlated returned events with the exercise, target, and time. EBS and SSM also used event identifiers. The SSM result came from a later live run after an earlier blocked attempt; the benign replay from the earlier attempt is separate evidence.

The run records describe removal of the exercise resources and temporary logging infrastructure. Account numbers, resource names, event identifiers, and raw cloud captures are not published here.

## Limits

These results establish telemetry delivery and query matching for the selected examples. The SSM query also matched a real benign command. S3 and EBS did not have benign controls in that run. Saved queries do not provide continuous alert delivery by themselves.

The row counts are not a detection rate, an attack-specificity measurement, or evidence of successful cross-cloud transfer. This historical AWS work is separate from the reviewed translation experiment.

Source: the project's dated three-rule validation report and its preserved run records. The public [Stratus Red Team project](https://github.com/DataDog/stratus-red-team) identifies the exercise framework used.
