# Troubleshooting

Open Settings → Diagnostics or the profile's Diagnostics action. Events identify creation, preparation, launch, running, cancellation and errors. Diagnostic archives exclude configuration secrets. Automatic blocking-error reports are enabled by default and can be disabled in Settings → Diagnostics. Review any attachment before publishing it in an issue.

If first-run installation is canceled, no game profile is launched. Start MultiABF again to retry. An incompatible or partial Sandboxie installation is left unchanged and reported explicitly. UAC may also be required when enabling an optional separate Windows user.

If profile deletion fails, the profile is retained with pending cleanup. Use Delete again to complete it; do not manually delete account hives, recovery files or shared caches.

For bug reports include the MultiABF release, Windows version, the action performed and the displayed error code. Do not post proxy passwords, account credentials, raw client logs or screenshots containing account information.

## DPB launch

See [Launch DPB](DPB.md). Save the path to the complete installed DPB EXE, wait for the managed PoE1 profile to run, and use its profile menu. A disabled command explains its reason. DPB must be elevated through the integrated launcher; do not grant administrator membership to the game account. If initialization fails, record the profile diagnostic error; process-running alone is not proof of connection. DPB2 is not supported by this integration.

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

Access denial, provider/read/clone failures, incorrect projected values and failed restoration remain blocking errors. Do not disable these checks to force a profile through. Send a new bug report from the failing preparation: its archive now includes each field's route, capability reason, HRESULT/type/status, active and restored checks, and nested WMI failures. Raw hardware identifiers and seed fingerprints are excluded from these diagnostic details.

The current release was checked with native helpers, controlled fixtures and the protected application without starting games or bots. The reporting device still needs to confirm its own result after updating.

## Profile creation: Generate identity / Windows error 2

The Windows message "The system cannot find the file specified" can refer to a volume lookup, not a missing game or helper executable. Version 1.0.5 handles a non-system volume disappearing or becoming not ready during enumeration, keeps healthy volumes, and records the skip. A failure involving the system volume, access denial or incomplete enumeration still blocks creation.

For volume-read failures, the error and diagnostic archive now identify the exact native API (for example QueryDosDeviceW or GetVolumePathNamesForVolumeNameW), the Windows error and the affected volume. The volume reference is its canonical Windows volume GUID, or the system drive root if its GUID could not be resolved. These details intentionally identify the problem volume; arbitrary folder paths, command arguments, disk serials and credentials are not included in this structured evidence.

Update and retry profile creation. A read-only retry with game launch disabled is enough to check the creation stage. If it still fails, send a fresh report containing the native-call and volume details. Reinstalling PoE or disabling identity checks is not a general solution to this error.

## Game exits, official update errors and canceled launches

Update to **1.0.7** or later so new reports include owned process exit evidence, the last window action, render/cache state, bounded redacted updater errors and the actual cancellation Stop outcome. Missing historical exit codes or dialog bodies cannot be recovered from an older report. A zero exit code does not establish a manual close. Keep the report number if you contact support; do not publish credentials or complete game logs.
