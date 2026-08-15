# Agent Authority Audit v1 — Intake and Scope Freeze

This intake establishes the signed, quantitatively bounded 48-hour engagement without requiring the client to expose more than necessary.

## 1. Organization and technical contact

- Organization / company:
- Technical contact:
- Security/contact escalation point:

## 2. Quantitative v1 scope

Default caps unless separately quoted:

- up to 3 repositories;
- up to 2 environments;
- up to 10 material actor/identity principals;
- up to 8 material integrations/tool surfaces;
- up to 25 material authority paths;
- up to 40 substantive evidence-source items.

Record the agreed scope:

- Included repositories:
- Included environments: LOCAL / DEVELOPMENT / STAGING / PRODUCTION
- Included material principals:
- Included integrations/tool surfaces:
- Expected material authority paths, if known:
- Expected evidence-source items:
- Representative-path sampling rule if a cap is exceeded:
- Explicit exclusions:

Anything beyond the accepted caps is prioritized/sampled transparently or separately re-scoped. It does not silently expand the 48-hour obligation.

## 3. Agent/runtime profile

- Agent or coding-agent products in use:
- Known runtime/orchestration framework:
- Primary entry points:
- Provider/account/tenant or trust domains:

## 4. Connected surfaces

Check/list only in-scope surfaces:

- source control
- MCP servers
- cloud provider
- deployment platform
- database / data warehouse
- storage
- messaging
- ticketing / project management
- CI/CD
- secrets / credential manager
- browser / web automation
- internal APIs
- external APIs
- policy / approval systems
- audit / telemetry systems
- other operational tools

## 5. What currently worries you?

- What action are you least certain an agent can or cannot perform?
- Where do you believe a human approval is required?
- What would be the most damaging accidental action or disclosure?
- Has there been an incident, near miss, surprising tool call, unauthorized change, or difficult-to-reconstruct action?
- What question are customers, security, leadership, or auditors already asking?

## 6. Known authority assumptions

List statements currently treated as true, for example:

- “The agent is read-only.”
- “Production deploys always require a human.”
- “Only the service account can access this database.”
- “The model cannot modify its own policy.”
- “Retries cannot repeat a side effect.”

These remain claims until the applicable verification threshold is met.

## 7. Evidence available

Identify read-only evidence that can be inspected:

- repository/configuration state
- workflow definitions
- policy files
- runtime traces
- integration metadata
- app / OAuth installation metadata
- IAM / role inventories
- deployment configuration/state
- architecture diagrams
- approval records
- audit/event logs
- revocation records/state

## 8. Temporary access method

Preferred order:

1. client-managed/federated or delegated read-only access;
2. scoped app/service access controlled by the client;
3. time-limited least-privilege temporary token/session only when necessary.

Record:

- Access mechanism:
- Scope/role granted:
- Expiry:
- Client revocation method:
- Approved secure transfer channel if a temporary token is unavoidable:

**Do not place raw passwords, API keys, private keys, recovery codes, or secret values in this intake, email, chat, issues, source control, screenshots, or audit artifacts.**

## 9. Active validation

Standard audit posture is passive evidence analysis.

- Is any active validation requested? YES / NO

If YES, it is not authorized by this intake alone. A separate written test plan must specify sandbox/non-production target where feasible, identities, exact allowed/prohibited actions, stop conditions, expected effects, rollback/restoration, monitoring/contact, and explicit authorization.

## 10. Delivery priorities

Rank:

1. authority/security exposure
2. confidentiality/sensitive-data reach
3. human approval enforcement
4. production/control-plane reachability
5. integration verification
6. audit / evidence reconstruction
7. customer / compliance readiness
8. control-plane implementation planning

## 11. Start condition / scope acceptance

The 48-hour clock begins when:

- this quantitative scope is accepted;
- required read-only access is ready;
- blocked/inaccessible surfaces are identified;
- sampling/overflow rules are understood;
- the technical contact is reachable for material ambiguity.

Client scope acceptance:
- Name / role:
- Date / time:
- Accepted scope version/reference:

Audit start timestamp:
