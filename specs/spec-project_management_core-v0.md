# TAP Project Management Core Plugin Specification

**Vendor-neutral project-management vocabulary substrate (milestones, tasks and the work that connects them). v0 is deliberately empty: the vocabulary is added as a real project needs it.**

## Plugin Identity

| Field | Value |
| --- | --- |
| Slug | `project_management_core` |
| Display name | TAP Project Management Core |
| Description | Vendor-neutral project-management vocabulary substrate (milestones, tasks and the work that connects them). v0 is deliberately empty: the vocabulary is added as a real project needs it. |
| Kind | `*_core` substrate: vendor-neutral project-management vocabulary. Consumes nothing; consumed by instance plugins that track work (highbar first) and by any future vendor plugin that observes a tracker. |

This plugin ships no TAP-managed types in v0, so it declares no default dimensions.

## Philosophy

This is a thin v0 (ruled 2026-09-22 for the highbar starter set): it exists to put the piece on the board so a design can reference it, not to model the domain. The full `create-plugin-spec` interview, prior-art search and requirement buy-in run when this plugin grows past v0; nothing here pre-empts them.

Nothing in v0 is observed or designed by this plugin; it is a container other work is composed into.

**Provenance markers:** none in v0 (no types, no data).

## Goals

| # | Name | Description |
| --- | --- | --- |
| 1 | On The Board | Exist as an installable plugin so the highbar stack can boot with it. |

## Requirements

| RID | Name | Status | Notes |
| --- | --- | --- | --- |
| req-project-management-core-record | [CI Record and Tests](#ci-record-and-tests) | Implemented | The in-package `ci` boot record and the manifest/behaviour tests |
| req-project-management-core-vocabulary | [Work Vocabulary](#work-vocabulary) | Backlog | Milestone, task and dependency types; added when highbar first tracks work on the grid |

---

### CI Record and Tests
----
RID: `req-project-management-core-record`

Status: `Implemented`

The in-package `ci` boot record (`req-boot-bootstrap-ci-record`) and the tests that run in it.

#### Implementation

`tap_plugin/project_management_core/boot/ci.boot.json` installs this plugin alone (it declares no dependencies), offline and credential-free; the consumer flips self to editable. `tap_plugin/project_management_core/tests/test_project_management_core_manifest.py` runs `validate_plugin` at structure and strict levels.

#### Acceptance Criteria

| ACID | Title | Status | Description | Notes |
| --- | --- | :---: | --- | --- |
| req-project-management-core-record-1 | Record Declared | Implemented | The manifest declares the `ci` record with its sha256. | |
| req-project-management-core-record-2 | Validates Strict | Implemented | `validate_plugin --strict` passes on the package. | |

---

### Work Vocabulary
----
RID: `req-project-management-core-vocabulary`

Status: `Backlog`

Milestone, task and dependency types; added when highbar first tracks work on the grid.
