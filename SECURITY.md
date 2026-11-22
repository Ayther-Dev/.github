# Security Policy

This document defines the **organization-wide security policy** for public repositories under the [Ayther-Dev](https://github.com/Ayther-Dev) GitHub organization.

Individual repositories may maintain their own `SECURITY.md` with component-specific threat models, CI security gates, and rollback procedures (for example, `AYTHER-Engine`, `AYTHER-Runtime`, and `AYTHER-Play-CE`). Where a repository defines its own `SECURITY.md`, that policy supplements this institutional baseline.

## Supported Versions

All public AYTHER repositories are currently in **pre-release** development. No long-term support (LTS) or production security-support commitment is offered prior to stable releases.

| Repository | Current Stage | Security Evaluation Target |
| --- | --- | --- |
| [AYTHER Engine](https://github.com/Ayther-Dev/AYTHER-Engine) | Release candidates (`0.1.0-rc.*`) | `main` (fixes ship in the next candidate) |
| [AYTHER Runtime](https://github.com/Ayther-Dev/AYTHER-Runtime) | Beta (`0.1.0-beta.*`) | `main` (fixes ship in the next beta) |
| [AYTHER SDK](https://github.com/Ayther-Dev/AYTHER-SDK) | Experimental / Developer Preview | `main` |
| [AYTHER Play CE](https://github.com/Ayther-Dev/AYTHER-Play-CE) | Active pre-release | `main` |
| [AYTHER Tessera](https://github.com/Ayther-Dev/AYTHER-Tessera) | MVP in development | `main` |

Earlier pre-release tags and snapshots are generally not backported. Supported version matrices will be published per repository once stable releases are established.

## Reporting a Vulnerability

**Do not disclose suspected security vulnerabilities or exposed secrets in public GitHub issues, pull requests, discussions, or social media.**

### Preferred Channel — GitHub Private Vulnerability Reporting

When reporting a vulnerability in a specific public repository, prefer GitHub's **Private Vulnerability Reporting** feature on that repository:

1. Open the affected repository under [Ayther-Dev](https://github.com/Ayther-Dev).
2. Navigate to the **Security** tab.
3. Select **Report a vulnerability**.

### Private Fallback & Multi-Repository Reports

If Private Vulnerability Reporting is not enabled on the affected repository, or if a report spans multiple AYTHER repositories, send a confidential report to:

- **Email:** `ayther-dev@outlook.com`

If you have discovered an exposed secret or credential, rotate or revoke it first if it belongs to you, and report the exposure privately without posting secret material publicly.

### What to Include

To help maintainers reproduce and assess the report quickly, please include:

- The affected repository, version, tag, or commit hash.
- Target operating system, architecture, and build/toolchain details (when relevant).
- A clear description of the vulnerability and its potential security impact.
- Minimal reproduction steps or a proof of concept free of personal data, secrets, and copyrighted game content.
- Known workarounds or suggested mitigations (if any).
- Whether you are available to validate a proposed fix.

## Priority Scope

Across the public AYTHER ecosystem, reports are especially valuable in the following areas:

- **`.ay` pack parsing, validation, and trust:** Signature verification bypasses, acceptance of untrusted/expired/development keys under production policies, path traversal, archive-extraction escapes, decompression bombs, and resource-limit bypasses (`AYTHER-Engine`, `AYTHER-SDK`, `AYTHER-Play-CE`).
- **Sandboxed scripting:** Escapes from the Lua sandbox or unauthorized filesystem, process, or network access (`AYTHER-Engine`, `AYTHER-SDK`).
- **Memory safety & native boundaries:** Memory corruption, use-after-free, buffer overflows, and FFI/ABI lifetime or ownership bugs across Rust and C/C++ (`AYTHER-Engine`, `AYTHER-Runtime`, `AYTHER-Tessera`).
- **Core loading & process boundaries:** Unsafe dynamic library loading, command-injection risks, and protocol-boundary issues between launcher, runtime, engine, and emulation providers (`AYTHER-Engine`, `AYTHER-Runtime`, `AYTHER-Play-CE`).
- **Release & supply-chain integrity:** Exposed credentials or signing keys, compromised build workflows, or mismatches between published artifacts, checksums, and provenance metadata.

## Response & Coordinated Disclosure Process

AYTHER is maintained by a small team on a best-effort basis during pre-release development. While fixed response SLAs are not guaranteed, maintainers aim to:

1. **Acknowledge** receipt of valid private reports promptly when possible.
2. **Triage** scope, affected components, and severity.
3. **Develop and verify** a fix or mitigation on private branches/advisories before public disclosure.
4. **Coordinate disclosure** once a fix is available, publishing affected versions, remediation guidance, and a GitHub Security Advisory or changelog entry where appropriate.

Please allow maintainers a reasonable window to investigate and prepare a remediation before publishing details that could enable exploitation.

## Out of Scope

The following items are generally outside the scope of this security policy:

- Commercial game ROMs, BIOS images, third-party emulator cores not distributed by AYTHER, and third-party `.ay` enhancement packs.
- Vulnerabilities in third-party dependencies that are neither pinned nor distributed by the affected AYTHER repository.
- Theoretical or roadmap-only gaps in unimplemented features, or issues requiring deliberate tampering with a local binary after integrity verification.
- Separate commercial AYTHER products and operated services (such as commercial AYTHER Play, AYTHER Lab, AYTHER Hub, and AYTHER Enterprise), which are governed by their own policies.

## Safe Testing

Test only systems, environments, and data that you own or have explicit permission to evaluate. Do not access other users' data, disrupt project infrastructure, or include copyrighted ROMs, game assets, personal data, or destructive payloads in reports.
