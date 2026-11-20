<div align="center">

<img src="https://saturn-core.com/favicon.png" alt="Eisoptric" width="96" height="96" />

# Eisoptric

**An independent AI research project on how models learn, and what they compute.**

[saturn-core.com](https://saturn-core.com) · [Research](https://saturn-core.com/research) · [Lilith](https://saturn-core.com/lilith) · [About](https://saturn-core.com/about) · [中文](https://saturn-core.com/zh)

</div>

> *Γνῶθι σεαυτόν.*
> Know thyself. Inscribed in the forecourt of the temple of Apollo at Delphi.

The name comes from the Greek *eisoptron*, a mirror: *eis*, into, and *opt-*, to see. A trained model knows something nobody wrote down, and acts on it. Eisoptric's work is to look into it: how it forms during training, what the network computes with it, and how to keep what the model does within rules people set.

Eisoptric was founded by Rick Weng in Taiwan, who is for now its only researcher. It is not part of a company or university.

## What we study

| | Area | Question |
| --- | --- | --- |
| § 1 | **Pretraining dynamics** | When does a capability appear during training, and what changes inside the network when it does? |
| § 2 | **Interpretability** | Which features and circuits carry a behaviour, and do they survive a causal test against a random control? |
| § 3 | **Agent oversight** | How can a model that acts through tools be kept inside rules people set, with a record of what it did? |

Research notes are in progress and will be published at [saturn-core.com/research](https://saturn-core.com/research), each with its code and data.

## Lilith

Small language models we train from scratch, to be released with every checkpoint, the exact data order and the training code, so that how a model learns can be studied rather than guessed. The Lilim are their smaller siblings, varying one thing at a time.

**Status:** in preparation. No model has been released yet. [About Lilith →](https://saturn-core.com/lilith)

## Tools from our work

| Tool | What it is | |
| --- | --- | --- |
| [**Eisoptric App**](https://github.com/Saturn-Technology-Project/Saturn-App) | The open-source workbench we use for experiments and interpretability: questions, code, every sample and the model's insides, kept together. Apache 2.0. | [Releases](https://github.com/Saturn-Technology-Project/Saturn-App/releases) · [Page](https://saturn-core.com/app) |
| **Eisoptric MCP** | The gateway we needed before letting agents act on their own: every tool call under policy, approval and audit. Free. | [Page](https://saturn-core.com/mcp) · [Console](https://dashboard.saturn-core.com) |

## Contact

General and collaboration: hello@saturn-core.com · Security: security@saturn-core.com
