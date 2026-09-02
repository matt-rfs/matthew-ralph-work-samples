# Bounded real-model claim-identification evidence

## The decision problem

AI can identify potentially useful claims in messy source material. A plausible model response, however, should not automatically become trusted system knowledge. PIR was designed to keep that distinction visible and enforceable.

The V008 validation tested one narrow question: can a hosted model materially reduce manual claim-identification work while PIR keeps the source grounding, deterministic validation, cost, privacy, and final decision boundaries intact?

## The governed corridor

```text
External material
→ extracted source evidence
→ model proposes CandidateClaim
→ PIR grounds + validates
→ human ACCEPT / EDIT_AND_ACCEPT / REJECT / DEFER
→ only approved material may become a durable Claim
```

**CandidateClaim is a model proposal. Claim is a durable governed record.** The model cannot directly promote one into the other. Only `ACCEPT` and `EDIT_AND_ACCEPT` may result in durable Claim creation.

## Bounded V008 result

The validation used five frozen public-safe synthetic fixtures: technical, marketing, experience/opinion, mixed, and a bounded injection fixture. Expected material spans were defined before execution.

| Evidence | Result |
| --- | --- |
| Expected material coverage | **5 / 5** |
| Grounding violations | **0** |
| Human decisions | **5 ACCEPT / 1 REJECT** |
| Operator manual-work-reduction judgment | **YES** |
| Model calls / retries | 5 / 0 |
| Structured responses | 5 / 5 |
| Valid CandidateClaims | 6 |
| Duplicates | 0 |
| Non-material noise | 1 / 6 (16.7%) |
| Reconciled hosted-model spend | $0.002041 of a $0.05 experiment ceiling |

The top-line results are deliberately fixture-bounded. They demonstrate a controlled validation result, not a production performance benchmark.

## Human authority stayed active

The six valid CandidateClaims were not treated as self-authorizing. A human accepted five and rejected one subjective distractor:

| Candidate proposal | Human decision |
| --- | --- |
| Protocol reduces failed retries 40%. | ACCEPT |
| Platform cuts deployment time in half. | ACCEPT |
| Workflow prevented three incidents last month. | ACCEPT |
| Service launched in June. | ACCEPT |
| Best option for everyone. | REJECT |
| Release reduced outages 20%. | ACCEPT |

The rejection matters: valid structured output is not automatically approved knowledge.

## Grounding is not fact verification

The model supplied supporting excerpts. PIR required each excerpt to match the attested source segment **exactly and uniquely**, then derived offsets deterministically. No fuzzy quote repair was allowed. All six final candidates passed the unchanged production validator.

That is exact grounding plus deterministic validation. It is not automatic fact verification.

## Failure investigation improved the contract

The test evolved through a compact failure-to-fix sequence:

- **V006:** real inference succeeded, but the temporary harness did not preserve enough safe diagnostic evidence.
- **V007:** improved observability exposed the actual issue—the model had been asked to generate data PIR itself should own.
- **V008:** the contract was corrected. The model generated semantic content; PIR retained system identity, exact offsets, accepted enum constraints, and deterministic validation.

The production validator was **not weakened** to accommodate the integration. This is evidence of contract design and provider-boundary debugging, not model authority.

## Bounded controls

The validation reconciled $0.002041 of hosted-model spend against an explicit $0.05 experiment ceiling. It also included a synthetic injection fixture: the expected candidate was extracted and no source instruction altered tool access, routing, authority, privacy, spend, or schema behavior.

That fixture is bounded evidence only. It does not establish broad prompt-injection resistance.

## What this evidence does not prove

- Five synthetic fixtures are not production-scale validation.
- PIR is not an autonomous research system or automatic fact checker.
- The result does not prove full evidence adjudication, routine hosted inference, enterprise deployment, or scale economics.
- The hosted-model execution was a bounded validation harness, not a standing production hosted-model platform.

## Matthew’s role

Matthew designed the refinery’s operating model, provenance and authority boundaries, deterministic validation strategy, provider/system contract, and real-model value test; directed bounded implementation and failure investigation; and retained human authority over promotion of model proposals into durable claims.
