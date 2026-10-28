# MultiABF

A Windows desktop manager for persistent Path of Exile 1 and Path of Exile 2 profiles and a live wall of game windows.

This repository contains documentation and binary releases only. MultiABF source code and development history are kept separately and are not public. Third-party components retain their own licenses.

## Download status

Download the Windows x64 preview EXE from [release 1.0.0-preview.164](https://github.com/firerister-ops/MultiABF-Releases/releases/tag/v1.0.0-preview.164). Place it in a permanent directory and compare its SHA256 with the published SHA256SUMS file. Preview builds are intended for evaluation.

## Getting started

1. Download the release EXE and place it in a permanent directory.
2. Start MultiABF. The distribution contains .NET, MultiABF components and the original pinned Sandboxie installer. If Microsoft Visual C++ x64 Runtime is missing or too old, MultiABF downloads the pinned original package directly from Microsoft and verifies its SHA256 before installation. Internet is required for that prerequisite only. First-time dependency/driver/service installation requires the Windows UAC prompt.
3. Select your PoE1 or PoE2 executable in Settings.
4. Create a profile, adjust its game settings if needed, and select Start.
5. Open a tile to control the game. Back to wall restores the main window. Stop closes the managed instance.

Creating and starting are separate actions. Generated identifiers are saved once and reused; restarting or changing display settings does not generate a new identity. Copy creates a separate profile with new identifiers.

## Settings

- English is the default for a new installation. Russian is available under Settings → General → Language / Язык. An existing selection is preserved.
- Tray minimization is optional and disabled by default.
- Active window size is global; game resolution and FPS limits belong to each profile.
- SOCKS5, CPU/RAM limits and an experimental separate standard Windows user are optional profile settings. Initial preparation in separate-user mode takes longer.
- Previous/next window and return-to-wall shortcuts can be recorded or disabled in Settings.
- Diagnostic archives remain local; no automatic upload is enabled.

## System requirements and limits

Windows x64 with Windows Graphics Capture support; the current build targets Windows 10 build 19041 or later. Sandboxie core 5.73.4 (Plus 1.18.4) is the pinned backend. Other existing Sandboxie versions are not automatically replaced. Administrator permission is needed for driver/service installation and managed account setup.

Acceptance covers a Windows 10 laptop with one NVMe volume and hybrid NVIDIA/Intel graphics, and a desktop with three fixed volumes. The accepted R164 laptop runs use one test client at a time, with both ordinary and separate standard Windows-user profiles. The same executable passed sequential blank-login, navigation, exact Stop and restart-persistence checks with PoE1 and PoE2 on the desktop, in both user modes. Different hardware and actual gameplay capacity may differ. Do not infer complete hardware-identity coverage from a profile status indicator; unsupported surfaces remain explicit.

## Data and removal

See [Data storage](DATA.md) and [Troubleshooting](TROUBLESHOOTING.md). Deleting a stopped managed profile also removes its owned data and any Windows account created for it. Shared dependencies and other profiles are retained.

## License

MultiABF is proprietary freeware. See [LICENSE.txt](LICENSE.txt) for our components and [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt) for dependencies. Free use does not remove Sandboxie's own commercial-use conditions.
