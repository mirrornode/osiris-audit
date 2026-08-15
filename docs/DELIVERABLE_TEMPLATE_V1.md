# Agent Authority Audit v1 — Deliverable Template

## 1. Executive Authority Summary

### Environment audited
- Scope:
- Delivery window:
- Primary agent/runtime:
- Repositories:
- Operational integrations:

### Bottom line
Answer in plain language:

- What can act?
- What can it affect?
- Where is approval technically binding?
- Where is authority only assumed or documented?
- What are the three highest-consequence gaps?

## 2. Authority Map

Represent each material path as:

`Actor → Identity → Integration/Tool → Resource → Action → Gate → Effect → Evidence`

For every node/edge, attach where applicable:

- evidence state: VERIFIED / PARTIALLY_VERIFIED / CLAIMED / UNKNOWN;
- consequence: L0–L4;
- environment;
- approval requirement;
- revocation state;
- source reference.

## 3. Authority Topology Table

| Actor | Identity | Resource | Action | Gate | Evidence state | Consequence | Notes |
|---|---|---|---|---|---|---|---|

## 4. Findings Register

For each finding:

### F-### — Title
- **Consequence:** L0 / L1 / L2 / L3 / L4
- **Evidence state:** VERIFIED / PARTIALLY_VERIFIED / CLAIMED / UNKNOWN
- **Affected path:**
- **Observed condition:**
- **Why it matters:**
- **Failure mode:**
- **Smallest corrective action:**
- **Longer-term control:**
- **Dependencies / caveats:**

## 5. Approval Boundary Review

Document:

- approvals that are actually enforced;
- approvals that exist only in UI/procedure/documentation;
- same-actor proposal/approval/execution paths;
- stale-state or retry risks;
- Council / Operator / security gates where applicable;
- any route capable of bypassing the intended approval surface.

## 6. Integration Verification Ledger

| Integration | Claimed capability | Directly verified capability | Unknown surface | Trust-domain crossing | Evidence |
|---|---|---|---|---|---|

## 7. Aggregate Authority

Assess the union of permissions held by each material actor rather than viewing integrations individually.

Include:

- overlapping grants;
- chained tools;
- cumulative operation sequences;
- cross-environment reach;
- policy or identity surfaces reachable by the same actor;
- whether multiple low-consequence capabilities combine into a higher-consequence effect.

## 8. Evidence Reconstruction

For representative high-consequence effects, answer whether the system can reconstruct:

1. who/what requested the action;
2. which identity actually acted;
3. which policy/approval governed it;
4. what current state was evaluated;
5. what execution occurred;
6. what effect resulted;
7. whether execution matched authorization.

## 9. Prioritized Remediation

### Immediate — reduce high-consequence exposure
1.
2.
3.

### Next — make authority explicit and enforceable
1.
2.
3.

### Later — control-plane / operator improvements
1.
2.
3.

## 10. Control-Plane Fit

For each material gap, identify whether remediation belongs primarily to:

- identity;
- resource canonicalization;
- policy decision;
- policy enforcement;
- explicit approval;
- delegation;
- revocation / expiry;
- aggregate-authority control;
- authorization receipt;
- execution receipt;
- operator/HUD visibility;
- monitoring / alerting.

## 11. Residual Unknowns

State every material unresolved surface explicitly. Do not silently transform incomplete evidence into a safe or unsafe verdict.

## 12. Handoff Decision

- [ ] No further action / risk accepted
- [ ] Client remediation using findings
- [ ] Control architecture engagement requested
- [ ] Implementation engagement requested

A follow-on engagement requires separate scope and authorization.
