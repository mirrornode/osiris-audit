# Agent Authority Audit

## See what your AI agents can do — with an evidence-backed authority map.

AI agents increasingly touch source control, APIs, databases, deployment systems, messaging, internal tools, and cloud infrastructure. The problem is not merely whether the agent works. The problem is whether anyone can clearly answer, for a defined environment and point in time:

- What can it actually do?
- Which identity performs the action?
- What resources can it reach directly or indirectly?
- Where is human approval technically enforced?
- Can authority be revoked?
- Can the action be reconstructed afterward?

The **Agent Authority Audit** is a 48-hour bounded technical assessment of a quantitatively capped agent-enabled environment, beginning after scope freeze and access readiness.

### What you receive

**Authority Map**  
A visual topology of actors, identities, providers/accounts, tools, resources, permissions, approval gates, execution paths, revocation, and evidence paths.

**Verified vs. Assumed View**  
A claim-specific separation between controls supported by sufficient evidence, partially verified controls, documented claims, and unresolved surfaces.

**Authority Findings**  
Specific hidden authority, weak approval boundaries, excessive reach, unsafe composition, revocation gaps, stale-state risks, sensitive-data exposure, and missing audit evidence.

**Prioritized Remediation Plan**  
The smallest sequence of changes that materially reduces risk and makes authority explicit.

### Standard v1 scope

Unless separately quoted, the 48-hour package is capped at up to:

- 3 repositories;
- 2 environments;
- 10 material principals;
- 8 material integrations/tool surfaces;
- 25 material authority paths;
- 40 substantive evidence-source items.

If discovery exceeds the agreed cap, coverage is prioritized/sampled transparently or separately re-scoped. The audit does not silently expand into organization-wide discovery.

### First supported profile

GitHub-centered agentic environments connected to operational tools: MCP, APIs, CI/CD, databases, cloud/deployment systems, messaging, and other automation surfaces.

The audit is provider-neutral. Claude, OpenAI, Gemini, Copilot, or a custom runtime may sit inside the environment; the assessment focuses on the authority topology around them.

### What makes this different

This is not a policy-writing exercise and not a generic observability dashboard.

The audit asks whether the intended boundary is supported by **actual enforcement evidence**.

A human approval button is not called an enforced control unless the observed execution path includes a technical gate that prevents effect without valid approval. A documented “read-only agent” is not called verified read-only unless the evidence threshold for the relevant enforcement point is met.

### Safe validation posture

The standard engagement is passive-by-default: configuration, metadata, policy, logs, traces, and existing records. Live bypass attempts, grant mutation, production effects, or active security testing require a separate written test plan and explicit authorization.

### Evidence posture

Every material claim is labeled:

**VERIFIED / PARTIALLY VERIFIED / CLAIMED / UNKNOWN**

Verification is claim-specific. Static configuration alone does not prove deployed enforcement. Unknowns stay unknown.

### Important limitation

The deliverable is a **point-in-time, evidence-backed map of the agreed observable scope**. It does not guarantee completeness or prove the absence of inaccessible, undisclosed, provider-internal, future, or out-of-scope authority paths.

### What happens after

The audit stands alone. You can remediate internally using the findings.

When useful, follow-on work can separately cover:

- deterministic approval gates;
- policy decision/enforcement boundaries;
- identity and resource normalization;
- bounded delegation and revocation;
- authorization/execution receipts;
- operator control surfaces and HUDs.

No implementation is bundled or assumed.

---

**Agent Authority Audit**  
*Map the authority. Verify the boundary. Control what matters.*
