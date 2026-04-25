# Repository Agent Instructions

Scope: entire repository.

This repository follows the shared OpenAutonomyX instruction layer in `openautonomyx/common-instructions` and is scoped to AgentNxt knowledge base documentation and reusable knowledge assets.

## Documentation-only alignment rule

For documentation alignment tasks, update README files, docs, examples, knowledge entries, and repo-level guidance only. Do not change application code unless a human maintainer explicitly requests implementation work.

## Shared references

Use these shared references as the default baseline:

- `standards/engineering-execution-standard.md`
- `policies/context-and-guardrails-policy.md`
- `policies/test-and-process-improvement-policy.md`
- `policies/airgapped-operation-policy.md`

Do not duplicate shared policies here. Reference them and add only knowledge-base-specific guidance.

## In scope

- Knowledge base documentation
- Source-of-truth notes for AgentNxt operations
- Curated references and examples
- Review notes for substantial knowledge changes
- Documentation for retrieval, indexing, and governance behavior

## Out of scope

- Organization-level vision or strategy source documents
- Generic shared prompt packs
- Application code owned by product repositories
- Large private datasets or binary model artifacts unless explicitly approved

## Documentation rules

1. Keep knowledge entries concise, sourced, and reviewable.
2. Separate current state, recommended next state, and future state when documenting evolving systems.
3. Document source, owner, freshness, and known limitations when possible.
4. Avoid copying shared policies or long source documents from sibling repos.
5. Record substantial restructuring or knowledge resets in `reviews/` when applicable.
6. Require reviewer approval and HITL sign-off for production-facing knowledge changes.
