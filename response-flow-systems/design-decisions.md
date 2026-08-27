# Response Flow Systems design decisions

## Proposed action is not execution authority

**Decision:** Keep a proposed outbound action separate from the authority required to proceed.

**Why:** A draft can be useful without being trustworthy enough to authorize itself.

**Operational failure prevented:** Unreviewed or implicitly approved work advancing because it exists in a queue.

**Validation / boundary:** Accepted offline contracts validate approval controls. They do not claim live sends or autonomous execution.

## Approval binds to exact reviewed state

**Decision:** Bind approval to the reviewed content, command, session, items, queue state, and evidence context.

**Why:** An approval is meaningful only for the state a reviewer actually saw.

**Operational failure prevented:** A stale or changed draft borrowing approval that was given to an earlier version.

**Validation / boundary:** Exact reviewed-state binding is within the accepted offline authority; the walkthrough shows a synthetic stale-approval rejection.

## Identity and lineage remain distinct

**Decision:** Preserve distinct treatment for provider resource identity, message identity, thread/reply lineage, and bounce lineage.

**Why:** These signals answer different questions and should not be collapsed into a convenient but unsafe proxy.

**Operational failure prevented:** A related thread event or bounce being attributed to the wrong message or approval context.

**Validation / boundary:** Accepted validation covers identity and lineage controls, not live provider connectivity.

## Ambiguity fails closed

**Decision:** Reject, pause, or require review when evidence is malformed, stale, conflicting, or insufficient.

**Why:** In a consequential commercial workflow, uncertainty should remain visible rather than become an unnoticed assumption.

**Operational failure prevented:** Silent progression through conflicting approval, evidence, or state.

**Validation / boundary:** Offline deterministic checks support this behavior. Production concurrency and customer operation remain outside current maturity.
