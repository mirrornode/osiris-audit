# Agent Authority Audit v1 — Engagement Contract

**Status:** Commercial validation draft  
**Delivery target:** 48 hours after signed scope freeze, complete bounded intake, and access readiness  
**Scope unit:** One quantitatively capped agent-enabled environment

## 1. Objective

Produce a point-in-time, evidence-backed reconstruction and visualization of the effective authority topology inside an agreed scope. The audit distinguishes directly verified controls from partial evidence, documentation, and unresolved surfaces.

The audit is diagnostic. It does not itself modify production authority and does not guarantee discovery of every authority path outside the agreed or observable scope.

## 2. Scope schedule and start condition

The 48-hour clock begins only after a written scope schedule is accepted.

Default v1 caps unless separately quoted:

- up to 3 repositories;
- up to 2 environments;
- up to 10 material actor/identity principals;
- up to 8 material integrations/tool surfaces;
- up to 25 material authority paths;
- up to 40 evidence-source items requiring substantive review.

The scope schedule identifies:

- included repositories and environments;
- named agent/runtime entry points;
- included integrations and trust domains;
- material identities/principals;
- explicit exclusions;
- known unavailable surfaces;
- client technical contact;
- evidence sources expected at start;
- any representative-path sampling rules.

If discovery exceeds a cap, the auditor does not silently expand the engagement. The client receives either: (a) prioritized representative-path coverage within the original cap, or (b) a written scope-change option for added time/cost. The 48-hour commitment applies to the accepted capped scope.

## 3. Evidence classes and verification threshold

Every material claim has an evidence state and a claim type. Evidence sufficiency depends on the claim being made.

### VERIFIED
The evidence available within scope is sufficient for the exact claim, at the stated point in time, under the verification matrix below. VERIFIED does not imply that no alternate path exists outside observed scope.

### PARTIALLY_VERIFIED
One or more material links required by the verification matrix are missing, stale, indirect, or deployment status cannot be corroborated.

### CLAIMED / DOCUMENTED
A stakeholder, policy, configuration, diagram, or documentation states the behavior, but the evidence threshold for VERIFIED was not met.

### UNKNOWN
The claim cannot be resolved within scope. UNKNOWN is not interpreted as safe, unsafe, allowed, or denied.

### Verification matrix

| Claim type | Minimum evidence for VERIFIED |
|---|---|
| Capability exists | Effective identity/permission evidence plus a current configuration or runtime/integration source linking the identity to the resource/action. |
| Capability denied / read-only | Effective permission or enforcement evidence showing the denied action is unavailable at the relevant enforcement point; static documentation alone is insufficient. |
| Human approval is binding | Evidence of the execution path and the technical gate that prevents effect without valid approval; UI/procedure evidence alone is insufficient. |
| Production reachability | Current deployment/integration path plus effective identity/permission evidence reaching the production resource. |
| Policy constraint is enforced | The policy/configuration version plus evidence that the relevant runtime/enforcement component is actually using or enforcing it. |
| Revocation works | Current revocation mechanism/configuration and evidence showing the enforcement surface consumes or checks that state within the claimed bound. |
| Audit reconstruction exists | Request/decision/execution/effect records can be linked for at least one representative path without relying on undocumented inference. |
| Absence of alternate path | Not assigned VERIFIED by this audit unless the bounded scope is demonstrably exhaustive for that trust domain; otherwise state the limitation explicitly. |

Evidence freshness is recorded where material. Static repository content may verify declared configuration at a revision, but not deployed enforcement unless deployment/use is independently corroborated.

## 4. Authority dimensions

The audit maps:

- actor / subject;
- effective identity;
- provider/account/tenant or trust domain;
- action;
- canonical resource;
- integration/tool path;
- environment;
- approval or policy gate;
- effect/execution identity;
- evidence path;
- revocation;
- composition / aggregate authority.

## 5. Impact and priority model

Access mode, evidence confidence, and impact are recorded separately. No single ordinal level substitutes for these dimensions.

### Access mode

`OBSERVE / READ / WRITE / TRIGGER / EXECUTE / DEPLOY / ADMINISTER / AUTHORIZE / DELEGATE`

### Impact dimensions

Each finding records Low / Moderate / High / Critical where applicable for:

