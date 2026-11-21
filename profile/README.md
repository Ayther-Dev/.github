# AYTHER

### Classic games. Reimagined.

**Open-source technology for real-time audiovisual remastering of classic games — preserving their original gameplay, logic, and identity.**

[Website](https://ayther.dev) · [GitHub Organization](https://github.com/Ayther-Dev) · [Explore AYTHER](https://github.com/Ayther-Dev/AYTHER)

---

## The Past Isn't Replaced. It's Reimagined.

Classic games are more than their original graphics and sound. Their identity lives in their gameplay, mechanics, timing, and design.

AYTHER makes it possible to reimagine their audiovisual presentation with high-definition graphics, enhanced audio, and modern visual effects while preserving the underlying game experience.

Our approach is:

- **Non-destructive:** Original game files remain unchanged.
- **Reversible:** Switch between original and enhanced presentation.
- **Extensible:** Use independently developed enhancement packs.
- **Open:** Build integrations and author packs using public tools and documented interfaces.
- **Preservation-minded:** Respect original gameplay and intellectual property rights.

## How AYTHER Works

AYTHER observes the audiovisual output of a running game, identifies supported elements, and substitutes compatible assets from separate `.ay` enhancement packs.

The engine handles identification and composition. The runtime manages the game session. The launcher provides the player experience.

Original gameplay remains under the control of the emulation system.

## Open Source Ecosystem

AYTHER is built around five public projects.

### AYTHER Engine

**The audiovisual remastering engine.**

[Explore Engine](https://github.com/Ayther-Dev/AYTHER-Engine)

- Deterministic audiovisual identification.
- Real-time asset substitution and HD composition.
- Vulkan rendering and audio processing.
- `.ay` pack validation, loading, and scripting.
- Integration with supported emulation providers.

**Status:** Active development, signed release candidates available.

### AYTHER Runtime

**The game-session host.**

[Explore Runtime](https://github.com/Ayther-Dev/AYTHER-Runtime)

- Game execution and session management.
- Original/HD presentation switching.
- Input, audio, display, and in-game controls.
- Integration with Engine and supported emulation providers.
- Local configuration and save-state support.

**Status:** Beta, with prerelease builds available.

### AYTHER SDK

**Open tools and contracts for developers and pack creators.**

[Explore SDK](https://github.com/Ayther-Dev/AYTHER-SDK)

- Public APIs and integration contracts.
- `.ay` pack specifications and tooling.
- Asset inspection and validation workflows.
- Signing and verification tools.
- Open authoring workflows independent of proprietary tools.

**Status:** Experimental / Developer Preview.

### AYTHER Play CE

**The open-source Community Edition launcher.**

[Explore Play CE](https://github.com/Ayther-Dev/AYTHER-Play-CE)

- Local game library management.
- Controller-friendly, ten-foot user interface.
- Local enhancement-pack installation.
- Game launching through AYTHER Runtime.
- Local saves and offline-first operation.

**Status:** Active pre-release development.

Play CE is designed to work independently of AYTHER-operated online services. An AYTHER account, subscription, or commercial marketplace is not required for local playback.

### AYTHER Tessera

**An open emulation core focused on determinism and structured observability.**

[Explore Tessera](https://github.com/Ayther-Dev/AYTHER-Tessera)

- Native emulation interfaces.
- Deterministic execution and replay.
- Structured hardware observability.
- Integration with AYTHER Engine.
- A foundation for future multisystem support.

**Status:** Active development. Initial MVP not yet accepted.

## Project Maturity

AYTHER is under active development. Individual components have different maturity levels, and no ecosystem-wide stable release is currently guaranteed.

Public APIs, supported platforms, pack formats, and compatibility contracts may evolve before their respective stable releases.

Refer to each repository's documentation and release notes for verified capabilities and current limitations.

## Open Technology, Independent Creativity

AYTHER follows an open-core model.

The public Engine, Runtime, SDK, Play CE, and Tessera projects provide the technological foundations for experimentation, interoperability, and community development.

Separate commercial products and services, including AYTHER Play, Lab, Hub, and Enterprise, may offer additional authoring workflows, connected services, distribution infrastructure, and professional integrations.

The public `.ay` format and community tooling are intended to remain usable without requiring proprietary authoring software.

## Get Involved

There are several ways to contribute:

- Improve code, tests, and performance.
- Review architecture and security.
- Improve documentation and developer onboarding.
- Test supported environments and report reproducible issues.
- Develop compatible tools and integrations.
- Contribute legally redistributable examples and test fixtures.

Start with the relevant repository's README, contribution guidelines, and open issues.

## Support Open-Source Development

AYTHER's public development includes engine technology, runtime integration, open tooling, deterministic emulation, documentation, testing, and community infrastructure.

**GitHub Sponsors will help sustain:**

- Maintenance and development of the public repositories.
- Cross-platform build and test infrastructure.
- Documentation, examples, and developer tools.
- Compatibility and conformance testing.
- Security hardening and release engineering.
- Long-term interoperability and preservation-oriented research.

Sponsorship supports the development of open-source technology. It does not purchase rights to third-party games, guarantee particular features, or grant commercial licenses.

_GitHub Sponsors enrollment is being prepared._

## Legal and Intellectual Property

AYTHER does not distribute commercial game ROMs, BIOS files, or unauthorized copyrighted game assets.

Users and contributors are responsible for obtaining the rights necessary to use and distribute their content.

Each public repository defines its applicable software license. Software licenses do not automatically grant rights to AYTHER trademarks or third-party intellectual property.

AYTHER is an independent project and is not affiliated with, endorsed by, or sponsored by Sega or any other game publisher or console manufacturer.

---

**AYTHER — Classic games. Reimagined.**

[ayther.dev](https://ayther.dev) · [Explore the Project](https://github.com/Ayther-Dev/AYTHER)
