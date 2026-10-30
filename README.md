# Incident Command Assistant

**Evidence-first incident analysis, from first signal to a human-reviewed update.**

![End-to-end incident review process](docs/images/end-to-end-review.svg)

This portfolio project packages a reusable instruction workflow for incident commanders. It helps turn incident notes, service updates, and metrics into a clear view of customer impact, uncertainty, response progress, and next decisions.

It is designed to make the incident easier to understand—not to take command. The assistant analyzes and drafts; a human verifies and decides what to communicate or do.

## The objective

During an incident, evidence is fragmented across updates, dashboards, alerts, and responder notes. This assistant provides a consistent way to:

- Explain the broken customer journey in everyday language.
- Separate facts, attributed reports, hypotheses, conflicts, and unknowns.
- Bound customer impact without inventing totals or percentages.
- Assess urgency and impact using the organization’s supplied policy.
- Track mitigation, validation, recovery, and follow-up actions distinctly.
- Prepare concise briefings for human review.

## Understand the service flow

![Fictional appointment-service flow with an example failure boundary](docs/images/service-flow.svg)

The pictured flow is fictional and illustrates how to describe a user journey. For any real incident, build the flow from supplied evidence; do not assume that the example components or fault location apply.

## Scenarios covered

![Scenario coverage and expected assistant behavior](docs/images/scenario-coverage.svg)

The scenario map shows the core reasoning challenges: incomplete evidence, conflicting updates, partial recovery, and requests to take operational actions. More detail is in [`docs/scenarios.md`](docs/scenarios.md).

## End-to-end process

1. **Scope** the incident, service, region, and time window.
2. **Read** supplied or authorized evidence and record its source window.
3. **Trace** the timeline, customer journey, and service flow.
4. **Assess** customer impact and urgency/impact using current supplied guidance.
5. **Review** cause, mitigation, validation, recovery, and open actions.
6. **Draft** the requested update and identify the highest-value gaps.
7. **Human review:** verify the evidence and decide what to share or execute.

The assistant does not post updates, page responders, edit records, deploy changes, or declare recovery on its own.

## Repository guide

- [`skill/SKILL.md`](skill/SKILL.md) — the reusable assistant instruction.
- [`skill/references/review-playbook.md`](skill/references/review-playbook.md) — evidence-led full review workflow.
- [`skill/references/output-contracts.md`](skill/references/output-contracts.md) — concise review and update structures.
- [`skill/references/safety-boundaries.md`](skill/references/safety-boundaries.md) — privacy, credential, and operational safeguards.
- [`docs/architecture.md`](docs/architecture.md) — components, request flow, and trust boundary.
- [`docs/scenarios.md`](docs/scenarios.md) — scenario goals and expected behavior.
- [`docs/validation-plan.md`](docs/validation-plan.md) — proposed synthetic evaluation plan.
- [`examples/synthetic-case.md`](examples/synthetic-case.md) and [`examples/sample-review.md`](examples/sample-review.md) — fictional input and illustrative output.

## Try it

Provide a compatible assistant with the files under `skill/` and a fictional or properly authorized evidence set. For example:

> Review this incident evidence. Summarize the customer impact, what is confirmed about recovery, the next open actions, and the most important uncertainty. Do not perform any incident operations.

The sample review demonstrates the intended evidence discipline. Adapt the package to your organization’s approved communication templates and priority policy before operational use.

## Safety and privacy

This public edition uses synthetic evidence and provider-neutral guidance. Never publish secrets, internal-only URLs, customer identifiers, confidential incident records, or proprietary policies. The instruction pack is not a permission boundary; the host platform must enforce access and tool permissions.

See [`skill/references/safety-boundaries.md`](skill/references/safety-boundaries.md) and [`docs/validation-plan.md`](docs/validation-plan.md).

## Project status

Provider-neutral portfolio material with fictional examples. No license is included yet; choose one before inviting reuse. No production integrations or operational actions are included.
