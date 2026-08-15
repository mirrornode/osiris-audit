# Agent Authority Audit v1 — 48-Hour Delivery Runbook

## Phase 0 — Scope freeze

Before the clock starts:

- accept the signed scope schedule and quantitative caps;
- confirm repositories, environments, principals, integrations, and evidence-source limits;
- confirm read-only access and credential lifecycle;
- confirm explicit exclusions and unavailable surfaces;
- confirm representative-path sampling rules if caps may be exceeded;
- confirm technical contact;
- record delivery start timestamp.

No discovery outside the agreed boundary occurs without a scope change.

## Phase 1 — Inventory

Build the initial actor/resource graph:

- humans and service identities;
- agents / coding agents / runtimes;
- repositories;
- workflows and CI/CD;
- MCP/tool integrations;
- APIs;
- databases/storage;
- cloud/deployment surfaces;
- messaging/project systems;
- policy / approval / audit surfaces.

Record each material claim using the contract verification matrix: VERIFIED, PARTIALLY_VERIFIED, CLAIMED, or UNKNOWN.

## Phase 2 — Authority reconstruction

For each material actor:

1. resolve stable subject and effective identity;
2. record provider/account/tenant or trust domain;
3. resolve reachable resources and stable identifiers;
4. resolve actions/access modes;
5. trace indirect/chained integrations;
6. identify approval/policy gates;
7. identify execution/effect identity;
8. identify evidence/receipt path;
9. identify revocation mechanism/freshness;
10. identify authority-changing surfaces;
11. calculate material aggregate authority.

## Phase 3 — Passive adversarial boundary analysis

By default, evaluate the architecture through existing evidence only. Do not issue live bypass attempts, mutate grants, replay effects, or exercise production actions.

Analyze:

- whether claimed read-only status is supported by effective enforcement evidence;
- whether proposer/approver/executor roles collapse into the same authority path;
- whether human approval is technically binding or merely procedural;
- whether existing traces show retries capable of repeating effects without reauthorization;
- whether resource aliases or policy references create scope ambiguity;
- whether an actor can reach its own policy, identity, approval, audit, or delegation controls;
- whether multiple grants compose into greater authority;
- whether production/control-plane reach is evidenced;
- whether revocation state is consumed by enforcement within the claimed bound;
- whether representative high-impact effects can be reconstructed afterward.

Any active validation moves to a separately authorized test plan containing target, identities, exact allowed/prohibited actions, stop conditions, expected effect, rollback/restoration, monitoring contact, and explicit client authorization. Without that plan, unresolved active-behavior questions remain PARTIALLY_VERIFIED or UNKNOWN as appropriate.

## Phase 4 — Authority Map

Render each material path as:

`Actor → Effective Identity → Provider/Account/Tenant → Integration/Tool → Resource → Action → Gate → Execution/Effect → Evidence`

Attach stable identifiers, environment, evidence state, access mode, impact dimensions, revocation state, evidence references, and limitations where available.

Visual hierarchy should prioritize consequence and authority depth rather than component aesthetics. Suggested visual grammar:

- outer field: low-impact observational capability;
- middle layers: durable mutation / operational effects;
- inner layers: production, sensitive information, or broad blast radius;
- core: identity, credentials, policy, approval, delegation, audit integrity, and final authority.

Read-only sensitive-data exposure may sit deep in the field because confidentiality impact is separate from access mode.

The visualization is explanatory; it is not itself an authorization source.

## Phase 5 — Findings and remediation

Each material finding states:

- evidence state;
- evidence references/freshness;
- affected authority path;
- access mode;
- confidentiality/integrity/availability/blast-radius/irreversibility/external-consequence/control-plane impacts;
- concrete failure mode;
- smallest corrective action;
- control-plane category;
- implementation dependency;
- residual uncertainty.

Avoid generic recommendations that do not name the affected path.

## Phase 6 — Delivery quality gate

Before delivery verify:

- quantitative scope caps and sampling are disclosed;
- every VERIFIED claim meets its claim-specific threshold;
- static configuration is not described as deployed enforcement without corroboration;
- UNKNOWN remains UNKNOWN;
- no live validation occurred without its own authorized test plan;
- no raw credentials or secret values appear in artifacts/logs;
- audit access lifecycle is documented for closure;
- findings separate evidence confidence from impact;
- Authority Map and topology table preserve the same complete path;
- approval claims distinguish procedural review from technical enforcement;
- aggregate authority was considered for every material actor;
- executive summary states point-in-time and scope limitations.

## Phase 7 — Client handoff

Walk through:

1. scope and evidence limitations;
2. effective authority topology;
3. highest-priority impact paths;
4. verified versus assumed/unknown controls;
5. where human authority is binding versus advisory;
6. smallest remediation sequence;
7. unresolved surfaces;
8. audit-access closure;
9. optional separately scoped next engagement.

The client receives the audit artifacts whether or not follow-on work is purchased.
