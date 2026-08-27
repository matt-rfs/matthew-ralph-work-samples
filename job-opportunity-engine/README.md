# Job Opportunity Engine

Job Opportunity Engine is a private, local-first governed career-operations system spanning job collection, deterministic evaluation, evidence-bound preparation, private artifact custody, and human review.

Career operations is the domain. The reusable system capabilities demonstrated here are evidence provenance, deterministic decisioning, identity isolation, governed preparation, lifecycle/state management, traceable artifacts, and human-controlled AI workflows.

## Matthew’s role

- Product and system architecture; operating-model definition
- Requirements, decision boundaries, lifecycle/state, and evidence-model design
- Governance, validation criteria, and implementation direction
- Human-review controls and bounded AI coding-agent direction

## System model

1. Collect, normalize, verify, and deduplicate an opportunity.
2. Extract requirements and evaluate fit deterministically.
3. Match governed evidence and approved capability assessments.
4. Rank the opportunity and gate preparation.
5. Freeze the verified preparation basis into an authoritative packet.
6. Validate evidence-bound claims and keep preparation artifacts private.
7. Present preparation state for candidate-scoped human review.

Deterministic software remains authority for identity, evidence, state, validation, and consequential decisions. Provider-neutral generation contracts and synthetic test behavior do not make generated output authoritative evidence.

## Public evidence path

- [Architecture diagram](architecture.svg)
- [Fictional evaluation walkthrough](synthetic-walkthrough.md)
- [Fictional preparation lifecycle](preparation-lifecycle.md)
- [Design decisions](design-decisions.md)
- [Validation snapshot](validation-snapshot.md)
- [Public portfolio case study](https://matt-rfs.github.io/matthew-ralph-portfolio/work/job-opportunity-engine/)

## What the public checkpoint supports

At the latest clean public checkpoint, committed private Python and SQLite authority was validated by **180 passing automated tests**. The checkpoint supports governed collection and evaluation, canonical evidence and capability matching, preparation orchestration, frozen packets, deterministic claim validation, private artifact custody, lifecycle controls, and candidate-scoped review behavior.

## Current boundary

This is not a production SaaS, autonomous career agent, live model-generation system, browser-automation tool, or ATS-submission system. Production document QA, cover-letter and application-question systems, live provider integrations, and final external submission remain outside the checkpoint. This repository intentionally excludes private runtime code, data, records, artifacts, packets, and configuration.

## Governance principles

- Keep private candidate evidence and preparation artifacts profile-isolated.
- Generated output is not authoritative evidence: AI may propose; evidence proves; humans approve.
- Make material evaluation rules inspectable and deterministic.
- Bind capability matching to approved assessments rather than unsupported inference.
- Freeze a preparation basis; if relevant underlying state changes, surface divergence rather than silently drifting.
- Require human control for consequential external actions.
