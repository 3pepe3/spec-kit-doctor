# Spec Kit Doctor

A Spec Kit extension that diagnoses project health and reports issues.

## What it does

Scans your Spec Kit project and checks 6 areas:

- **Project structure** — are `.specify/`, `specs/`, `scripts/`, `templates/`, `memory/` present?
- **AI agent configuration** — which agent is set up, do its commands exist?
- **Feature specifications** — for each feature, are spec.md/plan.md/tasks.md present?
- **Scripts health** — are all bash and PowerShell scripts present and executable?
- **Extensions health** — is extensions.yml valid, is the registry intact?
- **Git status** — are you in a repo, what branch?

Reports findings as errors, warnings, and notes with suggested fixes.

## Installation

```bash
specify extension add doctor
```

Or install from GitHub:

```bash
specify extension add --from https://github.com/KhawarHabibKhan/spec-kit-doctor/archive/refs/tags/v1.0.0.zip
```

## Usage

```
/speckit.doctor.check
```

Or using the alias:

```
/speckit.doctor
```

## Requirements

- Spec Kit >= 0.1.0

## Maintained native-layout compatibility

The 3pepe3 fork v1.0.1 verifies the Bash entrypoint against Spec Kit1.2.1
and Codex skills mode. It reads native integration state, `.specify/feature.json`
and environment feature selection, the `.registry` extension registry, and
only numbered feature directories. Shared contracts are not features.
Fenced example checkboxes are excluded. Bash requires Python3 and emits JSON;
`--json` is accepted for compatibility. It is read-only and reports errors with
a nonzero exit. Original PowerShell scripts remain, but native1.2 compatibility
has not been verified on Windows. Task counts never imply acceptance.
