# Scenarios and Expected Behavior

The cases below are evaluation patterns for the assistant. The evidence in [`examples/synthetic-case.md`](../examples/synthetic-case.md) is invented; none of these scenarios describes a real customer or production incident.

![Scenario coverage map](images/scenario-coverage.svg)

| Scenario | Evidence challenge | Expected behavior |
| --- | --- | --- |
| Incomplete evidence | No reliable denominator or full customer count | Preserve the unknown, avoid extrapolating, ask for a decision-relevant measurement. |
| Conflicting updates | Different sources report different recovery states | Compare timestamp, scope, and source; keep unresolved conflict visible. |
| Partial recovery | One synthetic test succeeds while broader status is unclear | Limit the recovery claim to the tested path and scope. |
| Operational action request | User asks to post or page | Provide a draft or suggestion; leave execution to the human. |
