# Security Policy

## Supported versions

| Version | Supported |
|---|---|
| 1.00 | Yes |

## Reporting a vulnerability

Please do not open a public issue for security problems. Send a report to **qq591277494@126.com** with:

- a description of the issue and its impact
- steps to reproduce
- your Windows version and, if relevant, GPU model
- any proof-of-concept material

You will receive an acknowledgement as soon as possible. Confirmed issues will be fixed and disclosed in a new release.

## Scope notes

VRAM Butler is a local Windows utility:

- it makes no network connections and collects no telemetry
- it terminates processes only when the user explicitly requests it, and only for the listed target names
- system components, explorer and agent hosts (Qoder, pwsh, node) are always protected from termination
- headless termination is disabled unless the explicit `-已授权` flag is provided

Reports about social engineering or about intentionally ending system components from the interactive UI are out of scope.
