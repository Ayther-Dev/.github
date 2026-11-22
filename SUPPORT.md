# Support

This document describes how to get community support across the public open-source repositories of the [Ayther-Dev](https://github.com/Ayther-Dev) organization.

Individual repositories may provide their own `SUPPORT.md` or troubleshooting guides with component-specific instructions. Where present, check the repository's documentation first.

## Community Support Scope

AYTHER's public components are under active **pre-release** development (release candidates, betas, developer previews, and MVPs in progress). Features, command-line options, APIs, and formats may be incomplete or subject to change before stable releases.

- Community support is provided on a **best-effort** basis by maintainers and contributors.
- Community channels do **not** provide guaranteed response times, production SLAs, or dedicated engineering support.
- Questions regarding separate commercial products, services, or licensing are handled outside public community support (see [Commercial Inquiries](#commercial-inquiries)).

## Where to Get Help

Please direct your question or issue to the repository that best matches the component you are using:

| Component | Repository | Use For |
| --- | --- | --- |
| **Ecosystem overview** | [AYTHER](https://github.com/Ayther-Dev/AYTHER) | High-level ecosystem questions and general orientation |
| **AYTHER Engine** | [AYTHER-Engine](https://github.com/Ayther-Dev/AYTHER-Engine) | Core Rust/C++ engine, asset identification, HD composition, Vulkan rendering, audio, Lua scripting, and `.ay` pack handling |
| **AYTHER Runtime** | [AYTHER-Runtime](https://github.com/Ayther-Dev/AYTHER-Runtime) | Game-session execution, CLI flags, Runtime–Play protocol, input maps, Vulkan presentation, and pause overlay |
| **AYTHER SDK** | [AYTHER-SDK](https://github.com/Ayther-Dev/AYTHER-SDK) | Public contracts, schemas, pack tooling, integration workflows, and SDK documentation |
| **AYTHER Play CE** | [AYTHER-Play-CE](https://github.com/Ayther-Dev/AYTHER-Play-CE) | Community Edition launcher, local library scanning, cover art, local pack installation, saves, and Runtime launch issues |
| **AYTHER Tessera** | [AYTHER-Tessera](https://github.com/Ayther-Dev/AYTHER-Tessera) | Deterministic emulation core, native C ABI, replay, and hardware observability |

### Choosing the Right Channel

- **Reproducible bugs & scoped feature requests:** Open a **GitHub Issue** in the affected repository after checking its documentation and searching existing issues to avoid duplicates.
- **General questions, ideas, and usage help:** Use **GitHub Discussions** when enabled on the organization or target repository. Where Discussions is not enabled, consult the repository's `README.md` and `docs/` first, or open a clearly scoped question in the relevant repository.

## Before Asking for Help

Before opening an issue or support thread:

1. Read the target repository's `README.md` and relevant documentation in `docs/`.
2. Verify that you are testing a recent commit or pre-release build and that your build/runtime dependencies match the documented lockfiles and environment requirements.
3. Search open and closed issues to see if the question or defect has already been addressed.

### Information to Include

When reporting a technical problem, include:

- The repository name and exact version, release tag, or commit hash.
- Operating system, architecture, GPU/driver (for rendering issues), and toolchain versions (for build issues).
- Exact commands or minimal steps to reproduce the issue (with personal paths or sensitive details redacted).
- Relevant logs, diagnostics, or error output.
- Expected behavior versus observed behavior.

### What Not to Upload

Never attach or link to:

- Commercial game ROMs, BIOS images, or decryption keys.
- Unauthorized copyrighted game assets, screenshots, or audio.
- Third-party emulator core binaries or commercial `.ay` packs.
- Private signing keys, credentials, tokens, or personal data.

Use minimal synthetic fixtures, homebrew, or original assets whenever a reproduction artifact is needed.

## Security Issues & Community Standards

- **Security vulnerabilities:** Never use public issues or support threads to report suspected vulnerabilities or exposed secrets. Follow the institutional [Security Policy](https://github.com/Ayther-Dev/.github/blob/main/SECURITY.md).
- **Code of Conduct:** All support interactions are governed by the institutional [Code of Conduct](https://github.com/Ayther-Dev/.github/blob/main/CODE_OF_CONDUCT.md).

## Commercial Inquiries

Separate commercial AYTHER products and services—including commercial AYTHER Play, AYTHER Lab, AYTHER Hub, and AYTHER Enterprise—as well as commercial partnerships, custom integrations, or dedicated support inquiries, are managed separately from open-source community support.

For commercial or institutional inquiries, visit [ayther.dev](https://ayther.dev) or contact `ayther-dev@outlook.com`.
