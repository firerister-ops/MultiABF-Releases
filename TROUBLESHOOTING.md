# Troubleshooting

Open Settings → Diagnostics or the profile's Diagnostics action. Events identify creation, preparation, launch, running, cancellation and errors. A local diagnostic archive excludes free-form messages and configuration secrets; no archive is sent automatically. Review any attachment before publishing it in an issue.

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

The archive now contains the entire retained chronology, operation/stage durations and helper outcomes. Storage failure details show parent/child availability, individual checks, activation and phase counters, root-boundary evidence and failed bindings. The coverage section identifies the exported range; prior deleted events cannot be reconstructed. Raw identity values, argv and credentials are excluded, but your report description is included as written. No report is uploaded automatically.

## The selected executable was not recognized as PoE

Update to 1.0.3 or later. Choose PoE1 or PoE2 and the intended installed executable in Settings, then create the profile. Your explicit game selection is authoritative; a renamed or updated executable does not need to match embedded recognition markers. Saved profiles keep their game selection at launch. An older API integration that omits the game selection still uses automatic recognition.

## Disk capability and storage identity errors

Version 1.0.4 reads disk capabilities before applying MultiABF storage modules. A known unavailable property or unsupported identifier format can produce **partial** coverage: supported fields are verified and unavailable values remain native. Partial does not mean every hardware identity field is isolated.

Access denial, provider/read/clone failures, incorrect projected values and failed restoration remain blocking errors. Do not disable these checks to force a profile through. Send a new bug report from the failing preparation: its archive now includes each field's route, capability reason, HRESULT/type/status, active and restored checks, and nested WMI failures. Raw hardware identifiers and seed fingerprints are excluded from these diagnostic details.

The current release was checked with native helpers, controlled fixtures and the protected application without starting games or bots. The reporting device still needs to confirm its own result after updating.
