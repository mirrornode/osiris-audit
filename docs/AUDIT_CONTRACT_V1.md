# Agent Authority Audit v1 — Engagement Contract

**Status:** Commercial validation draft  
**Delivery target:** 48 hours after complete bounded intake and access readiness  
**Scope unit:** One bounded agent-enabled environment

## 1. Objective

Reconstruct and visualize the effective authority topology of an agent-enabled operational environment, clearly separating directly verified capability from assumptions, undocumented expectations, and inaccessible surfaces.

The audit is diagnostic. It does not itself modify production authority.

## 2. Required intake

The 48-hour clock begins only after the agreed intake is complete.

Minimum intake:

- primary repository or repository set in scope;
- named environment(s): local / development / staging / production;
- known agent or coding-agent entry points;
- known tool, MCP, API, database, cloud, deployment, messaging, or workflow integrations;
- available configuration / policy / workflow files;
- read-only access sufficient to inspect the agreed surfaces;
- a named technical contact for access clarification;
- explicit exclusions and protected surfaces that must not be inspected.

Optional but valuable:

- current architecture diagram;
- existing IAM / role / service-account inventory;
- deployment topology;
- approval workflow documentation;
- security or compliance requirements;
- recent incident or near-miss motivating the audit.

## 3. Evidence classes

Every material claim in the audit is assigned one of four states:

### VERIFIED
Direct evidence supports the stated capability, boundary, or constraint.

Examples: repository configuration, policy file, workflow definition, authenticated integration metadata, runtime trace, role assignment, explicit approval check.

### PARTIALLY_VERIFIED
Some of the path is evidenced, but at least one material link remains unresolved.

### CLAIMED / DOCUMENTED
Documentation or stakeholder description states the behavior, but direct operational evidence was not available.

### UNKNOWN
The surface could not be resolved within scope. Unknown never means safe, unsafe, allowed, or denied by inference alone.

## 4. Authority dimensions

The audit maps authority across these dimensions:

- **Actor / subject** — human, agent, service, workload, app, bot, CI/CD identity.
- **Identity** — account, workload identity, service account, token principal, app installation, or equivalent.
- **Action** — read, write, mutate, trigger, approve, execute, deploy, administer, authorize, delegate.
- **Resource** — repository, database, service, environment, cloud resource, communication surface, deployment target, secret store, policy surface.
- **Path** — direct or chained route from actor to effect.
- **Gate** — policy, approval, review, branch protection, runtime check, human confirmation, security verdict, or equivalent enforcement point.
- **Evidence** — what proves the request, decision, execution, and resulting effect.
- **Revocation** — how authority is withdrawn and how quickly enforcement learns of that withdrawal.
- **Composition** — whether individually bounded grants combine into greater effective authority.

## 5. Severity / consequence model

Findings are ranked by consequence, not novelty.

### Level 0 — Observational
Read-only or informational capability with no meaningful protected-state effect.

### Level 1 — Mutable low-impact
Can alter bounded non-production or reversible state.

### Level 2 — Operational
Can trigger workflows, modify shared systems, create durable artifacts, or affect team operations.

### Level 3 — High consequence
Can mutate production, deploy, reach sensitive data, change credentials, or cause externally visible effects.

### Level 4 — Authority / control plane
Can change security policy, approval behavior, identity mappings, audit evidence, delegation rules, enforcement controls, or another actor's effective authority.

Severity may be raised by blast radius, irreversibility, sensitivity, uncertainty, weak provenance, composition, or missing revocation.

## 6. Authority Map

The primary artifact represents:

`actor → identity → integration/tool → canonical resource → action → gate → execution path → evidence`

Each edge is marked with evidence state and consequence level where supported.

The map must make visible:

- hidden or indirect paths;
- verified versus assumed access;
- crossings between trust domains;
- approval gates that exist only in documentation;
- paths where human review occurs but is not technically binding;
- unbounded or unclear delegation;
- aggregate authority across multiple integrations;
- paths to production or authority-changing effects;
- evidence discontinuities.

## 7. Required findings categories

The audit actively tests for:

- excessive or undocumented authority;
- unverified integration assumptions;
- human approval that is advisory rather than enforcing;
- self-ratification / same-actor approval paths;
- provider or tool output treated as execution authority;
- mutable policy references without integrity binding;
- stale approval / state mismatch;
- retries that reuse authorization without revalidation;
- weak or absent revocation semantics;
- resource aliasing / scope ambiguity;
- multi-grant authority composition;
- audit success confused with authorization correctness;
- evidence paths that cannot reconstruct who authorized what;
- UI / dashboard representations that understate actual authority.

## 8. Deliverables

### A. Executive authority summary
A short plain-language answer to: what can act, what can it affect, where does human authority hold, and what needs attention first?

### B. Authority Map
Visual and machine/structured representation where practical.

### C. Evidence ledger
Key claims with evidence class and source reference.

### D. Findings register
Each finding includes consequence, evidence, affected path, failure mode, and remediation direction.

### E. Prioritized remediation plan
Ordered by risk reduction and implementation dependency.

### F. Control-plane fit assessment
Maps findings to possible control classes such as:

- policy decision / enforcement;
- explicit approval gate;
- identity hardening;
- resource canonicalization;
- delegation envelope;
- revocation / expiry;
- aggregate-authority ceiling;
- authorization / execution receipt;
- operator/HUD visibility.

## 9. Explicit exclusions

Unless separately contracted, the audit does not include:

- exploit development or active penetration testing;
- social engineering;
- credential harvesting;
- destructive testing;
- production changes;
- legal advice or certification;
- formal SOC 2 / ISO / FedRAMP / EU AI Act certification;
- source-code quality review unrelated to authority or control flow;
- unlimited repository or organization-wide discovery;
- inference about inaccessible provider-internal behavior.

## 10. Safety and access posture

- Prefer read-only access.
- Use least privilege necessary for evidence collection.
- Do not request raw secret values when metadata or configured references are sufficient.
- Do not copy credentials into audit artifacts.
- Flag inaccessible surfaces rather than bypassing them.
- Client retains control over access removal at all times.

## 11. Timing

The standard delivery target is 48 hours after complete intake and access readiness for the agreed bounded environment.

The clock pauses when a blocking access dependency, materially incomplete scope definition, or client-requested hold prevents evidence collection.

## 12. Handoff

The audit ends with a decision point:

- **Accept risk / no further work**;
- **Remediate internally** using the findings;
- **Architecture engagement** for control-boundary design;
- **Implementation engagement** under a new scope.

No remediation or implementation is assumed or automatically authorized by purchase of the audit.
