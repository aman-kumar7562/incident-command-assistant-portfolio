# Review Playbook

Use this sequence for a full incident review. Skip sections that do not help answer the user’s request, and mark unavailable evidence plainly.

## 1. Establish scope and source coverage

Record the incident identifier, affected service or feature, region/environment, requested time window, and current review time. List the sources that were actually reviewed and their latest timestamp. Call out partial history, pagination, stale snapshots, or failed access when material.

## 2. Build a compact evidence ledger

For each important claim, capture:

| Claim | Evidence and time | Evidence type | Confidence or limitation |
| --- | --- | --- | --- |
| What users experienced | Source and timestamp | Observed / reported / inferred | Scope and uncertainty |

Do not promote a hypothesis to a fact. Resolve conflicts by comparing source authority, scope, and time. If the conflict changes the decision, leave it visible and state what would resolve it.

## 3. Describe the customer journey

Explain the relevant user or operator action from start to finish. Identify where it failed, what symptom appeared, and which component or dependency is implicated by evidence. A small arrow flow is useful when it makes the failure boundary clearer.

## 4. Assess impact and priority

Summarize affected user groups, regions, environments, features, and known customer cases. Keep measured windows and denominators explicit. Separate observed sample failure rates from total population impact.

Assess urgency and impact using the current policy supplied for this organization. Explain the evidence behind each dimension, note unsupported assumptions, and recommend a priority only when its mapping is available. Otherwise state that priority validation is pending policy.

## 5. Review response and recovery

Build a deduplicated timeline of detection, investigation, mitigation, validation, and recovery. For each action, distinguish:

- Completed, with evidence of completion.
- In progress, with the latest update.
- Planned or proposed, not yet executed.
- Suggested follow-up, not yet accepted.

Recovery is established only for the paths and scope supported by successful validation. Keep partial recovery and continuing symptoms visible.

## 6. Identify decision-relevant gaps

Ask focused questions that could change impact, priority, mitigation, or closure decisions. Prefer a few specific questions over a generic checklist. Explain why an answer matters.

## 7. Produce the requested output

Lead with the current assessment, then provide only the supporting detail needed for the request. Use plain language. Link or identify sources when available. Apply the human-review disclaimer in the output contract.
