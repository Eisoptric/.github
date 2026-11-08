<div align="center">

# Saturn

### Tools for secure, accountable AI

[Website](https://saturn-core.com) · [Saturn MCP](https://saturn-core.com/mcp) · [Saturn App](https://saturn-core.com/app) · [Whitepaper](https://saturn-core.com/trust) · [Sponsor](https://github.com/sponsors/Saturn-Technology-Project)

</div>

---

An AI system is safe to rely on only when you can say **what it is allowed to do**, and **what it actually does**.

Saturn works on both sides of that problem with two free products:

| | For | What it does |
| --- | --- | --- |
| **[Saturn MCP](https://saturn-core.com/mcp)** | Teams running AI agents | An MCP gateway that puts every tool call under policy, human approval, and audit. |
| **[Saturn App](https://github.com/Saturn-Technology-Project/Saturn-App)** | People studying models | An open-source desktop workbench for AI research: run experiments, read every sample, look inside the model. |

Both are free, with every feature on every account. Saturn App is open source under the Apache License 2.0.

---

## Saturn MCP

**The MCP gateway that decides what your agents may do.**

Agents talk to Saturn instead of your MCP servers. Saturn exposes only the tools you choose, checks every call against policy down to its arguments, pauses sensitive calls for a person, and records every decision. No SDK and no agent code changes: it works at the protocol level.

```text
policy    Payments  v3  production

rule      payments.transfer
when      amount > 1000 AND currency == "USD"
decision  approval_required

rule      db.drop_table
when      true
decision  deny
```

- **One endpoint** for every agent and every MCP server, over standard MCP on HTTP
- **Tool sets** per agent, across servers; tools outside the set do not exist for that agent
- **Argument-level policies**, ordered and versioned; every call records the policy and rule that decided it
- **Approvals** by one reviewer or a group quorum, with the full call context
- **Credential vault** sealed with ML-KEM-1024 and AES-256-GCM; agents never see upstream secrets
- **Audit trail** with zero-access encrypted payloads, plus HMAC-signed webhooks
- **OAuth 2.1 with PKCE** for every agent, and role-based access in the console

Works with Claude, ChatGPT, Cursor, Gemini, LM Studio, Saturn App, or any MCP client.

[Get started](https://dashboard.saturn-core.com) · [Learn more](https://saturn-core.com/mcp)

---

## Saturn App

**A workbench for AI research, on your own computer.**

Saturn App is organized around your questions, models, experiments, and findings rather than around chats. Write the code yourself, run experiments locally or on your own SSH host, and decide how much the assistant may do.

- **Experiments** that freeze into versions and only compare runs measured the same way
- **Samples** across every model that saw them, with your label beside the scorer's
- **Inspect**: activations at every layer, activation patching against a random control, and sparse-autoencoder features
- **Assistant modes**: Ask, Approve, Auto, or Agent; verdicts, labels, and merges stay yours
- **Plain-file records** in `.saturn/research`, next to your code, ready to diff and commit
- **Bring your own models**: API keys, your Claude or ChatGPT plan, or offline models through LM Studio

macOS 12+ on Apple silicon. Interface in English and Traditional Chinese. Currently a preview release.

[Download](https://github.com/Saturn-Technology-Project/Saturn-App/releases) · [Source](https://github.com/Saturn-Technology-Project/Saturn-App) · [Learn more](https://saturn-core.com/app)

---

## How we build

- **Free.** Both products cost nothing, with every feature on every account.
- **Open.** Saturn App is open source, and every release carries a checksum and signed build provenance.
- **Verifiable.** The [system whitepaper](https://saturn-core.com/trust) explains how keys, payloads, and credentials are protected, and what Saturn cannot see.
- **Honest about limits.** The gateway processes plaintext in flight. The App's modes are a workflow constraint, not a security boundary.

---

## Support Saturn

Saturn is built in the open and paid for by the people who use it. If Saturn helps you, [sponsoring it on GitHub](https://github.com/sponsors/Saturn-Technology-Project), monthly or one-time, keeps both products free.

Contributions are welcome too: star the repository, open an issue, or send a pull request to [Saturn App](https://github.com/Saturn-Technology-Project/Saturn-App).

---

<div align="center">

**AI you can control, and understand.**

© 2026 Saturn Technology Project by Rick Weng

</div>
