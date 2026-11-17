# Troubleshooting

Open Settings → Diagnostics or the profile's Diagnostics action. Events identify creation, preparation, launch, running, cancellation and errors. Diagnostic archives exclude configuration secrets. Automatic blocking-error reports are enabled by default and can be disabled in Settings → Diagnostics. Review any attachment before publishing it in an issue.

If first-run installation is canceled, no game profile is launched. Start MultiABF again to retry. Version 1.0.25 uses Direct only and does not install Sandboxie. UAC may also be required when enabling an optional separate Windows user.

If profile deletion fails, the profile is retained with pending cleanup. Use Delete again to complete it; do not manually delete account hives, recovery files or shared caches.

For bug reports include the MultiABF release, Windows version, the action performed and the displayed error code. Do not post proxy passwords, account credentials, raw client logs or screenshots containing account information.

## Unexpected game exit and HTTP 429

Version 1.0.26 refreshes exit evidence at terminal Direct cleanup. An exit code/time may still be unavailable when Windows cannot supply them; Unknown does not identify who closed the game or prove a crash cause. Use a fresh diagnostic archive for a repeated failure.

HTTP 429 concerns report delivery after the failure, not the game itself. The local archive stays pending. Retry after the server limit clears; the same report ID and bytes are reused. From 1.0.26, recognized server reason codes distinguish rate limiting from upload_busy when the server supplies that detail.


## ID! or a red ID row (1.0.25)

Open ID and expand the marked group for its reason. A failed optional ID channel uses system values; other verified channels continue. Assigned values/settings are retained. Retry using the existing profile preparation after resolving the cause. Ordinary starts do not repeatedly deep-check a remembered failure. Reports include error codes and safe hardware catalogue failure facts, not the full local identifiers.


## DPB launch

See [Launch DPB](DPB.md). Save the path to the complete installed DPB EXE, wait for the managed PoE1 profile to run, and use its profile menu. A disabled command explains its reason. DPB must be elevated through the integrated launcher; do not grant administrator membership to the game account. If initialization fails, record the profile diagnostic error; process-running alone is not proof of connection. DPB2 is not supported by this integration.

From1.0.32, exit-triggered reports include bounded, redacted technical evidence from that exact DPB run before the error is queued: errors, exception types, stack frames and fixed lifecycle markers. The archive records absent/unreadable/unsafe logs and truncation. Raw log files, settings, account data, paths and endpoints are excluded. If DPB did not write/flush a failure, the report cannot invent its cause from exit-1 alone.

## A profile cannot be created: file not found

In version 1.0.1 or later, read the creation step, File/component path and Windows number shown in the status bar. Hover over the status to read the complete message. If Windows did not report a path, the message states this explicitly.

Use **Report a problem** for the whole application after the failure, since the incomplete profile may have been rolled back. Include the full error shown on screen and the application version in your description. The diagnostic attachment retains the step and component basename, but deliberately omits full computer paths, command arguments and credentials. The update reports the cause; it does not automatically reinstall missing components.

## Storage identity readback rejected

For `identity_storage_device_readback_invalid`, update to 1.0.2 or later, repeat the failing profile preparation and use **Report a problem**. Select the whole application if profile creation was rolled back. Do not manually bypass the helper check.

The archive now contains the entire retained chronology, operation/stage durations and helper outcomes. Storage failure details show parent/child availability, individual checks, activation and phase counters, root-boundary evidence and failed bindings. The coverage section identifies the exported range; prior deleted events cannot be reconstructed. Raw identity values, argv and credentials are excluded, but your report description is included as written. Automatic blocking-error delivery follows Settings → Diagnostics.

## The selected executable was not recognized as PoE

Update to 1.0.3 or later. Choose PoE1 or PoE2 and the intended installed executable in Settings, then create the profile. Your explicit game selection is authoritative; a renamed or updated executable does not need to match embedded recognition markers. Saved profiles keep their game selection at launch. An older API integration that omits the game selection still uses automatic recognition.

## Disk capability and storage identity errors

Version 1.0.4 reads disk capabilities before applying MultiABF storage modules. A known unavailable property or unsupported identifier format can produce **partial** coverage: supported fields are verified and unavailable values remain native. Partial does not mean every hardware identity field is isolated.

From 1.0.25, failures limited to identity channels are shown as Failed in the ID table and do not block the entire profile. Other verified channels remain active. Ownership, incomplete restoration/cleanup, required executable/config/account and assigned proxy/privacy failures remain blocking. Send a new bug report from the failing preparation: its archive now includes each field's route, capability reason, HRESULT/type/status, active and restored checks, and nested WMI failures. Raw hardware identifiers and seed fingerprints are excluded from these diagnostic details.

The current release was checked with native helpers, controlled fixtures and the protected application without starting games or bots. The reporting device still needs to confirm its own result after updating.

## Profile creation: Generate identity / Windows error 2

The Windows message "The system cannot find the file specified" can refer to a volume lookup, not a missing game or helper executable. Version 1.0.5 handles a non-system volume disappearing or becoming not ready during enumeration, keeps healthy volumes, and records the skip. From 1.0.25, a failure limited to identity enumeration is recorded as an ID failure while independent channels continue. Actual launch/config/storage access requirements and unfinished cleanup remain blocking.

For volume-read failures, the error and diagnostic archive now identify the exact native API (for example QueryDosDeviceW or GetVolumePathNamesForVolumeNameW), the Windows error and the affected volume. The volume reference is its canonical Windows volume GUID, or the system drive root if its GUID could not be resolved. These details intentionally identify the problem volume; arbitrary folder paths, command arguments, disk serials and credentials are not included in this structured evidence.

Update and retry profile creation. A read-only retry with game launch disabled is enough to check the creation stage. If it still fails, send a fresh report containing the native-call and volume details. Reinstalling PoE or disabling identity checks is not a general solution to this error.

## Game exits, official update errors and canceled launches

Update to **1.0.7** or later so new reports include owned process exit evidence, the last window action, render/cache state, bounded redacted updater errors and the actual cancellation Stop outcome. Missing historical exit codes or dialog bodies cannot be recovered from an older report. A zero exit code does not establish a manual close. Keep the report number if you contact support; do not publish credentials or complete game logs.

## Unable to connect to patching server

The official game updater could not reach the patch server. If this occurs with a selected proxy, change the proxy or close the updater and update the game manually through the official launcher without a proxy, then retry in MultiABF. A successful proxy availability test does not prove access to the game patch server.

The existing **Settings → Automatically update the game** option controls the separate official update check. When it is disabled, normal profiles use their saved direct-launch arguments (new profiles use `--nopatch --nologo`). Skipping a launcher does not install a mandatory patch, so the game may still refuse login until manually updated. After a failed automatic update, MultiABF first closes its owned updater and tries direct launch with the assigned proxy. It retains an update warning and a separate fallback receipt for unchanged game files so other queued windows do not repeat the failed check. It never claims the game was updated. An updater still running or unconfirmed cleanup blocks that transition; assigned-proxy failures remain blocking.

From 1.0.33, send a fresh report after a failure: it includes the updater checkpoint, process-validation reason and Windows error when available, proxy assignment and bounded numeric evidence from that exact updater proxy run. Missing logs and truncated tails are explicit. The report contains no proxy addresses, passwords or raw proxy log lines. These observations distinguish failure stages; they cannot identify a cause that the updater/payload never recorded.
