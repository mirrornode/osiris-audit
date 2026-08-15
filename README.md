# Agent Authority Audit

**See what your AI agents can do — with an evidence-backed authority map.**

Agent platforms give you agents. This audit gives you a point-in-time, bounded view of the authority those agents can be shown to hold across repositories, tools, integrations, approval surfaces, and execution paths.

## The 48-hour audit

The Agent Authority Audit is a fixed-scope technical engagement for one quantitatively capped agent-enabled environment.

The 48-hour clock begins after signed scope freeze, complete intake, and access readiness. Standard v1 scope is capped at up to 3 repositories, 2 environments, 10 material principals, 8 material integrations/tool surfaces, 25 material authority paths, and 40 substantive evidence-source items unless separately quoted.

Within that scope, the audit reconstructs and visualizes:

- actors and effective identities;
- provider/account/tenant or trust-domain context;
- repositories and connected operational surfaces;
- read/write/trigger/execute/administer capability;
- tool and integration reachability;
- human approval gates and whether they are technically binding;
- delegation and authority boundaries;
- credential / trust-domain crossings;
- revocation state where observable;
- audit and evidence paths;
- verified constraints versus partial, claimed, or unknown surfaces;
- highest-impact authority and control gaps.

The primary deliverable is an **Authority Map**, not a generic governance report.

## First supported environment profile

> **GitHub-centered agentic environments with runtime agents or coding agents connected to APIs, MCP/tool surfaces, databases, deployment systems, cloud services, messaging systems, or other operational integrations.**

The model/provider is not the organizing principle. Claude, OpenAI, Gemini, Copilot, custom Python agents, or another provider may sit inside the environment. The audit maps the **authority topology around the agent**.

## Five questions the audit answers

1. **What can act within the observed scope?**
2. **On what resources?**
3. **Under whose authority?**
4. **Where is approval actually enforced?**
5. **Can the decision and resulting effect be reconstructed afterward?**

## Deliverables

Every 48-hour Agent Authority Audit includes:

1. **Authority Map** — actor → effective identity → provider/account → integration → resource → action → gate → execution/effect → evidence.
2. **Evidence State View** — `VERIFIED / PARTIALLY_VERIFIED / CLAIMED / UNKNOWN` applied per material claim/edge using claim-specific thresholds.
3. **Authority Findings** — excessive reach, weak approval enforcement, unsafe composition, revocation gaps, stale-state risks, sensitive-data exposure, or missing evidence.
4. **Impact View** — confidentiality, integrity, availability, blast radius, irreversibility, external consequence, and control-plane reach kept separate from access mode and evidence confidence.
5. **Prioritized Remediation Plan** — smallest corrections first, with dependencies and uncertainty called out.
6. **Control-Plane Fit Assessment** — identifies which gaps belong to identity, policy, approval, delegation, revocation, receipts, aggregate-authority controls, or operator/HUD surfaces.

See `docs/AUDIT_CONTRACT_V1.md` for the exact boundary and `docs/DELIVERABLE_TEMPLATE_V1.md` for the claim/edge evidence model.

## Validation posture

The standard audit is passive-by-default. We inspect configuration, metadata, policy, logs, traces, and existing records. Live bypass attempts, grant mutation, production effects, or active security testing require a separately authorized written test plan.

## What this is not

The audit is not:

- a penetration test;
- a legal/compliance certification;
- a guarantee of complete organization-wide authority discovery;
- an automatic permission scanner that treats platform metadata as ground truth;
- authorization to change production systems;
- an implementation engagement bundled into discovery.

Unknowns remain unknown and are labeled as such.

## Commercial path

- **Structural Scan — $149**: separately defined low-friction entry engagement. See `docs/STRUCTURAL_SCAN_V1.md` for its scope, turnaround, evidence standard, outputs, exclusions, and comparison with the full audit.
- **Agent Authority Audit — fixed-scope paid engagement**: capped 48-hour Authority Map and remediation plan.
- **Control Architecture / Remediation**: deterministic approval, delegation, revocation, identity, policy, and evidence design.
- **Implementation / Operations**: installation or adaptation of enforcement and operator-control surfaces under separately agreed scope.

The audit pays for the discovery required to scope later implementation accurately. It does not manufacture an implementation sale by overstating findings.

## Access posture

All temporary audit/scan access must be removed or expired at delivery. Continued access is permitted only under a separately authorized follow-on engagement that explicitly governs its scope and duration.

## Operating principle

> **Observed authority is distinguished from claimed authority. Missing evidence does not become permission.**

The result is a point-in-time evidence-backed map of the agreed observable scope. It does not prove that inaccessible, undisclosed, provider-internal, future, or out-of-scope paths do not exist.

## Status

Agent Authority Audit v1 is being prepared for initial commercial validation. The methodology is provider-neutral; the first supported environment profile is GitHub-centered agentic operations.
