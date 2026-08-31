# Lab 01 — Model Regression Gate

A frozen AI reliability experiment asking whether a proposed configuration made a bounded business workflow worse and whether it should be released.

## Experiment

- **Evaluation set:** 30 fixed synthetic cases
- **Comparison:** frozen baseline versus candidate configurations
- **Method:** evaluation rules and release criteria were frozen before final execution

## Deterministic result

| Check | Baseline | Candidate |
| --- | ---: | ---: |
| Deterministic validation | 30 / 30 | 30 / 30 |
| Deterministic regressions | 0 | 0 |
| Deterministic fixes | 0 | 0 |
| Hard-gate violations | 0 | 0 |

## Historical automated release decision

**FAIL**

The candidate's automated factual-support result was **58.6%**, below the frozen **90%** semantic threshold. Baseline automated factual support was **50.0%**. One candidate semantic judgment was unavailable.

The automated FAIL is preserved as the historical system decision. Later review adds interpretation; it does not rewrite the record.

## Post-experiment human audit

All **60 / 60** outputs were reviewed.

| Measure | Baseline | Candidate |
| --- | ---: | ---: |
| Human-confirmed factual support | 96.7% | 70.0% |
| Judge/human agreement | 53.3% | 43.3% |

The audit also recorded 24 false positives, 6 false negatives, and one unavailable judge result.

## Key finding

The local semantic evaluator was not reliable enough to deserve release authority in this bounded experiment. That finding did not make the candidate safe: human review independently confirmed that the candidate configuration performed materially worse than baseline on factual support.

## What required human judgment

- **Evaluator authority:** a score did not automatically earn decision authority.
- **Evidence integrity:** contaminated execution was rejected rather than normalized into the final result.
- **Interpretation:** evaluator unreliability did not erase the candidate's independently confirmed degradation.
- **Historical record:** the automated FAIL remained part of the evidence trail after the later audit.

## Canonical evidence

This curated summary routes to—not replaces—the [canonical Lab 01 evidence](https://github.com/matt-rfs/ai-systems-reliability-lab/tree/main/labs/01-regression-gate), [public evidence index](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/01-regression-gate/results/PUBLIC_EVIDENCE.md), and [semantic audit report](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/01-regression-gate/results/v0.3.1-semantic-audit/semantic_audit_report.md).

## Boundary

Synthetic and local. This is not a production benchmark, certification, production deployment, customer system, or general claim about all LLM-as-judge systems.
