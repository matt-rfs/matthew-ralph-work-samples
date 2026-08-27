# Job Opportunity Engine design decisions

## Deterministic authority around model-assisted work

**Decision:** Keep identity, state, validation, and consequential evaluation rules deterministic even where AI may assist interpretation.

**Why:** A career workflow needs a stable account of what was considered and why, not a moving interpretation that cannot be inspected later.

**Risk prevented:** A plausible model output silently changing a consequential decision or creating inconsistent evaluation.

**Validation / boundary:** Provider-neutral generation contracts and synthetic test behavior are bounded by deterministic validation. No live provider-backed generation runtime is claimed.

## Evidence-backed claims rather than generated truth

**Decision:** Require prepared claims to point back to governed evidence and validate them deterministically.

**Why:** A polished sentence can exceed what evidence supports.

**Risk prevented:** Unsupported metrics, capabilities, or interpretations entering a preparation artifact.

**Validation / boundary:** Claim validation and artifact-to-evidence relationships are implemented. Private claim manifests and evidence contents are not published.

## Frozen preparation packets and visible divergence

**Decision:** Freeze the verified job, evaluation, evidence, capability, and baseline basis for a preparation packet; surface divergence if that basis changes.

**Why:** A package that was valid for one snapshot must not silently remain authoritative after relevant facts change.

**Risk prevented:** Stale preparation being mistaken for current approved material.

**Validation / boundary:** Packet persistence and divergence checks are implemented. This does not claim a completed production approval or submission workflow.

## Private artifact custody and resume lineage

**Decision:** Keep preparation artifacts private, profile-owned, traceable, and linked to approved evidence and resume lineage.

**Why:** Preparation materials can contain sensitive candidate information even when their governing controls are useful to discuss publicly.

**Risk prevented:** Cross-profile leakage, path exposure, or public release of private artifacts.

**Validation / boundary:** Private storage, ownership, digest, and evidence-link controls are tested. Production DOCX/PDF artifact QA remains incomplete.

## Human control for final external action

**Decision:** Prepare material for review while retaining a human boundary before final external action.

**Why:** Career claims and submission decisions are consequential and require accountable judgment.

**Risk prevented:** An automated submission representing a person with incomplete, stale, or unsupported claims.

**Validation / boundary:** `NEEDS_HUMAN` and `REVIEW_READY` support review-state visibility. Final autonomous submission is outside scope.
