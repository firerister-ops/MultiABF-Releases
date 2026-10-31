# Risks, warnings and known limitations

[Overview](README.md) · [User guide](GUIDE.md) · [Troubleshooting](TROUBLESHOOTING.md)

## Game accounts and service rules

**MultiABF does not provide an anti-ban guarantee.** Isolation, different profile identifiers and a separate Windows account do not establish that accounts cannot be linked or sanctioned. Do not treat a green status or successful SDK connection as approval from a game publisher.

The [official Grinding Gear Games terms](https://www.pathofexile.com/legal/terms-of-use-and-privacy-policy) cover both PoE and PoE2 and restrict automated software/bots and unauthorized client modification. Violations can lead to loss of access. Review the current terms before deciding whether to use third-party software; this application does not grant an exception. Terms checked on 2026-10-31.

## Isolation and privacy limits

- A Sandboxie container and an optional standard Windows account are not a virtual machine or a separate physical computer. The host OS, drivers, installed game and hardware resources remain shared.
- Generated identifiers apply to implemented/verified surfaces. Some surfaces are unsupported, blocked or unmeasured. Complete hardware identity separation, anonymity and isolation from every game getter are not promised.
- Without an explicitly configured and verified route, profiles may share the host's public IP. A successful SOCKS5 connection test alone does not prove that all game traffic uses that route. MultiABF is not a system-wide VPN.
- Screenshots, logs and manually entered report text can contain sensitive data. The built-in report form excludes game logs, screenshots, passwords and settings, but you should still review your description and any files you share separately. Submitted reports are sent to the ABF server and its support/report-processing channel; the service necessarily handles the network connection.

## Compatibility and stability

- Game, DPB, plugin, Windows, graphics-driver and Sandboxie updates can change compatibility. PoE1 and PoE2 require their matching DPB generation. MultiABF does not repair third-party bot logic or guarantee plugin behavior.
- SDK attachment means the observed connection initialized; it is not proof of successful gameplay, every input path or every plugin. There can be crashes or hangs after a successful launch.
- Source windows are managed asynchronously. A launcher/game window can still be visible briefly during startup; suppression of every first frame is not guaranteed.
- The optional separate-Windows-user mode is experimental, needs account preparation and may take substantially longer on first use. Do not use OS-account cleanup tools manually against active managed accounts.
- Existing incompatible Sandboxie installations are not silently replaced. Review the reported conflict rather than changing shared driver configuration while clients are running.

## Resources, updates and data loss

- Several game clients share CPU, RAM, GPU and disk bandwidth. Client capacity depends on the machine and scene. Low RAM caps can prevent startup or terminate a client; CPU/FPS limits can reduce responsiveness. A resource cap does not reserve capacity.
- Official game updates modify the shared game installation, not just one container. Do not interrupt an active patcher or remove its files. A running client can block the update; cancellation of profile startup waits for safe updater completion.
- **Normal close stops managed game/DPB processes.** Save or finish any in-game work before closing MultiABF. A forced process kill or OS failure can leave work incomplete and require recovery.
- **Deleting a profile removes its owned local data and application-created Windows user.** Stop first, read the confirmation and keep a backup if needed. There is no claim of an undo/recycle-bin restore.
- Moving a data folder does not transfer machine-bound credentials or recreate Windows accounts. Keep backups before migration or changing installations; reselect paths on the destination computer.

## System permissions and licenses

Initial driver/service installation and managed-account work can require administrator permission. This affects the host Windows installation; it is not contained entirely inside a profile. Download MultiABF only from its [release repository](https://github.com/firerister-ops/MultiABF-Releases/releases), compare SHA256 and investigate security warnings rather than disabling security tools automatically.

MultiABF's freeware license does not replace the game, DPB or Sandboxie licenses. Sandboxie Plus has separate [certificate requirements](https://sandboxie-plus.com/contribute/) for certain business/education uses. Check the applicable terms yourself.

## What has and has not been verified

The published 1.0.0 artifact passed protected packaging, version/serialization and isolated API startup/shutdown checks. Earlier unchanged-code acceptance includes owned PoE1 managed runs and PoE2/DPB2 SDK startup, capture, interaction/return and shutdown. The reporting channel was verified through creation, duplicate-safe retry, stored/downloaded archive integrity and support-channel delivery.

This evidence does not establish universal hardware support, a fixed startup time, an unlimited client count, uninterrupted gameplay, complete identity coverage or immunity from game-account sanctions. If a problem occurs, stop the affected profile, record its operation/error and use **Report a problem**. Do not repeatedly restart a failing bot without understanding its requirements.
