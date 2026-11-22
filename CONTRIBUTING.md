# Contributing to AYTHER

## Welcome

Thank you for your interest in contributing to **AYTHER**.

This document defines the **organization-wide contribution guidelines** for all public repositories under the [Ayther-Dev](https://github.com/Ayther-Dev) organization. It covers shared expectations around workflow, architecture, licensing, legal boundaries, and community standards.

Individual repositories may include their own `CONTRIBUTING.md` and developer guides with language-, toolchain-, build-, and test-specific instructions (for example, Rust, C++, CMake, Vulkan, Slint, or ABI checks). Where a repository provides its own `CONTRIBUTING.md`, follow both its repository-specific technical requirements and the institutional principles below.

## Public Projects

Contributions are welcome across AYTHER's public open-source repositories:

| Repository | Focus |
| --- | --- |
| [AYTHER Engine](https://github.com/Ayther-Dev/AYTHER-Engine) | Real-time audiovisual identification, asset substitution, Vulkan rendering, audio processing, and `.ay` pack handling |
| [AYTHER Runtime](https://github.com/Ayther-Dev/AYTHER-Runtime) | Game-session host, original/HD presentation, input handling, overlay, and emulation-provider integration |
| [AYTHER SDK](https://github.com/Ayther-Dev/AYTHER-SDK) | Public APIs, integration contracts, schemas, `.ay` pack tooling, and open authoring workflows |
| [AYTHER Play CE](https://github.com/Ayther-Dev/AYTHER-Play-CE) | Open-source, offline-first Community Edition launcher for local libraries, packs, and Runtime integration |
| [AYTHER Tessera](https://github.com/Ayther-Dev/AYTHER-Tessera) | Open emulation core focused on deterministic execution, structured observability, and native Engine integration |

The [AYTHER](https://github.com/Ayther-Dev/AYTHER) repository serves as the public overview and entry point for the ecosystem.

## Ways to Contribute

You can contribute to AYTHER in many ways beyond writing code:

- **Bug reports:** Report reproducible issues with clear environment details, minimal steps, and expected vs. observed behavior.
- **Code & fixes:** Implement bug fixes, performance improvements, tests, and scoped features.
- **Documentation:** Improve READMEs, guides, architecture notes, API references, and onboarding instructions.
- **Testing & QA:** Validate supported platforms, add automated tests, and build legally redistributable synthetic test fixtures.
- **Design & proposals:** Discuss technical proposals, contract changes, and interoperability improvements through issues before opening large pull requests.
- **Tooling & integrations:** Build compatible open tooling, schemas, or integrations against AYTHER's public contracts.

## Before You Start

Before beginning work on a change:

1. Check open issues, recent pull requests, and existing specifications/docs in the target repository to avoid duplicating work already underway.
2. Read the target repository's `README.md`, `CONTRIBUTING.md` (if present), and development setup documentation.
3. For non-trivial changes—especially changes affecting public APIs, ABIs, pack formats, protocols, or architecture—open an issue to discuss scope and design before investing heavily in implementation.
4. Keep changes focused. Separate bug fixes or functional additions from unrelated refactoring or formatting sweeps.

## Development Workflow

1. **Fork and branch:** Fork the target repository (or create a branch if you have write access) from an up-to-date `main` branch. Use a short, descriptive branch name (for example, `fix/...`, `feat/...`, or `docs/...`).
2. **Make small, coherent commits:** Each commit should represent a logical unit of work. Most AYTHER repositories follow [Conventional Commits](https://www.conventionalcommits.org/) (`feat:`, `fix:`, `docs:`, `test:`, `chore:`, etc.).
3. **Run local checks:** Format your code, run linters/static analysis, and execute the repository's build and test suite before pushing.
4. **Update documentation and tests:** Keep docs, schemas, ABI bindings, changelogs (when applicable), and tests in sync with code changes in the same pull request.
5. **Open a pull request against `main`:** Clearly explain:
   - What problem the change solves and why.
   - Which components, files, or contracts are affected.
   - How the change was tested (including platforms and commands run).
   - Any known limitations, risks, or follow-up items.

Do not open pull requests containing unfinished `WIP` commits targeting `main` unless explicitly marked as a **Draft** pull request for early feedback.

## Code Quality

All contributions are expected to meet the target repository's quality bar:

- **Formatting & static analysis:** Follow the repository's configured formatters and linters (e.g., `cargo fmt`, `cargo clippy`, `clang-format`, `clang-tidy`).
- **Tests:** Bug fixes should include a regression test that fails without the fix. New behavior and contract changes must include automated tests.
- **Honest test reporting:** Never present skipped tests as passing. If hardware, fixtures, or platform constraints prevented a test from running, state that explicitly in the pull request.
- **CI compliance:** Pull requests must pass all required CI checks before merging.
- **Safe input handling:** Treat external inputs—including `.ay` packs, scripts, patches, ROMs, media assets, and user-supplied cores—as untrusted input. Validate paths, bounds, and resource limits explicitly.
- **No secrets:** Never commit credentials, private signing keys, tokens, or machine-specific paths.

## Architecture & Specifications

AYTHER's architecture depends on strict technical boundaries:

- **Preserve game logic vs. audiovisual presentation separation:** Changes must preserve the strict separation between the original game's logic/execution and its audiovisual presentation layer. AYTHER must remain non-destructive (never modifying original ROMs) and reversible (preserving access to the original presentation).
- **Respect public contracts and specifications:** Public APIs, C/FFI ABIs, `.ay` pack formats, process protocols, and serialization schemas are versioned contracts shared across repositories. Do not introduce silent breaking changes; update the specification, consumers, and contract tests together.
- **Maintain open-core and repository boundaries:** Public repositories must remain self-contained and free of proprietary code, private-service dependencies, or assumptions that commercial sibling repositories exist.
- **No undocumented dependencies:** Do not introduce external dependencies without verifying license compatibility, maintenance posture, and build/distribution impact according to the target repository's dependency policy.

## Legal & Licensing

- **Repository licenses:** Each public AYTHER repository defines its applicable FOSS license in its root `LICENSE` file (currently **Mozilla Public License 2.0 (`MPL-2.0`)** across Engine, Runtime, SDK, Play CE, and Tessera) and scope notes in `NOTICE.md` where present. By submitting a contribution, you represent that you have the right to contribute it under the target repository's license.
- **No ROMs, BIOS, or unauthorized assets:** Never commit, upload, or attach commercial game ROMs, BIOS images, decryption keys, commercial game artwork/audio/screenshots without authorization, or third-party emulator core binaries to any repository, issue, pull request, or test fixture. Use only original, synthetic, public-domain, or explicitly authorized material.
- **Clean provenance:** Record origin and license information for any third-party code, fonts, icons, or assets you propose to introduce. Do not copy or port restricted or non-commercial third-party code into AYTHER repositories.
- **Trademarks:** Contributing code or documentation does not grant rights to AYTHER trademarks, logos, or branding beyond what is necessary to comply with license notices.

## Security

Do **not** report suspected security vulnerabilities, exploitable bugs, or exposed secrets in public issues, pull requests, or discussions.

Follow the target repository's `SECURITY.md` policy and use GitHub's private vulnerability reporting feature where enabled.

## Community Standards

All participation in AYTHER spaces is governed by the institutional [Code of Conduct](https://github.com/Ayther-Dev/.github/blob/main/CODE_OF_CONDUCT.md). By contributing, you agree to uphold those standards.

## Review Process

Maintainers review pull requests based on technical correctness, adherence to architectural and legal boundaries, test coverage, and maintainability.

- **Feedback & iteration:** Reviewers may request changes, additional tests, or smaller, split pull requests. Address review comments directly and keep discussion constructive and focused on the work.
- **Acceptance criteria:** A pull request is ready to merge once it satisfies the repository's specifications and quality gates, passes required CI checks, resolves review feedback, and complies with AYTHER's licensing and legal boundaries.
- **Availability:** AYTHER is under active development with a small maintainer team. Review times may vary depending on complexity and current release priorities.
