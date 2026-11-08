<div align="center">

# Saturn Technology Project

### Infrastructure for the Agentic Enterprise

The control layer that lets AI agents **run, connect, act, and operate safely in production**.

[Website](https://saturn-core.com) · [Saturn App](https://github.com/Saturn-Technology-Project/Saturn-App) · [Sponsor](https://github.com/sponsors/Saturn-Technology-Project)

</div>

---

AI agents are getting access to real tools, real data, and real accounts. The layer between an agent and those systems is usually an afterthought: long-lived credentials in the prompt, no clear permissions, and no record of what happened.

Saturn is that missing layer. We don't build another agent. We build what agents need to work inside real organizations: **runtime, identity, permissions, policy, approval, and audit**.

> The agent decides **what it wants to do**.
> Saturn decides **who is acting, what is allowed, whether a human must approve, and how the action is executed and recorded**.

---

## What We Build

| Component | What it does | Status |
| --- | --- | --- |
| **Saturn App** | Local app to create agents, connect models and MCP servers, configure RAG, and run agents on your machine. | Available |
| **Saturn MCP** | One MCP endpoint for agents. Routes requests to mapped, authorized tools instead of direct connections to every server. | In development |
| **Policy Engine** | Defines what an agent can access and execute, under which conditions, and when a human must approve. | In development |
| **Agent Identity & Access** | Identities, scoped credentials, and authorization for agents acting for a human or on their own. | In development |
| **Audit & Observability** | Traces every tool call, policy decision, approval, and result. | In development |
| **Agent Runtime** | Portable execution environment: state, secrets, tool execution, approvals. Runs locally, in containers, or on Kubernetes. | In development |
| **MCP Marketplace** | Discover MCP capabilities and connect them to Saturn without manual configuration. | Planned |
| **Connectors SDK** | Expose internal APIs, databases, and services to agents through Saturn MCP. | Planned |
| **Saturn Cloud** | Managed runtime, team management, policies, and audit at scale. | Planned |
| **Agent Wallet** | Lets agents make payments under spending limits, allowlists, and approval rules, without holding private keys. | Exploring |

---

## Architecture

```text
                    +-------------------+
                    |     AI Agents     |
                    +---------+---------+
                              | MCP
                    +---------v---------+
                    |    Saturn MCP     |
                    +---------+---------+
                              |
          +-------------------+-------------------+
          |                   |                   |
   +------v------+     +------v------+     +------v------+
   |  Identity   |     |   Policy    |     |    Audit    |
   |  & Access   |     |   Engine    |     | & Telemetry |
   +------+------+     +------+------+     +------+------+
          +-------------------+-------------------+
                              |
                    +---------v---------+
                    | Capability Mapping|
                    | tools · resources |
                    +---------+---------+
                              |
                    +---------v---------+
                    |   Agent Runtime   |
                    | execution·secrets |
                    | approval · state  |
                    +---------+---------+
                              |
          +-------------------+-------------------+
          |                   |                   |
   +------v------+     +------v------+     +------v------+
   | MCP Servers |     | Enterprise  |     | APIs and    |
   |             |     | Systems     |     | Services    |
   +-------------+     +-------------+     +-------------+
```

### Two authority models

- **Human-centric agents** act on behalf of a person, using delegated authority and that person's permissions.
- **Agent-centric agents** have their own identity, credentials, limits, and audit trail.

This lets Saturn serve both personal assistants and autonomous enterprise agents.

---

## Policy, in practice

Policies apply at every level: organization → user → agent → MCP server → tool → resource → parameters.

```text
Coding Agent · GitHub
  repo.read       ALLOW
  repo.search     ALLOW
  issue.create    ALLOW
  workflow.run    REQUIRE APPROVAL
  repo.delete     DENY
```

Decisions can depend on identity, environment, time, risk, and usage limits. The default is least privilege.

Every action that passes through Saturn produces an audit event: who initiated it, which tool and resource, the policy decision, any approval, the result, latency, and cost. Payload logging is configurable separately for privacy and data-residency requirements.

---

## Design Principles

1. **Agents don't hold privileged credentials.** Secrets stay out of the model context.
2. **Every action is governed** by identity, policy, context, and approval.
3. **Capabilities are composable** through standard interfaces, not one-off integrations.
4. **The runtime is portable.** Run it locally, on your own infrastructure, or on Saturn Cloud.
5. **Execution is observable**, with traceable records and deterministic authorization.
6. **Humans stay in control** of high-impact actions.

---

## Research

Saturn is growing into an independent AI lab. Alongside the infrastructure, we work on:

- **Interpretability**: activation-steering experiments on small open models
- **Papers**: publishing what we learn, including negative results
- **Models**: training our own models and releasing the weights

---

## Open Source

Core infrastructure, including the runtime, is developed in the open so it can be inspected and deployed without Saturn Cloud. Commercial offerings focus on managed infrastructure, centralized governance, and enterprise security.

## Support Saturn

Saturn is independent and self-funded. If this work matters to you, [sponsoring us on GitHub](https://github.com/sponsors/Saturn-Technology-Project) directly funds compute for research, infrastructure costs, and time spent maintaining the open-source projects.

---

<div align="center">

**AI agents are becoming a new class of software worker.<br>Saturn builds the infrastructure they need to operate safely.**

[saturn-core.com](https://saturn-core.com)

</div>
