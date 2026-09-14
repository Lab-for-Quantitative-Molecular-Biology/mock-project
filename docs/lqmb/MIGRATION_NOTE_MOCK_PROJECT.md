# Mock project v0.2 migration note

This mock project was originally created from the LQMB v0.1 template and was used to test Claude Code behaviour.

Version 0.2 migrates the project to the explicit LQMB living-project framework.

The existing workflow-test document and all project-specific content remain project content and are not replaced by the template update.

The `template.commit` field in `.lqmb/project.json` is intentionally `null` in this migration package. After `lqmb-template` v0.2.0 has been merged and tagged, replace it with the exact commit SHA of the canonical v0.2.0 release before committing the mock-project migration.
