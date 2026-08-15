# Agent Authority Audit v1 — Intake

This intake is designed to establish a bounded 48-hour engagement without requiring the client to expose more than necessary.

## 1. Environment

- Organization / company:
- Technical contact:
- Primary repository or repositories:
- Environment(s) in scope: LOCAL / DEVELOPMENT / STAGING / PRODUCTION
- Agent or coding-agent products in use:
- Known runtime/orchestration framework:

## 2. Connected surfaces

Check or list what the in-scope agents may interact with:

- GitHub / GitLab / other source control
- MCP servers
- cloud provider
- deployment platform
- database / data warehouse
- storage
- messaging / Slack / Teams
- ticketing / project management
- CI/CD
- secrets / credential manager
- browser / web automation
- internal APIs
- external APIs
- other operational tools

## 3. What currently worries you?

In plain language:

- What action are you least certain an agent can or cannot perform?
- Where do you believe a human approval is required?
- What would be the most damaging accidental action?
- Has there been an incident, near miss, surprising tool call, unauthorized change, or difficult-to-reconstruct action?
- What question are customers, security, leadership, or auditors already asking?

## 4. Known authority assumptions

List any statements currently treated as true, such as:

- “The agent is read-only.”
- “Production deploys always require a human.”
- “Only the service account can access this database.”
- “The model cannot modify its own policy.”
- “Retries cannot repeat a side effect.”

The audit will distinguish these assumptions from directly verified controls.

## 5. Evidence / access available

Identify what can be provided read-only:

- repository access
- workflow definitions
- policy/configuration files
- runtime traces
- integration metadata
- app / OAuth installation metadata
- IAM / role inventories
- deployment configuration
- architecture diagrams
- approval records
- audit/event logs

Do not send raw passwords, API keys, private keys, or secret values through this intake.

## 6. Explicit exclusions

List resources, repositories, environments, data, or integrations that must remain out of scope.

## 7. Delivery priority

Rank the most valuable output:

1. authority/security risk
2. human approval enforcement
3. production reachability
4. integration verification
5. audit / evidence reconstruction
6. customer / compliance readiness
7. control-plane implementation planning

## 8. Start condition

The 48-hour delivery clock begins when:

- scope is mutually understood;
- required read-only access is available;
- blocked/inaccessible surfaces are identified;
- the technical contact is reachable for material access ambiguity.
