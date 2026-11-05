# Changelog

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
