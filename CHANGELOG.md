# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-11-07

### Added

- Per-process dedicated and shared VRAM listing from the Windows GPU Process Memory performance counters
- Whole-card VRAM usage bar through `nvidia-smi`, with automatic fallback
- Dark rounded card interface with real large application icons and colored usage bars
- One-click and double-click process termination with a unified confirmation dialog
- Red consequence warnings before ending system components such as DWM, CSRSS and WINLOGON
- Scrollbar-free mouse-wheel browsing with double-buffered cards
- Animated three-dot loading window and smooth fade-in on startup
- Headless agent interface: read-only listing, dry run, authorized release, VRAM requirement gate, JSON result file and exit codes
- Custom application icon and embedded version metadata
- Single-file source in Chinese with no comments, plus a single-file executable

### Security

- System components, explorer and agent hosts (Qoder, pwsh, node) are protected from termination
- Headless termination always requires an explicit target list and the `-已授权` flag
- No network access, no telemetry, no registry writes, no background service

### License

- Released under the PolyForm Noncommercial License 1.0.0. Commercial use requires a separate license.
