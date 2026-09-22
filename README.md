# project-management-core-tap

Vendor-neutral project-management vocabulary substrate (milestones, tasks and the work that connects them). v0 is deliberately empty: the vocabulary is added as a real project needs it.

## Read first

`specs/spec-project_management_core-v0.md` — this is a thin v0 that puts the piece on the board; the full spec interview runs when the plugin grows.

## Stand it up

From a TAP core checkout:

```bash
scripts/spawn-session.sh <label> cli --from 'git+https://github.com/unified-systems-com/project-management-core-tap@<rev>#ci' --dev-plugins project_management_core
```
