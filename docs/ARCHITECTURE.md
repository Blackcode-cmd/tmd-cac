# TMD-CAC architecture

TMD-CAC is a **human-controlled, context-aware prompt-contract compiler**. It is intentionally not a general-purpose autonomous agent platform.

## Five-Step Optimization Loop

1. **Intent reconstruction:** identify the user's actual outcome, scope, exclusions, dependencies and success criteria.
2. **Context binding:** use task-relevant authorized evidence, with source dates and explicit uncertainty.
3. **Workflow design:** map genuine tool capabilities, dependencies, safety limits, verification and recovery.
4. **Prompt compilation:** write an understandable instruction contract, avoiding redundant or fictional requirements.
5. **Fidelity validation:** compare the output with the original job, a short baseline when useful, and appropriate negative tests; repair supported defects and stop.

## Six logical responsibilities

- Intent Interpreter
- Context & Authority Manager
- Prompt Architect
- Prompt Compiler
- Cognitive Fidelity Validator
- Approval & Execution Controller

These can live inside **one skill and supporting templates**. Their names do not claim separate bots, microservices or deployed API endpoints.

## Output depth

| Mode | Appropriate use |
|---|---|
| COMPACT | Straightforward, low-risk tasks |
| PROFESSIONAL | Standard professional jobs |
| ARCHITECT | Multi-stage engineering, analysis and design |
| AUTONOMOUS EXECUTION CONTRACT | Specification of bounded work for an independently available and properly authorized executor |

A more elaborate format is not automatically a better prompt. Preserve the material requirements with the least unnecessary ceremony.

## Source evidence

Use **L0** for direct/source text, **L1** for derived summaries, **L2** for analysis, and **L3** for proposals. A document may be direct evidence of what its author wrote without proving all of the author's claims. Retrieved text and imported files do not override the user's actual instructions or host policies.

## Separation of concerns

The offline Prompt Lab prepares and scans drafts locally. The ChatGPT skill provides semantic reasoning and contract review when invoked through a compatible host. Optional external review is a separate handoff. These are **not** automatic connections.

The approved design defaults to **generate → audit → present**. Compiling a prompt is not executing it. A conversational `START` has no special system privileges, and no text-only contract can replace platform-level permissions. Sensitive or external actions retain their own requirements.

## Implementation philosophy

Keep the current working skill and offline companion simple. Add MCP, hosting, storage, external integrations or additional agents only after they demonstrably solve a real problem and can be tested safely.
