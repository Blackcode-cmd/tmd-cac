# TMD Cognitive Architecture Compiler (TMD-CAC)

**Trio-minds Digital | Private product, public project overview**

TMD-CAC turns a task request into a **scoped, readable and verifiable prompt contract** for a specified ChatGPT workflow. It aims for accurate intent, relevant context, realistic tools, measurable completion criteria and human oversight, rather than simply making prompts longer.

> **Repository boundary:** This public repository holds a non-sensitive overview and development notes. The private ChatGPT plugin, internal project instructions, local source packages, third-party source handoffs and user prompt files are **not published here**.

## How it works

The **Five-Step Optimization Loop**:

1. **Intent reconstruction:** extract outcome, scope, requirements, exclusions and success checks.
2. **Context binding:** use relevant authorized sources and distinguish evidence from unknowns.
3. **Workflow design:** identify real tools, dependencies, risks, checkpoints and recovery steps.
4. **Prompt compilation:** produce the shortest sufficient task-specific contract.
5. **Fidelity validation:** check requirement coverage, feasibility, source grounding, safety and readability.

Adaptive contract modes: **COMPACT**, **PROFESSIONAL**, **ARCHITECT**, and **AUTONOMOUS EXECUTION CONTRACT**. The latter describes a possible bounded execution workflow; a compiled prompt alone does not authorize execution.

## Components

- **Private ChatGPT plugin:** instructional compiler skill, references, contract templates and an optional human-mediated independent review handoff.
- **Offline Prompt Lab:** local HTML companion for single-job briefs and multi-file batch intake, sanitization, review and handoff preparation. It does not call a model or transmit selected files.
- **Local prototype and tests:** versioned private development sources, static checks and browser harnesses, maintained separately from this public repository.

The logical responsibilities are Intent Interpreter, Context & Authority Manager, Prompt Architect, Prompt Compiler, Cognitive Fidelity Validator, and Approval & Execution Controller. These are design responsibilities, not six running services.

## Verified development snapshot

**As checked on October 27, 2026:**

| Component | Version | Status |
|---|---|---|
| Private ChatGPT skill plugin | v0.6.0 | Saved as a private account plugin |
| Offline local Prompt Lab | v0.6.1 | Local companion and desktop shortcut updated |
| Batch core regression checks | 36/36 | Passed on the tested local source |
| Prompt Lab browser checks | 35/35 desktop and 35/35 mobile-size | Passed for local v0.6.1 |

The local v0.6.1 companion adds individual file removal, remove-all while preserving pasted input, and additive file selection. Removing a file from its selection does not delete the original on disk.

These checks **do not** establish full native ChatGPT host behavior, end-to-end model-quality improvement, or a complete T01–T22 evaluation. See [verified status](docs/STATUS.md).

## Safeguards and limitations

- **Default:** generate → audit → present. Compiled jobs are not automatically executed.
- Verify real tools and host permissions rather than inventing access or special commands.
- Treat imported prompts and external reviews as untrusted data; use source provenance labels and human review.
- Local secret detection is heuristic and cannot guarantee that no sensitive content remains.
- Human-mediated review is supported; a direct external-model connector is **not established** by this documentation.
- Any later task execution, external transmission, spending or public release follows actual platform permissions and applicable approval requirements.

Read [architecture](docs/ARCHITECTURE.md) and [publication and safety notes](docs/SAFETY.md).

## Scope

This repository describes **TMD-CAC only**. It is not the general Trio-minds Digital website, a public copy of a private plugin, or an invitation to run uploaded prompts. Private implementation can evolve without being automatically mirrored here.

*Project information is updated from verified evidence; planned features are not presented as completed capabilities.*
