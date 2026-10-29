# Troubleshooting

Open Settings → Diagnostics or the profile's Diagnostics action. Events identify creation, preparation, launch, running, cancellation and errors. A local diagnostic archive excludes free-form messages and configuration secrets; no archive is sent automatically. Review any attachment before publishing it in an issue.

If first-run installation is canceled, no game profile is launched. Start MultiABF again to retry. An incompatible or partial Sandboxie installation is left unchanged and reported explicitly. UAC may also be required when enabling an optional separate Windows user.

If profile deletion fails, the profile is retained with pending cleanup. Use Delete again to complete it; do not manually delete account hives, recovery files or shared caches.

For bug reports include the MultiABF release, Windows version, the action performed and the displayed error code. Do not post proxy passwords, account credentials, raw client logs or screenshots containing account information.

## DPB launch

See [Launch DPB](DPB.md). Save the path to the complete installed DPB EXE, wait for the managed PoE1 profile to run, and use its profile menu. A disabled command explains its reason. DPB must be elevated through the integrated launcher; do not grant administrator membership to the game account. If initialization fails, record the profile diagnostic error; process-running alone is not proof of connection. DPB2 is not supported by this integration.
