# Data storage

- New installations: %LOCALAPPDATA%/MultiABF/data — database, profile settings and identifiers, UI/operator settings, logs, local diagnostic archives and cleanup records.
- An existing default %LOCALAPPDATA%/MultiClient database is reused in place so its saved paths and account bindings remain valid. An explicitly configured data directory is preserved. Settings → Open data folder always opens the active root.
- %LOCALAPPDATA%/MultiABF/runtime — shared native resources extracted from the EXE, grouped by content hash. These are application components, not per-profile identities.
- %PROGRAMDATA%/MultiClient — shared helpers and necessary account/recovery files, accessible to the configured Windows account.
- Sandboxie-managed directories — isolated profile game files.
- Windows-managed locations — service/driver registration and profiles for optional managed standard accounts.
- The .NET host may use its standard temporary extraction directory for native runtime files.

Profile deletion is available after Stop completes. The operation removes owned config/binding/window/verification files and profile identity/proxy/privacy/resource records when no other profile references them. A created Windows account is removed through its normal managed lifecycle. A driver-verified sandbox root is required before file deletion; links, unknown paths, live processes or locked files produce an error instead of a false success. Retry Delete after the reported obstruction is resolved. Interrupted deletion prevents a partially removed profile from launching.

Ordinary logs and generated local diagnostic ZIP archives follow the configured 7/14/30/90-day retention. Unresolved recovery evidence is preserved. Shared native/account caches are not deleted merely because one profile is removed. New native-cache sets carry a verified content catalogue; inactive sets older than seven days are retired only after full file/hash validation. Unknown or legacy sets and files in use are retained. Microsoft prerequisite downloads are kept in the active data root under cache/installers, verified before use, and removed after successful installation when Windows releases them.

Proxy passwords are stored in Windows Credential Manager. Managed Windows-account credentials use their protected local recovery store. Copying the data directory to another PC does not migrate those Windows-bound secrets or recreate Windows accounts. No credentials or complete game logs belong in this public repository.
