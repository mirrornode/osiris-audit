# Agent Authority Audit

## Know exactly what your AI agents can do — and prove it.

AI agents increasingly touch source control, APIs, databases, deployment systems, messaging, internal tools, and cloud infrastructure. The problem is not merely whether the agent works. The problem is whether anyone can clearly answer:

- What can it actually do?
- Which identity performs the action?
- What resources can it reach directly or indirectly?
- Where is human approval technically enforced?
- Can authority be revoked?
- Can the action be reconstructed afterward?

The **Agent Authority Audit** is a 48-hour bounded technical assessment of one agent-enabled environment.

### What you receive

**Authority Map**  
A visual topology of actors, identities, tools, resources, permissions, approval gates, execution paths, and evidence paths.

**Verified vs. Assumed View**  
A clear separation between controls we can directly evidence and controls that exist only as documentation, expectation, or unresolved platform behavior.

**Authority Findings**  
Specific hidden authority, weak approval boundaries, excessive reach, unsafe composition, revocation gaps, stale-state risks, and missing audit evidence.

**Prioritized Remediation Plan**  
The smallest sequence of changes that materially reduces risk and makes authority explicit.

### First supported profile

GitHub-centered agentic environments connected to operational tools: MCP, APIs, CI/CD, databases, cloud/deployment systems, messaging, and other automation surfaces.

The audit is provider-neutral. Claude, OpenAI, Gemini, Copilot, or a custom runtime may sit inside the environment; the assessment focuses on the authority topology around them.

### What makes this different

This is not a policy-writing exercise and not a generic observability dashboard.

The audit asks whether the intended boundary is **actually enforced**.

A human approval button is not counted as a control unless the execution path is structurally unable to proceed without the valid approval. A documented “read-only agent” is not counted as read-only until the effective access path supports that claim.

### Evidence posture

Every material claim is labeled:

**VERIFIED / PARTIALLY VERIFIED / CLAIMED / UNKNOWN**

Unknowns stay unknown. Missing evidence is never converted into an assumption of safety.

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
