## 1.0.27 - 2026-11-16

- Open Proxy in the top toolbar. Paste a list at the top or import TXT/CSV, then edit saved proxies in the table below. Common port/login/password fields fill missing values. The + button adds an empty row; fields can be copied and edited.
- New and changed proxies are checked automatically. Green/red status and response time show whether an HTTP request through SOCKS5 succeeds. This is not ICMP ping or proof of game routing.
- Keep named accounts and their assigned proxies in one place, see free/assigned proxies and select an account when creating or editing a profile. Both PoE1 and PoE2 are supported.
- Accounts and proxies persist after profile deletion. Copies retain the selected account/proxy while receiving independent profile IDs and configuration files.

Passwords remain in Windows Credential Manager and are excluded from ordinary API lists and diagnostic archives. Game sign-in remains manual; automatic login is not included.

## 1.0.26 - 2026-11-16

- Refresh final held-process exit evidence when Direct cleanup changes the profile to Stopped; preserve actual exit codes/time without inventing user intent.
- Keep recognized report-server rate-limit/upload-busy reasons beside HTTP status, without retaining raw error bodies.
- Preserve local pending report archives and the same upload ID/bytes on existing retry paths. No server-limit change or new automatic resend loop.
- The original game exit cause is not established by the old sample. No game/DPB/load run is part of this diagnostic release.

## 1.0.25 - 2026-11-16

- Direct-only profiles for PoE1/PoE2; remove Sandboxie backend/installer/settings while retaining legacy data and optional separate Windows users.
- Continue after individual ID failures, keep independently verified channels and assigned values, and show red Failed rows plus ID! on profile cards.
- Reuse unchanged ID proofs, retain valid WMI subsets on explicit retry, improve safe hardware-model failure diagnostics and fix live warning-label localization.
- Keep required EXE/account/proxy/privacy and ownership/cleanup errors blocking. Full ID values remain local.
- Reduce the sole EXE from about 599 to 301 MB. No new game/DPB/load runs are part of this release.

## 1.0.24 - 2026-11-15

- Reuse unchanged verified Direct ID channels across unrelated launcher updates; validate changed channel components, settings and account/hardware-dependent inputs.
- Prepare only channels that require a fresh check, preserving ready profile identifiers and their existing proof.
- Recover headless startup capture automatically when the game has not presented its first frame. Native errors, ownership failures and failed restoration remain blocking.
- Pre-release Home-PC verification starts20prepared PoE1 profiles without DPB in61.3seconds; all120channel receipts remain unchanged and all20reach headless, including two automatically recovered frame timeouts. This is a login-screen observation, not a universal timing or gameplay-capacity guarantee.
- Stable packaging passes173protected non-DPB checks. No further game or DPB tests are part of this release.

## 1.0.23 - 2026-11-15

- Preserve all selected Direct identities when a patched game hands off to a new executable child.
- Add verified compatibility data for the measured current PoE1 and PoE2 executable layouts; retain newer bundled/downloaded catalogs instead of downgrading them.
- Correct normal DPB closure when its settings window is open, and show a readable error when DPB cannot recognize the game build.
- Keep existing profile IDs and saved settings. DPB SDK compatibility is separate; no further DPB tests were performed for this release.

## 1.0.22 - 2026-11-15

- Signed background application updates, idle-only replacement/restart, an Updates settings tab, downgrade prevention and local rollback/recovery.
- Per-profile native DPB configuration seeding, remembered selection, independent copied settings and preservation across component refreshes.
- Product HTTPS update channel with one current stable server artifact; previous server EXEs are removed only after verified activation. Existing pre-updater installations require one manual update.

## 1.0.21 - 2026-11-15

- Keep game/frame input queues independent, preserve original ownership and maintain relative z-order without focus transfer.
- Preserve pointer/keyboard focus, native modules and saved identities; verify opening, menu navigation, minimize/restore and return to the wall.
- Home-PC three-profile PoE1 login-screen functional checks pass; no gameplay claim.

## 1.0.20 - 2026-11-14

- Faster owned game-window activation and overlapping previous-window headless caching.
- Preserve native modules and saved identities; add safe presentation-phase timings.
- Home-PC three-profile PoE1 login-screen checks pass; no universal timing or gameplay claim.

## 1.0.19 - 2026-11-14

- Structural game-image recognition, validated local cache and independently updated compatibility data.
- Preserve all selected Direct identities and leave optional rendering enabled if its layout is unresolved.
- Latest unknown-hash PoE1 image accepted on Home-PC with three full-ID profiles, headless restore/recache and repeat launch.

## 1.0.18 - 2026-11-14

- Support the verified PoE1 3.30.0 client for Direct CPU identities and DX11 cached headless mode.
- Official updates use the initiating profile proxy.
- Reuse prepared IDs after game-written config changes and clear resolved memory-wait notices.
- Repeated launch of 20 prepared PoE1 login-screen clients checked on Home-PC; no gameplay or universal timing claim.

## 1.0.9 - 2026-11-13