- **Confidentiality** — exposure of protected or sensitive information;
- **Integrity** — ability to alter protected state or outputs;
- **Availability** — ability to disrupt or remove service/resource availability;
- **Blast radius** — breadth of affected resources/users/environments;
- **Irreversibility** — difficulty of restoring the prior state;
- **External consequence** — customer, financial, legal, public, or third-party effect;
- **Control-plane reach** — ability to alter identity, policy, approval, delegation, credentials, audit evidence, or enforcement itself.

Evidence confidence remains the separate VERIFIED / PARTIALLY_VERIFIED / CLAIMED / UNKNOWN state.

### Priority

Final priority is an auditor judgment derived from the impact dimensions, access mode, exploitability/feasibility of the observed path, aggregate composition, and uncertainty. The report must state the contributing dimensions rather than presenting a bare score.

Read-only access to secrets or customer data can therefore be high-priority confidentiality exposure even though its access mode is READ.

## 6. Authority Map

The primary artifact represents:

`actor → effective identity → provider/account/tenant → integration/tool → canonical resource → action → gate → execution/effect → evidence`

Each material edge includes, where available:

- stable subject and resource identifier;
- environment;
- evidence state;
- access mode;
- impact dimensions;
- approval requirement;
- revocation state/freshness;
- evidence-source reference;
- limitations/unknowns.

The map must expose indirect paths, trust-domain crossings, procedural-versus-technical approvals, aggregate authority, production/control-plane reach, and evidence discontinuities.

## 7. Validation posture

The standard audit is **passive evidence analysis by default**. It may inspect configuration, metadata, policy, logs, traces, and existing records, but does not issue live requests intended to test bypass, mutate grants, exercise production effects, or alter authorization state.

Any active validation requires a separately approved written test plan specifying:

- non-production/sandbox target where feasible;
- test identities/accounts;
- exact allowed actions;
- prohibited actions;
- stop conditions;
- expected observable effect;
- rollback/restoration plan;
- monitoring/contact during the test;
- explicit client authorization.

Without that test plan, questions such as bypassability, retry side effects, and revocation propagation are answered from passive evidence and labeled according to the evidence threshold achieved.

## 8. Required findings categories

The audit examines, within the agreed passive scope, excessive/undocumented authority, unverified integrations, weak approval enforcement, same-actor authority concentration, stale state/approval, revocation gaps, resource ambiguity, aggregate composition, policy-integrity gaps, execution/evidence discontinuity, and misleading UI representations.

## 9. Deliverables

- Executive authority summary;
- Authority Map;
- Evidence ledger;
- findings register with separate impact dimensions and evidence state;
- prioritized remediation plan;
- control-plane fit assessment;
- residual unknowns and scope limitations.

## 10. Explicit exclusions

Unless separately contracted and authorized:

- exploit development or penetration testing;
- live bypass attempts;
- social engineering;
- credential harvesting;
- destructive testing;
- production changes;
- legal/compliance certification;
- unlimited organization-wide discovery;
- inference about inaccessible provider-internal behavior.

## 11. Temporary access lifecycle

Client access is treated as temporary audit access.

- Prefer client-managed, federated, delegated, or app-based read-only access over shared credentials.
- Raw passwords, private keys, API keys, recovery codes, or secret values MUST NOT be sent through ordinary intake documents, email, chat, repository issues, or audit artifacts.
- If a temporary token/session is unavoidable, transfer must use a client-approved secure channel and the credential must be least-privileged, scoped to the engagement, and time-limited.
- Credential values must not be committed to source control or copied into findings, screenshots, logs, prompts, or deliverables.
- Local/tool logging that could capture credential values must be disabled, redacted, or reviewed before use.
- Access must be revocable by the client throughout the engagement.
- All audit access MUST be removed or expired at delivery.
- Continued access after delivery is permitted only under a separately authorized follow-on engagement that explicitly identifies the retained access, scope, purpose, and new expiry/review point.
- Any suspected credential disclosure or unintended privilege must be reported to the client contact promptly and use of that credential stops until disposition.
- The delivery record MUST confirm that audit access was removed/expired, or identify the separately authorized follow-on engagement governing continued access.

## 12. Timing and completeness limitation

The delivery target is 48 hours for the signed capped scope after access readiness. Blocking access or client-requested holds pause the clock.

The audit is a point-in-time assessment of evidence observable within the agreed scope. It does not warrant that inaccessible, undisclosed, provider-internal, future, or out-of-scope authority paths do not exist.

## 13. Handoff

The client may accept risk, remediate internally, request a separate architecture engagement, or request separately scoped implementation. Purchase of the audit does not authorize remediation or production change.
