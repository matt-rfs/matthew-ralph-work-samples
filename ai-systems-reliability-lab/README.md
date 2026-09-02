# AI Systems Reliability Lab

Small, bounded experiments demonstrating AI evaluation, failure analysis, evidence integrity, and human authority.

## Lab 01 — Model Regression Gate

A frozen AI reliability experiment asking whether a proposed configuration made a bounded workflow worse—and whether it should be released.

The experiment used 30 synthetic cases and froze the evaluation rules before final execution. Both baseline and candidate passed deterministic validation, but the historical automated release decision was **FAIL** because the candidate's factual-support score of **58.6%** remained below the frozen **90%** threshold.

A later human audit reviewed all **60 / 60** outputs. It confirmed that the candidate had materially lower factual support than baseline while also showing that the local semantic evaluator was not reliable enough to serve as release authority in this bounded experiment. The original automated FAIL remains preserved as historical evidence.

**Evaluate:** Should this configuration be released?

## Lab 02 — Failure Forensics

A frozen, synthetic five-stage workflow asking where a bad outcome actually began—not merely where it became visible.

Across **14 frozen cases** (three clean and 11 injected failures), the deterministic fixture recorded **70 / 70 complete stage traces** and localized the expected first causal stage, root failure type, and propagation-or-containment outcome in **14 / 14** cases. Its outcomes are deliberately bounded: **4 propagated**, **5 contained**, and **5 local/no downstream propagation**.

**Diagnose:** Where did the failure begin?

Together, the two Labs connect **evaluate → diagnose**: first ask whether a candidate configuration earns release; then, when an outcome fails, require evidence showing where the failure actually started.

## Matthew’s role

Designed the evaluation approach, frozen release criteria, causal experiment structure, decision boundaries, validation strategy, evidence-integrity rules, and human-review controls; directed bounded implementation and testing against those requirements. For Lab 02, Matthew required inspectable intermediate state and real stage-to-stage consumption, rejected a mechanically plausible but causally weak first publication candidate, and directed the repaired experiment and validation against stricter evidence requirements.

## What this demonstrates

- **AI evaluation discipline:** release criteria and evaluator behavior were defined and tested rather than improvised after results appeared.
- **Technical-program judgment:** deterministic validation was separated from probabilistic semantic judgment.
- **AI governance:** automated evaluator output was not treated as unquestionable authority.
- **Human oversight:** questionable machine judgment triggered structured human review.
- **Evidence integrity:** contaminated and failed states were preserved rather than rewritten into cleaner-looking evidence.
- **Failure analysis:** downstream symptoms were distinguished from the stage that causally failed.

## Curated evidence path

- [Model Regression Gate](model-regression-gate.md)
- [Evaluator audit](evaluator-audit.md)
- [Validation snapshot](validation-snapshot.md)
- [Failure Forensics](failure-forensics.md)
- [Lab 02 validation snapshot](lab-02-validation-snapshot.md)
- [Public portfolio case study](https://matt-rfs.github.io/matthew-ralph-portfolio/work/ai-systems-reliability-lab/)

## Canonical technical evidence

This directory is a curated interpretation layer, not a second technical source of truth. The canonical public evidence remains in [matt-rfs/ai-systems-reliability-lab](https://github.com/matt-rfs/ai-systems-reliability-lab), including the [Lab 01 overview](https://github.com/matt-rfs/ai-systems-reliability-lab/tree/main/labs/01-regression-gate), [public evidence index](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/01-regression-gate/results/PUBLIC_EVIDENCE.md), and [semantic audit report](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/01-regression-gate/results/v0.3.1-semantic-audit/semantic_audit_report.md). Lab 02's canonical record includes its [Failure Forensics README](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/02-failure-forensics/README.md), [measured results](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/02-failure-forensics/results/measured_results.json), and [failure-lineage visual](https://github.com/matt-rfs/ai-systems-reliability-lab/blob/main/labs/02-failure-forensics/results/failure_lineage.svg).

## Boundary

These are synthetic, local experiments—not production benchmarks, production AI reliability platforms, production incident forensics, or autonomous production systems. Lab 02 invokes no model, reports token fields as unavailable, and incurred $0 API/service spend. Its fixture execution timing is not a claim about model or production latency.
