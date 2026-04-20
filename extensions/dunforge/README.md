# DunForge Tiled Extension Scaffold

This directory is an early, non-invasive scaffold for DunForge inside Tiled.
It does not register a `.dun` map format yet. The first script only adds
validation and profile-inspection actions so development can begin safely.

## Files

```text
dunforge.js       Tiled scripting bootstrap
profiles/l1.json  First profile-data draft
```

## Local install during development

1. Open Tiled.
2. Open Preferences.
3. Go to Plugins or Scripting, depending on the Tiled version.
4. Add this directory as an extension or scripting folder.
5. Restart Tiled if the script does not hot-load.

## Development rules

- Keep the loader lossless before adding convenience edits.
- Keep profile mappings in data files, not hardcoded action logic.
- Treat subtile overlays as editor semantics, not as the binary source of truth.
- Register the `.dun` map format only after fixture-based round-trip tests exist.

## Planned actions

- Bind DunForge profile
- Validate current map
- Show round-trip safety report
- Import `.dun` with profile detection
- Export `.dun` with diagnostics
