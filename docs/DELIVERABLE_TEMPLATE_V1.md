# Agent Authority Audit v1 — Deliverable Template

## 1. Executive Authority Summary

### Environment audited
- Signed scope schedule:
- Delivery window:
- Primary agent/runtime:
- Repositories:
- Environments:
- Material principals:
- Operational integrations:
- Sampling/overflow notes:

### Bottom line
Answer in plain language:

- What can act within the observed scope?
- What can it affect?
- Where is approval technically binding?
- Where is authority only assumed, documented, partial, or unknown?
- What are the three highest-priority authority/control gaps?

State explicitly that this is a point-in-time, evidence-backed assessment of the agreed scope and does not prove the absence of undiscovered or inaccessible paths.

## 2. Authority Map

Represent each material path as:

`Actor → Effective Identity → Provider/Account/Tenant → Integration/Tool → Canonical Resource → Action → Gate → Execution/Effect → Evidence`

For every node/edge attach where applicable:

- stable subject/resource identifier;
- environment;
- evidence state: VERIFIED / PARTIALLY_VERIFIED / CLAIMED / UNKNOWN;
- access mode;
- impact dimensions;
- approval requirement;
- revocation state/freshness;
- evidence-source reference;
- point-in-time/freshness information;
- limitations or unavailable surfaces.

## 3. Authority Topology Table

| Subject ID | Actor | Effective Identity | Provider/Account/Tenant | Integration/Tool | Resource ID | Resource | Environment | Action / Access Mode | Gate | Execution / Effect | Revocation | Evidence State | Evidence Ref | Key Impact | Notes / Limits |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|

## 4. Findings Register

For each finding:

### F-### — Title
- **Evidence state:** VERIFIED / PARTIALLY_VERIFIED / CLAIMED / UNKNOWN
- **Access mode:** OBSERVE / READ / WRITE / TRIGGER / EXECUTE / DEPLOY / ADMINISTER / AUTHORIZE / DELEGATE
- **Confidentiality impact:** Low / Moderate / High / Critical
- **Integrity impact:** Low / Moderate / High / Critical
- **Availability impact:** Low / Moderate / High / Critical
- **Blast radius:** Low / Moderate / High / Critical
- **Irreversibility:** Low / Moderate / High / Critical
- **External consequence:** Low / Moderate / High / Critical
- **Control-plane reach:** Low / Moderate / High / Critical
- **Priority:**
- **Affected path:**
- **Observed condition:**
- **Evidence / freshness:**
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
- stale-state or retry risks visible from passive evidence;
- Council / Operator / security gates where applicable;
- any evidenced route around the intended approval surface;
- unresolved bypass questions that would require separately authorized active validation.

## 6. Integration Verification Ledger

| Integration | Provider/Account/Tenant | Claimed Capability | Verified Capability/Constraint | Verification Threshold Met? | Unknown Surface | Trust-Domain Crossing | Evidence / Freshness |
|---|---|---|---|---|---|---|---|

## 7. Aggregate Authority

Assess the union of permissions held by each material actor rather than viewing integrations individually.

Include:

- overlapping grants;
- chained tools;
- cumulative operation sequences;
- cross-environment reach;
- sensitive-data reach even when read-only;
- policy, identity, credential, approval, delegation, or audit surfaces reachable by the same actor;
- whether multiple low-impact capabilities combine into a higher-impact effect.

## 8. Evidence Reconstruction

For representative high-impact effects, answer whether the system can reconstruct:

1. who/what requested the action;
2. which effective identity acted;
3. which provider/account/tenant and integration carried the action;
4. which resource/action was targeted;
5. which policy/approval governed it;
6. what current state was evaluated;
7. what execution occurred;
8. what effect resulted;
9. whether execution matched authorization.

## 9. Prioritized Remediation

### Immediate — reduce highest-impact exposure
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

For each material gap identify whether remediation belongs primarily to:

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

## 11. Residual Unknowns and Scope Limitations

State every material unresolved, inaccessible, undisclosed, provider-internal, sampled, or out-of-scope surface explicitly. Do not silently transform incomplete evidence into a safe or unsafe verdict.

## 12. Audit Access Closure

Record:

- client-managed/delegated access removed or retained;
- temporary credentials expired/revoked;
- any intentional follow-on access and its separate authorization;
- any credential/security incident encountered during the engagement.

## 13. Handoff Decision

- [ ] No further action / risk accepted
- [ ] Client remediation using findings
- [ ] Control architecture engagement requested
- [ ] Implementation engagement requested

A follow-on engagement requires separate scope and authorization.
