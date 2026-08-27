# Job Opportunity Engine design decisions

## Deterministic authority around model-assisted work

**Decision:** Keep identity, state, validation, and consequential evaluation rules deterministic even where AI may assist interpretation.

**Why:** A career workflow needs a stable account of what was considered and why, not a moving interpretation that cannot be inspected later.

**Risk prevented:** A plausible model output silently changing a consequential decision or creating inconsistent evaluation.

**Validation / boundary:** The clean public checkpoint includes deterministic evaluation and state controls. It does not claim autonomous search or final submission.

## Evidence-backed claims rather than generated truth

**Decision:** Treat generated language as preparation, not as authoritative candidate evidence.

**Why:** A polished sentence can exceed what the evidence supports.

**Risk prevented:** Unsupported capability inflation in an evaluation or application artifact.

**Validation / boundary:** Evidence governance and approved capability matching are within the public checkpoint; private evidence contents are not published.

## Explicit profile isolation

**Decision:** Keep candidate evidence and profile context isolated rather than allowing broad, implicit reuse.

**Why:** Relevance, ownership, and privacy depend on knowing which approved evidence belongs to which context.

**Risk prevented:** Cross-context evidence use and accidental disclosure of private career material.

**Validation / boundary:** Candidate isolation and privacy guards are part of the safe public validation description. No real profile or evidence identifiers appear here.

## Human control for final external action

**Decision:** Prepare material for review while retaining a human boundary before final external action.

**Why:** Career claims and submission decisions are consequential and require accountable judgment.

**Risk prevented:** An automated submission representing a person with an incomplete, stale, or unsupported claim.

**Validation / boundary:** The system can support review-oriented preparation at the clean public checkpoint. Final autonomous submission is outside scope.
