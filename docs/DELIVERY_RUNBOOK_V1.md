# Agent Authority Audit v1 — 48-Hour Delivery Runbook

## Phase 0 — Scope freeze

Before the clock starts:

- confirm bounded environment;
- confirm repositories and environments in scope;
- confirm read-only access;
- confirm explicit exclusions;
- identify unavailable surfaces;
- confirm technical contact;
- record delivery start timestamp.

No discovery outside the agreed boundary occurs without scope change.

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

Record each item as verified, partially verified, claimed, or unknown.

## Phase 2 — Authority reconstruction

For each material actor:

1. resolve identity;
2. resolve reachable resources;
3. resolve actions/permissions;
4. trace indirect/chained paths;
5. identify approval gates;
6. identify execution identity;
7. identify evidence/receipt path;
8. identify revocation mechanism;
9. identify authority-changing surfaces;
10. calculate material aggregate authority.

## Phase 3 — Adversarial boundary checks

Test the architecture against bounded questions, without destructive execution:

- Is claimed read-only status mechanically true?
- Can a proposer also approve or execute?
- Can human approval be bypassed through another path?
- Can a retry repeat a side effect without fresh authorization?
- Can policy/resource aliases broaden access?
- Can an actor reach its own policy, identity, or approval controls?
- Do multiple grants combine into greater authority?
- Can production be reached indirectly?
- Can revocation be verified and propagated?
- Can the highest-consequence effects be reconstructed after the fact?

## Phase 4 — Authority Map

Render the effective topology:

`Actor → Identity → Tool/Integration → Resource → Action → Gate → Effect → Evidence`

Visual hierarchy should prioritize consequence and authority depth rather than component aesthetics.

Suggested visual grammar:

- outer field: observational/read-only;
- middle layers: mutation / durable operational effects;
- inner layers: production / sensitive resources;
- core: security, policy, credentials, delegation, audit integrity, final authority.

The visualization is an explanatory representation of observed controls; it is not itself an authorization source.

## Phase 5 — Findings and remediation

Each material finding must state:

- evidence;
- affected path;
- consequence;
- uncertainty;
- concrete failure mode;
- smallest corrective action;
- control-plane category;
- implementation dependency.

Avoid generic recommendations such as “improve governance” or “use least privilege” without naming the actual affected path.

## Phase 6 — Delivery quality gate

Before delivery, verify:

- every high-consequence claim has source evidence or explicit uncertainty;
- unknowns remain labeled unknown;
- no raw secret values appear in artifacts;
- recommendations do not imply controls were implemented;
- Authority Map and findings register agree;
- approval claims distinguish procedural review from technical enforcement;
- aggregate authority was considered for every material actor;
- the executive summary can be understood without reading the full evidence ledger.

## Phase 7 — Client handoff

Walk through in this order:

1. effective authority topology;
2. highest-consequence paths;
3. what is verified vs assumed;
4. where human authority is binding vs advisory;
5. smallest remediation sequence;
6. unresolved surfaces;
7. optional next engagement.

The client receives the audit artifacts whether or not they purchase follow-on work.
