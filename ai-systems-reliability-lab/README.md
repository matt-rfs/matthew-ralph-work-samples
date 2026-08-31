# AI Systems Reliability Lab

Small, bounded experiments demonstrating AI evaluation, release gating, failure analysis, and human authority.

## Lab 01 — Model Regression Gate

A frozen AI reliability experiment asking whether a proposed configuration made a bounded workflow worse—and whether it should be released.

The experiment used 30 synthetic cases and froze the evaluation rules before final execution. Both baseline and candidate passed deterministic validation, but the historical automated release decision was **FAIL** because the candidate's factual-support score of **58.6%** remained below the frozen **90%** threshold.

A later human audit reviewed all **60 / 60** outputs. It confirmed that the candidate had materially lower factual support than baseline while also showing that the local semantic evaluator was not reliable enough to serve as release authority in this bounded experiment. The original automated FAIL remains preserved as historical evidence.

## Matthew’s role

Designed the evaluation approach, frozen release criteria, decision boundaries, validation strategy, evidence-integrity rules, and human-review controls; directed bounded implementation and testing against those requirements.

## What this demonstrates

- **AI evaluation discipline:** release criteria and evaluator behavior were defined and tested rather than improvised after results appeared.
- **Technical-program judgment:** deterministic validation was separated from probabilistic semantic judgment.
- **AI governance:** automated evaluator output was not treated as unquestionable authority.
- **Human oversight:** questionable machine judgment triggered structured human review.
- **Evidence integrity:** contaminated and failed states were preserved rather than rewritten into cleaner-looking evidence.

## Curated evidence path

- [Model Regression Gate](model-regression-gate.md)
- [Evaluator audit](evaluator-audit.md)
- [Validation snapshot](validation-snapshot.md)
- [Public portfolio case study](https://matt-rfs.github.io/matthew-ralph-portfolio/work/ai-systems-reliability-lab/)

## Canonical technical evidence

This directory is a curated interpretation layer, not a second technical source of truth. The canonical public evidence remains in [matt-rfs/ai-systems-reliability-lab](https://github.com/matt-rfs/ai-systems-reliability-lab), including the [Lab 01 overview](https://github.com/matt-rfs/ai-systems-reliability-lab/tree/main/labs/01-regression-gate), [public evidence index](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/01-regression-gate/results/PUBLIC_EVIDENCE.md), and [semantic audit report](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/01-regression-gate/results/v0.3.1-semantic-audit/semantic_audit_report.md).

## Boundary

This is a synthetic, local experiment—not a production benchmark, production AI reliability platform, general claim about LLM-as-judge systems, or autonomous production release system. It reports $0 API/service spend, not a broader claim about compute cost.
