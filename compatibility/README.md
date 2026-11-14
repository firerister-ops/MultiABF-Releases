# Game compatibility data

MultiABF 1.0.19 and later resolve game CPU instructions and supported DX11 render layouts from executable structure. This catalog supplies separately published exact descriptions, masked recipes and confirmed non-instruction exclusions. It contains no executable payloads or user identifiers.

The runtime checks schema, image identity, PE sections and actual instructions before use. Unknown required CPU layouts block launch with an actionable error. Unknown optional render layouts leave rendering enabled. Validated descriptions are cached locally by image hash. A compatible ordinary patch does not require a new MultiABF binary. Changes to the hook mechanism can still require an application update.

The built-in baseline works offline. When local recognition fails, the runtime requests `catalog.v1.json` from this publisher repository over HTTPS with a five-second bound. Data revisions are independent of application versions. Render recipes here are explicitly game/renderer-specific; current generic render recognition is PoE1 DX11.
