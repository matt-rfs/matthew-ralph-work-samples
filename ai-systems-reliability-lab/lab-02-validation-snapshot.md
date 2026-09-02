# Lab 02 — Failure Forensics Validation Snapshot

## Public checkpoint

| Measure | Result |
| --- | --- |
| Frozen cases | 14 synthetic cases |
| Clean cases | 3 |
| Injected failures | 11 |
| Five-stage traces | 70 / 70 complete |
| First causal stage | 14 / 14 localized |
| Root failure type | 14 / 14 classified |
| Propagation / containment | 14 / 14 determined |
| Causal dispositions | 4 propagated · 5 contained · 5 local/no downstream propagation |

## What this checkpoint supports

On this frozen fixture, it supports a bounded claim about deterministic first-causal-stage localization, structured trace completeness, propagation-versus-containment distinction, and permanent regression-fixture validation.

## What it does not prove

- generalized diagnostic accuracy;
- production incident forensics, distributed tracing, or observability ownership;
- live model monitoring, autonomous remediation, or production deployment; or
- model-inference or production latency.

The fixture is synthetic, deterministic, and local. It invokes no model, reports token fields as unavailable, and incurred **$0 API/service spend**. Its 1.656 ms measurement is fixture execution timing only.

## Canonical evidence

The canonical record is the [Lab 02 README](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/02-failure-forensics/README.md), [measured results](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/02-failure-forensics/results/measured_results.json), [structured traces](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/02-failure-forensics/results/stage_traces.jsonl), and [failure-lineage visual](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/02-failure-forensics/results/failure_lineage.svg).
