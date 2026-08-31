# Validation Snapshot

## Public checkpoint

**Lab 01 — Model Regression Gate**

| Measure | Result |
| --- | --- |
| Frozen cases | 30 synthetic cases |
| Deterministic validation | 30 / 30 baseline · 30 / 30 candidate |
| Deterministic regressions | 0 |
| Hard-gate violations | 0 |
| Automated release | FAIL |
| Frozen semantic threshold | 90% |
| Candidate automated factual support | 58.6% |
| Human audit | 60 / 60 outputs |
| Human-confirmed factual support | 96.7% baseline · 70.0% candidate |
| Judge/human agreement | 53.3% baseline · 43.3% candidate |

## What this checkpoint supports

It supports a bounded claim about frozen evaluation discipline, deterministic validation, historical release gating, evaluator validation, and human review. The local semantic evaluator was not reliable enough to serve as release authority in this experiment; human review independently confirmed the candidate's degradation.

## What it does not prove

- a production benchmark or production AI reliability platform;
- a general claim about LLM-as-judge systems;
- autonomous production release authority; or
- customer deployment or production traffic.

The experiment was synthetic and local, with $0 API/service spend.

## Canonical evidence

The canonical record is the [Lab 01 overview](https://github.com/matt-rfs/ai-systems-reliability-lab/tree/main/labs/01-regression-gate), [public evidence index](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/01-regression-gate/results/PUBLIC_EVIDENCE.md), and [semantic audit report](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/01-regression-gate/results/v0.3.1-semantic-audit/semantic_audit_report.md).
