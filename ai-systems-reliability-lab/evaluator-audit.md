# Evaluator Audit

## Automated result

The frozen automated release decision for Lab 01 was **FAIL**: the candidate's automated factual-support result was **58.6%**, below the frozen **90%** threshold.

## Human audit

After the experiment, human review examined **60 / 60** outputs. Human-confirmed factual support was **96.7%** for baseline and **70.0%** for candidate. Judge/human agreement was **53.3%** for baseline and **43.3%** for candidate.

## Why release authority was not granted

The local semantic evaluator produced 24 false positives, 6 false negatives, and one unavailable result. In this bounded experiment, that was insufficient reliability for the evaluator to serve as release authority.

## What the audit did not change

The original automated FAIL remains historical evidence. The audit did not make the candidate safe: it independently confirmed materially lower candidate factual support than baseline.

## Boundary

This is a bounded conclusion about one local semantic evaluator in one frozen synthetic experiment. It is not a general finding about LLM-as-judge systems.

## Canonical evidence

Read the [canonical semantic audit report](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/01-regression-gate/results/v0.3.1-semantic-audit/semantic_audit_report.md) and [public evidence index](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/01-regression-gate/results/PUBLIC_EVIDENCE.md) for the authoritative technical record.
