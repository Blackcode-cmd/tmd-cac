# TMD-CAC status and verification

**Evidence date: October 28, 2026.** This document distinguishes the saved private ChatGPT plugin, tested local Prompt Lab, automated local preparation, and behaviors that remain unverified.

## Verified component versions

| Area | Current checked state |
|---|---|
| Account plugin | TMD-CAC **v0.6.0**, still a **private** ChatGPT user plugin |
| Offline companion | Local **Prompt Lab v0.6.2**, with project preset and the third written Kai policy |
| Local version control | Private local Git repository with a feature branch; no remote configured |
| Public GitHub repository | Documentation-only overview, not a mirror of private source code |

## Implemented local capabilities

- Single-job form with objective, scope, deliverables, requirements and acceptance checks.
- TMD-CAC project preset with builder label, operating roles, written project boundaries and a distinct Kai/tool-efficiency **proposal**, not live Grok permissions.
- Up to 20 jobs through text/Markdown files, supported JSON job arrays, or a pasted prompt; 1 MiB per selected file and 5 MiB total input limits.
- Selected-file list with per-file Remove, Remove all without wiping the pasted job, and Clear batch. Original files are not deleted.
- Local redaction of common credential patterns, suspicious instruction flags, revision-sensitive drafts and distinct ChatGPT/Kai handoff packet formats.
- **New local manifest preflight:** verifies source-file identity, byte/word counts, checksums, UTF-8, file count/limits and the existing heuristic scanner.
- **New local offline composer:** takes a passing manifest, loads the actual TMD-CAC preset, and produces individual revision-bound **DRAFT** contracts, a builder packet, and a concise review index. Runs are deterministic and fail closed if an existing artifact has been altered.
- Both tools operate locally and do not connect to ChatGPT, send data to Kai, or execute imported jobs.

## Verification evidence

| Gate | Observed result | Scope |
|---|---|---|
| Previous v0.6.2 core regression checks | 40/40 passed | Local batch parsing and output behavior |
| Previous v0.6.2 browser desktop-size checks | 46/46 passed | Local UI harness |
| Previous v0.6.2 browser mobile-size checks | 46/46 passed | Local UI harness at small viewport |
| Current preflight on selected TMD-CAC jobs | 14/14 passed; zero findings | Exact selected source files, heuristic scan |
| Preflight negative/positive regression assertions | 6 passed | Manifest tampering, project and file boundaries |
| Composer regression assertions | 11 passed | Revision consistency, DRAFT states, reuse/tamper handling |
| Automated draft generation | 14/14 draft contracts produced | Local deterministic drafting only |

The recorded browser checks are not a manual accessibility assessment. Local tests and static detection cannot establish prompt quality, privacy guarantees or host-model behavior.

## Outstanding verification and restrictions

- Full native ChatGPT T01–T22 model behavior and fair baseline quality comparisons are **not complete**.
- This automation is an **offline draft composer**; semantic interpretation/validation requires the ChatGPT TMD-CAC skill in an available host.
- Kai/Grok independent review is optional and remains **NOT SENT** until an actual approved handoff. Direct authenticated connector access is not established.
- The local v0.6.2 companion and automated tools have **not** been released as a new private ChatGPT account plugin.
- A hosted public website, hardened independent executor and autonomous downstream-job execution are **not implemented**.
- The private source repository is separate from public documentation. No private prompt inputs, sources, local paths, secrets or generated packets are mirrored here.

## Recommended next checks

1. Review the generated builder packet in an authorized ChatGPT session and run semantic fidelity tests against a short baseline.
2. Perform manual keyboard and screen-reader usability testing for the offline UI.
3. Decide whether to package the tested local companion into the existing private plugin through a guarded versioned update.
4. Add any genuine model-to-model integration only after supported tools, recipient scope and security gates are verified.

**Default TMD-CAC workflow remains:** compile → audit → present, not automatic execution of an imported job.
