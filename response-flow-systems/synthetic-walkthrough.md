# Fictional walkthrough: stale approval fails closed

**Everything in this walkthrough is fictional.** The business, lead, message, review state, and outcome are invented. No real prospect, customer, contact, outreach record, or live send is depicted.

## Scenario

Fictional business **Harborlight Services** receives an inquiry from fictional organization **Cedar Works**. A proposed response, **Response A**, is prepared for human review in an offline governance workflow.

The walkthrough demonstrates accepted offline governance contracts. It does not depict Gmail, Sheets, Make, a provider call, or an external send.

## 1. Proposed response is not authority

The draft is associated with the fictional lead and its current evidence context. It is a proposal, not permission to act.

## 2. Human review and exact approval

A reviewer approves Response A as reviewed: its content, the relevant items, the current queue state, and the evidence context are bound together. The approval is meaningful precisely because it is not a general, reusable “yes.”

## 3. A relevant change occurs after approval

Before any next step, new fictional information changes the intended response: the lead requests a different contact window and the draft is revised to **Response B**. The stored approval still describes Response A and the earlier state.

## 4. The old approval is rejected

The governance contract compares the approval to the current reviewed state. Because the content and context no longer match, the old approval is not treated as current authority.

The item **fails closed**: it pauses and returns to review. It does not silently advance on the strength of an approval that no longer matches the proposed action.

## 5. Lineage remains distinct

Suppose a later fictional incoming message refers to the thread but carries a different message identity than the original proposed response. Thread relationship alone is not enough to prove the identity or status of a particular message. The system keeps resource identity, message identity, reply/thread lineage, and bounce lineage distinct.

That distinction prevents a loosely related signal from being treated as confirmation of the wrong item.

## 6. Renewed human review

The reviewer can inspect Response B and the new context, then approve that exact state or decline it. The walkthrough ends at the governance boundary: it shows valid or invalid eligibility, not a live external action.

## What this demonstrates

The system protects against stale approval, ambiguous lineage, and silent progression. It demonstrates offline deterministic governance around approval, evidence, and state—not live outbound automation.
