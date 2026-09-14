# Decisions

Record consequential scientific, analytical, computational, or organisational decisions.

## 2026-09-14 — Update LQMB template from v0.2.0 to v0.2.1

### Decision

Adopted `lqmb-template` v0.2.1 (commit `6d58cb61b262e8098678844b01ab30b51ae5c861`), replacing the
previously recorded v0.2.0 (commit `d41e607f70a2f4f0f7a417db85a3ae7f6d604c5a`).

### Rationale

Requested by the human user after being informed that a newer template release was available.
A manifest-driven three-way comparison (recorded template commit vs. new template release vs.
current project files) found no local modifications to any template-managed file, so every
changed file could be adopted from upstream without conflict.

### What changed

Adopted from upstream (template-managed, changed upstream, unmodified locally):
`CLAUDE.md`, `AI_PROVENANCE.md`, `TEMPLATE_VERSION`, `.github/pull_request_template.md`,
`.github/workflows/ci.yml`, `.lqmb/manifest.json`, `.lqmb/README.md`,
`.lqmb/bin/template-status.py`, `docs/lqmb/LQMB_LIVING_PROJECT_FRAMEWORK.md`,
`docs/lqmb/TEMPLATE_UPDATE_PROTOCOL.md`.

Added (new upstream file): `docs/lqmb/DEPENDENCY_UPDATE_PROTOCOL.md`.

Unchanged (no upstream change): `CONTRIBUTING.md`, `.gitignore`, all `.github/ISSUE_TEMPLATE/*`,
`docs/lqmb/V0.2_MIGRATION_FROM_V0.1.md`.

Preserved (project-owned, not part of the template): `docs/lqmb/MIGRATION_NOTE_MOCK_PROJECT.md`,
`.lqmb/project.json` (only its `template.version`/`template.commit` fields were updated),
`.lqmb/dependencies.json`. No `protected_paths` (`src/`, `tests/`, `data/`, `docs/research-log.md`,
etc.) were touched.

Notably, `.lqmb/manifest.json` changed schema upstream: `.lqmb/project.json` and
`.lqmb/dependencies.json` are now explicitly classified as `project_configured_paths` rather than
being covered by a wholesale `.lqmb/` entry in `template_managed_paths`.

### Alternatives considered

None — this is a mechanical template sync with no local divergence to reconcile.

### Consequences

`CLAUDE.md` itself changed materially upstream (e.g. Claude may no longer create a commit, push a
branch, or open a pull request without explicit human authorisation; a read-only
`template-status.py --check-upstream` check is now expected at first interaction). Future sessions
will follow the updated instructions.

### Revisit when

Not applicable — routine template sync.

### Decision

### Rationale

### Alternatives considered

### Consequences

### Revisit when

<!-- Optional: state what new evidence would justify revisiting the decision. -->
