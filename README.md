# ProjectGovernanceOS

ProjectGovernanceOS (PGOS) is a lightweight governance protocol for
LLM-assisted projects.

PGOS intentionally has one normative system file: [`PGOS.md`](PGOS.md).
It defines the operating protocol for the Customer, Strategist, Tech
Lead, Executor, Reviewer, Auditor, and Council without requiring a
custom runtime, workflow engine, schema system, daemon, or governance
directory.

## Status

**Version:** `v1.0.0-rc2`\
**Stage:** real-project pilot candidate

This release candidate passed the final design/patch review and is
intended for validation on real projects before a stable `v1.0.0`
release.

## Start a new project

1.  Give `PGOS.md` to a fresh capable LLM session.
2.  Tell it that you are starting a new project.
3.  Describe the project naturally.
4.  Continue primarily through the Strategist. PGOS will route technical
    planning, execution, independent review, Council, and audit only
    when useful.

The Customer should make goals, preferences, risk, and acceptance
decisions; the Customer should not become the routine shell operator or
message bus between internal roles.

## Continue an existing project

1.  Give `PGOS.md` to a fresh capable LLM session.
2.  Tell it that you are continuing an existing project.
3.  Follow the bounded read-only reconnaissance flow defined in
    `PGOS.md`.
4.  Let the Strategist reconstruct current state from repository
    evidence and durable project documentation before authorizing new
    mutation work.

Old chat history is not intended to be a dependency.

## Project copies

A project may keep its own copy of `PGOS.md` so that the governance
rules used by that project are explicit and versioned with the project.

Updating PGOS is a governed hot-swap: historical facts and accepted
project decisions remain evidence; the adopted PGOS version governs
future actions.

## Design principles

-   Customer attention is scarce.
-   Governance should facilitate development, not become the project.
-   One mutation writer at a time.
-   Mutation work is independently reviewed.
-   Durable project memory belongs to the project, not to chat history
    or transport files.
-   Git records project history; it is not a governance engine.
-   PGOS is a governance protocol, not a technical security sandbox.
-   Add machinery only after a concrete need is demonstrated.

## Repository contents

``` text
ProjectGovernanceOS/
├── PGOS.md
├── README.md
└── LICENSE
```

`PGOS.md` is the normative PGOS artifact. `README.md` and `LICENSE` are
repository support files, not additional governance rules.

## License

MIT License. See [`LICENSE`](LICENSE).
