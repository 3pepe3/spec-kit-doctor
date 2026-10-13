# Changelog

## Unreleased

- Diagnose current `.specify/` infrastructure, Codex skills and `.registry` extension metadata while retaining explicit legacy-layout compatibility.
- Share a read-only Python engine between Bash and PowerShell; emit clean JSON with detailed findings and explicit optional YAML-validation limits.
- Validate installed script families rather than requiring both; remove automatic repair suggestions from the diagnostic command workflow.
- Add fixture tests for layouts, malformed configuration, argument handling and unchanged project files; PowerShell parity runs only where its runtime exists.

## 1.0.0 (2026-03-13)

- Initial release
- Project health diagnostic command (`/speckit.doctor.check`)
- Checks: project structure, AI agents, feature specs, scripts, extensions, git
- Bash and PowerShell script parity
