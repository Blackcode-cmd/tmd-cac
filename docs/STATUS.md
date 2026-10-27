# TMD-CAC status and verification

**Evidence date: October 27, 2026.** This document distinguishes the saved account plugin, the tested local companion, and unverified behaviors.

## Current verified versions

| Area | Checked state |
|---|---|
| Account plugin | TMD-CAC v0.6.0, saved as a **private** ChatGPT account plugin |
| Companion webpage | Local offline **Prompt Lab v0.6.1** on the authorized development laptop |
| Public GitHub repository | Documentation-only public overview; not a mirror of private source code |

The offline companion is a self-contained HTML page launched from a desktop shortcut. It prepares draft prompt contracts locally; it does not perform LLM inference, external source retrieval, third-party communication, or downstream task execution.

## Implemented companion behavior

- Single-job form with objective, scope, requirements, deliverables and acceptance checks.
- One-project batch handoff desk: up to 20 jobs, `.txt`, `.md` and constrained `.json` inputs; per-file limit 1 MiB, total selected files 5 MiB, prompt text limit 100,000 characters.
- Shared builder label, written working perspectives and permission boundaries; the label does not choose a model in ChatGPT.
- Local redaction of recognized credential patterns, suspicious-instruction flags, separate sanitized per-job drafts and optional human-mediated review packets.
- Review invalidation after changed inputs; stable content-derived revision identifiers for sanitized batch drafts.
- Local v0.6.1 selection UX: remove one file, remove all files without wiping the pasted job, and add selections incrementally. No original file is deleted.
- Desktop and mobile-size responsive layout tests.

## Test evidence

| Gate | Observed result | What it means |
|---|---|---|
| Batch core regression tests | **36/36 passed** | Local parsing, source bounds, redaction patterns and output invariants |
| v0.6.1 browser suite, desktop viewport | **35/35 passed** | Includes selected-file removal and existing batch-flow checks |
| v0.6.1 browser suite, mobile-size viewport | **35/35 passed** | Same automated checks at a small viewport |

Browser checks are performed in an automated local browser, not equivalent to manual use on all systems. Secret detection is heuristic; a clean scan is not proof of privacy.

## Not yet established

- Full native ChatGPT behavioral testing of all T01–T22 scenarios.
- Measured model quality advantage over a plain, equivalent baseline.
- A direct authenticated integration with external reviewing models.
- A public hosted TMD-CAC website.
- A hardened standalone execution-permission service.
- Host activation of the v0.6.1 local companion as a new account plugin release.

Do not infer these capabilities from a ZIP archive, prompt, saved private plugin, local UI or passing static tests. Verified status should be revised when independent evidence becomes available.

## Next small milestones

1. Run equivalent baseline-versus-compiled task evaluations with actual ChatGPT skill use.
2. Audit usability and accessibility with real operator feedback.
3. Reconcile local v0.6.1 companion changes into the private plugin only through its own tested versioned update process.
4. Consider additional integration infrastructure only for proven needs, with separate approvals.
