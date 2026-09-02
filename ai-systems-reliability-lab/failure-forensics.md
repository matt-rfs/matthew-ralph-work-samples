# Lab 02 — Failure Forensics

## Where did the failure actually begin?

A bad final output can be a downstream symptom rather than the causal origin. Lab 02 is a frozen, synthetic experiment that traces a bounded five-stage AI workflow—**Normalize → Classify → Select evidence → Recommend → Generate final brief**—to the first stage that actually failed.

## Result

- **14 / 14** expected first causal stages localized on the frozen 14-case fixture.
- **14 / 14** root failure types classified.
- **14 / 14** propagation-or-containment outcomes determined.
- **70 / 70** structured stage traces complete.
- Causal outcomes: **4 propagated · 5 contained · 5 local/no downstream propagation**.

The fixture contains three clean cases and 11 injected failures. These results apply only to that frozen synthetic fixture; they are not a generalized diagnostic-accuracy claim.

## Root cause, not visible symptom

The experiment distinguishes three outcomes. A **propagated** failure is an earlier invalid state actually consumed by a later stage and observed in its output. A **contained** failure stops later stages fail-closed; that blocked sequence is not propagation. A **local** failure has no invalid downstream output.

For example, a classification defect can be the root cause even when evidence selection, recommendation, and the final brief visibly show its symptoms. The correct response is to repair the narrow failing contract, not assume final generation was the cause.

## Matthew’s role

Matthew designed the forensic experiment around causal failure localization, required inspectable intermediate state and real stage-to-stage consumption, rejected a mechanically plausible but causally weak first publication candidate, and directed the repaired experiment and validation against stricter evidence requirements.

## What required human judgment

- **Causality rather than sequence:** stage order alone did not prove propagation; a later invalid output had to consume the earlier invalid state.
- **Propagation rather than containment:** fail-closed blocked stages were recorded as contained, not presented as downstream propagation.
- **Publication authority:** the initial evidence candidate was rejected because its mechanically assigned propagation did not demonstrate causal consumption.
- **Regression preservation:** `evidence-01` fails before its bounded correction at `select_evidence` with `EVIDENCE_FAILURE`, then passes after the expected evidence is restored. The pre-fix/post-fix loop remains a permanent regression test.

## Boundary

This is a frozen, synthetic, deterministic local fixture—not production incident forensics, an observability platform, distributed tracing, live model monitoring, autonomous remediation, or a claim about all AI workflows. No model is invoked; token fields are unavailable; API/service spend is **$0**. The measured **1.656 ms** is fixture execution timing, not a model-inference or production-latency metric.

## Canonical technical evidence

This page curates the public interpretation. The canonical evidence is in the [AI Systems Reliability Lab repository](https://github.com/matt-rfs/ai-systems-reliability-lab):

- [Lab 02 README](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/02-failure-forensics/README.md)
- [Measured results](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/02-failure-forensics/results/measured_results.json)
- [Failure-lineage visual](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/02-failure-forensics/results/failure_lineage.svg)
- [Frozen expected-failure map](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/02-failure-forensics/data/expected_failures.jsonl)
