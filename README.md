# Agent Authority Audit

**Know exactly what your AI agents can do — and prove it.**

Agent platforms give you agents. This audit gives you a bounded, evidence-backed view of the authority those agents actually hold across repositories, tools, integrations, approval surfaces, and execution paths.

## The 48-hour audit

The Agent Authority Audit is a fixed-scope technical engagement for one bounded agent-enabled environment.

Within 48 hours of complete access/intake, the audit reconstructs and visualizes:

- actors and identities;
- repositories and connected operational surfaces;
- read / write / execute capability;
- tool and integration reachability;
- human approval gates and where they are actually enforced;
- delegation and authority boundaries;
- credential / trust-domain crossings;
- audit and evidence paths;
- verified constraints versus assumptions;
- highest-impact authority and control gaps.

The primary deliverable is an **Authority Map**, not a generic governance report.

## First supported environment profile

The initial commercial profile is intentionally narrow:

> **GitHub-centered agentic environments with runtime agents or coding agents connected to APIs, MCP/tool surfaces, databases, deployment systems, cloud services, messaging systems, or other operational integrations.**

The model/provider is not the organizing principle. Claude, OpenAI, Gemini, Copilot, custom Python agents, or another provider may sit inside the environment. The audit maps the **authority topology around the agent**.

## Five questions the audit answers

1. **What can act?**
2. **On what resources?**
3. **Under whose authority?**
4. **Where is approval actually enforced?**
5. **Can the decision and resulting effect be reconstructed afterward?**

## Deliverables

Every 48-hour Agent Authority Audit includes:

1. **Authority Map** — actors → identities → integrations → resources → permissions → approval gates → execution paths → evidence paths.
2. **Verified / Assumed Boundary View** — separates directly observed constraints from unverified claims or unavailable surfaces.
3. **Authority Findings** — hidden authority, excessive reach, missing enforcement, stale approval, weak revocation, unbounded delegation, or audit gaps.
4. **Severity / Consequence View** — findings arranged by consequence rather than by component count.
5. **Prioritized Remediation Plan** — smallest corrections first, with implementation dependencies called out.
6. **Control-Plane Fit Assessment** — identifies which gaps can be addressed through approval gates, delegation boundaries, revocation, policy enforcement, receipts, or operator/HUD surfaces.

See `docs/AUDIT_CONTRACT_V1.md` for the exact boundary.

## What this is not

The audit is not:

- a penetration test;
- a legal/compliance certification;
- a promise to enumerate access that cannot be directly evidenced;
- an automatic permission scanner that treats platform metadata as ground truth;
- authorization to change production systems;
- an implementation engagement bundled into discovery.

Unknowns remain unknown and are labeled as such.

## Commercial path

The product ladder is deliberately simple:

- **Structural Scan — $149**: small bounded manual structural review; useful as a low-friction first engagement.
- **Agent Authority Audit — fixed-scope paid engagement**: 48-hour Authority Map and remediation plan for one bounded environment.
- **Control Architecture / Remediation**: design of deterministic approval, delegation, revocation, identity, and evidence boundaries.
- **Implementation / Operations**: installation or adaptation of enforcement and operator control surfaces under separately agreed scope.

The audit pays for the discovery required to scope later implementation accurately. It does not manufacture an implementation sale by overstating findings.

## Operating principle

> **Observed authority is distinguished from claimed authority. Missing evidence does not become permission.**

The system is mapped as it can be verified, not as documentation says it ought to behave.

## Status

Agent Authority Audit v1 is being prepared for initial commercial validation. The methodology is provider-neutral; the first supported environment profile is GitHub-centered agentic operations.