- Start ready profiles concurrently with Start all or Start selected. Compatible identity preparation is reused; changing related components, profile settings or hardware invalidates the corresponding proof.
- New profiles receive persistent realistic CPU/GPU model names. Existing identifiers and channel selections remain unchanged. Compact ID details show the assigned models and readable status.
- Separate GPU readings, RAM usage, commit and pagefile information make resource limits easier to see.
- Improved launch failure reasons, owned-process cancellation/cleanup and diagnostic reports for both PoE1 and PoE2.
- Protected package: 155 contract checks and 84 verified embedded resources. The beta acceptance checked ready-profile reuse and persistence on Home-PC for both games. Mass-start timing on this stable release is not yet measured. A rare reported WMI MAC failure remains under investigation; the new reports preserve its native error details.

# Changelog

## 1.0.8 — stable, 2026-11-08

- Profile ID inspection: hover over **ID** for a compact group summary with checked/saved/attention indicators. Click or press Enter/Space for a persistent details window with collapsible groups, selectable values and wheel scrolling. Green checks require matching preparation evidence; this is not a live check inside a running game.
- Preparation saves the full available assigned list locally, including storage-device IDs and network interface/association GUIDs. It is excluded from manual and automatic reports. Identical network association GUIDs are grouped; counts include virtual and system Windows interfaces, not just physical cards.
- New automatic Direct profiles and copies receive independent persistent identities. Existing unassigned profiles remain unchanged, including on Start; copies retain their selected channels.
- New Direct profiles select all supported identity channels, including CPU brand, GPU description, Vulkan UUID and Windows group/owner under the current user, including administrator. Existing explicit Off choices remain unchanged. CPU support validates exact game builds; unknown builds require a compatibility update. The compact ID summary includes CPU/GPU/RAM and original/Off states.
- Optional distribution of Direct DX11/DX12 clients across dedicated GPUs, accounting for pending and cached clients and weighting assignment by VRAM capacity. Disabled by default; Vulkan requires it to be disabled. This does not promise adaptive GPU-utilization balancing.
- Memory controls show Windows committed memory and manage bounded automatic pagefile growth. The growth limit is 32–128 GiB (128 GiB by default); launches wait when the required memory cannot be made available. Manual reduction saves the next-startup size and disables automatic growth. MultiABF never restarts Windows.
- Includes the 1.0.7 failure diagnostics and the background-render lifecycle fixes from the integrated work.

Stop managed profiles, close MultiABF and back up its active data folder before replacing the EXE. These checks do not establish a new in-game capacity or dual-GPU benchmark.

## 1.0.7 — stable diagnostics, 2026-11-07

- Automatic reports now retain the owned game's exit code and time, last window action, background-render/cache state and observed managed Stop requests. Unavailable data stays explicit; an exit code alone does not identify who closed a client.
- Official game-update failures include bounded error-dialog text with paths and private values redacted. Canceled launches retain the actual Stop result or exception category.
- Existing report opt-out and failed-delivery retry remain available. No screenshots, complete game logs or memory dumps are added. These diagnostics help investigate future failures; this update does not claim to fix the past reported crashes.

## 1.0.6 — stable, 2026-11-07

- Direct launches with independent persistent profiles and optional separate
  standard Windows users. Sandboxie installation is an explicit optional action.
- Improved window wall, taskbar-aware maximization, input defaults for both games,
  configuration Save/copy behavior and managed DPB launch/Stop handling.
- Optional **Disable rendering in the background** per profile, Off by default:
  retain a static frame in memory, restore rendering before Open, and refresh
  the frame on return. Initial support is verified PoE1 3.29.3c DX11 in Direct
  mode. Active managed DPB and unsupported builds/renderers remain unsuppressed.
- Normal official game updates, localized updater completion and correct cached
  update invalidation when the real game executable changes behind its launcher.
- Automatic blocking-error reports with opt-out, local delivery state and retry;
  ordinary validation, readiness, warnings and cancellation are excluded. Automatic
  reports do not include screenshots or complete game logs.

Background rendering suppression does not establish RAM/VRAM savings or a fixed
number of in-game clients. Autologin is not included. Back up profile data, stop
profiles and close MultiABF before replacing the EXE.

## 1.0.6-beta.1 — beta, 2026-11-05

- Direct mode: launch multiple clients with independent configs and optional
  separate standard Windows users, without installing Sandboxie.
- Retain the wall, interactive control, preparation, DPB attachment and exact Stop
  pipeline. Sandboxie installation is now an explicit Settings action.
- Include the complete Direct runtime in the standalone EXE; use portable absolute
  runtime paths and retain profile data when updating.
- Improve disk capability checks, real-volume verification and missing-board
  handling. Unsupported channels remain visible; genuine identity mismatches,
  access errors and restoration failures remain blocking.

Direct is not equivalent to Sandboxie isolation. Capacity at the login screen
does not establish capacity during gameplay or with bots. See [risks](RISKS.md).

## 1.0.5 - stable, 2026-11-02

Volume enumeration and profile-creation fix.

- Continue enumerating healthy local volumes when a non-system volume disappears or becomes not ready during a per-volume read; record the skipped volume and exact Windows call/error.
- Keep system-volume failures, access denial, unsupported operations and incomplete enumeration blocking. No empty-volume fallback or guessed identity.
- Show the exact native API and volume reference in profile-creation errors, the journal and diagnostic archives. Include skipped-volume observations in operation tracing.
- Apply the shared fix to PoE1/PoE2 runtime paths and both x64/x86 hardware diagnostic helpers. Preserve exact helper trust pins.

Checked without starting games or bots. The reporting user must retry profile creation to confirm their device-specific result.


## 1.0.4 - stable, 2026-11-02

Disk compatibility and diagnostic update.

- Read disk capabilities in a separate unboxed helper before enabling MultiABF storage modules.
- Verify supported fields individually; preserve unsupported native fields and report partial coverage explicitly.
- Keep access errors, corrupted data, projection mismatches and restoration failures blocking.
- Include per-field capability state, reason, route, HRESULT, CIM/VARIANT type, native status and returned lengths in diagnostic archives; retain nested WMI failure details without raw hardware identifiers.

Validated without starting games, DPB or bots. Partial hardware acceptance on the reporting machine remains to be confirmed.


## 1.0.3 - stable, 2026-11-02

- Respect your selected PoE1/PoE2 game instead of rejecting an executable because its embedded metadata is missing, changed or identifies another generation.
- Remove repeated game recognition from saved-profile launch and CPU/WMI-account preflight so the same rejection does not return later.
- Preserve the selected game and its configuration layout. Legacy API requests without a selected game retain automatic recognition.
- Existing file, helper ownership, architecture and identity readback requirements remain in place.


## 1.0.2 - stable, 2026-11-01

- Preserve the full available diagnostic history instead of only the last 250 events, including early failures for a selected profile.
- Trace operations, preparation stages, helper commands and rollback with timing, results, cancellation and error codes. Repeated frames and normal background polls are excluded.
- Include detailed storage-readback checks, parent/child verification and native counters for `identity_storage_device_readback_invalid`, plus structured privacy/readiness failures.
- Exclude raw identifiers, credentials, command arguments and host paths from diagnostic evidence. Existing journal retention still applies.
- Storage verification is unchanged. This update improves evidence; it does not claim to fix the customer's underlying disk compatibility failure.


## 1.0.1 - stable, 2026-11-01

- Explain profile-creation failures with the failing step, file/component path and Windows code for both games.
- Keep bounded creation-failure metadata in diagnostic reports after rollback without including command arguments, credentials or full host paths.
- Verified protected EXE error responses, report archives and normal shutdown without launching games or bots.

## 1.0.0 — stable, 2026-10-31

- Expanded feature overview, English interface screenshots, complete settings/workflow guide and explicit risks/privacy/deletion warnings. Documentation update only; release binary and tag are unchanged.

- Promote verified preview176 functionality to the stable main lane with a freshly compiled, jointly protected Windows x64 artifact.
- Active standalone MultiABF report channel, shared PoE1/PoE2 lifecycle, official updates, prepared-profile reuse and owned-account cleanup.
- Fresh package/API/version checks; unchanged functional source retains existing runtime acceptance limits.

## 2026-10-31 — Report backend activated

- Standalone MultiABF manual reports now reach the production receiver/private storage and existing notification channel with an explicit MultiABF product field.
- Protected preview176 sender, matching downloaded attachment and idempotent replay verified. No client binary change is required.

## 1.0.0-preview.176

- Register startup observation before CurrentUser Resume or at the earliest verified SeparateUser point; handle owned launchers/renderers before ordinary instance registration.
- Keep interactive windows and unrelated processes excluded; verify full process creation time.
- Common PoE1/PoE2 window path, 27 focused checks, owned WPF integration fixture and protected PoE2 API lifecycle acceptance.

## 1.0.0-preview.175

- Park owned launchers and repair observed source-window position/style resets without waiting for wall refresh.
- Keep interactive windows and unrelated processes excluded; verify full process creation time.
- Common PoE1/PoE2 window path, 22 focused checks, owned WPF integration fixture and protected PoE2 API lifecycle acceptance.

## 1.0.0-preview.174

- Compact profile actions at upper right, status at lower right and one-line PID/CPU/RAM/GPU/DPB telemetry.
- Separate PoE1/DPB1 and PoE2/DPB2 paths; observed SDK2 connection without bot Start.
- Normal application close stops owned game/DPB processes; profile deletion includes its owned separate Windows user.
- Official standalone game-update checks with cancellation and installation-busy handling; no fixed game-EXE hash allowlists.
- Grouped diagnostics and manually submitted report archives, with local retention on delivery failure.
- Stable preparation-proof contract and DPB rules prepared before caching, retaining actual native-component checks and fresh primary readback.
- Fixed protected Retry, live footer bindings and early launch-worker failure handling.

Third-party plugin/gameplay health and copying Windows-bound credentials between computers are outside SDK attachment acceptance.
