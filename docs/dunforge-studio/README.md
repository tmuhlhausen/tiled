# DunForge Studio

DunForge Studio is a Diablo-focused authoring concept built around Tiled as the
source-of-truth 2D editor, with a stricter `.dun` model and a future companion
preview application.

This scaffold captures the first slice of that direction inside the repository
without wiring it into the application build yet.

## Goals

- Keep `.dun` round-trips safe before adding any interpretation layers.
- Preserve raw Blizzard-era data where semantics are still uncertain.
- Move monster, object, and profile mappings out of hardcoded logic and into
  profile data.
- Make Tiled the authoritative editing surface for 2D authoring.
- Leave room for a later 2.5D preview/editor companion.

## Proposed split

### DunForge Core

Shared format and validation library.

Responsibilities:

- Parse and write `.dun` files.
- Preserve unknown raw sub-layer data.
- Provide editor-friendly views over base tiles, subtile occupancy, monsters,
  objects, and room masks.
- Validate profile bindings and round-trip safety.

### DunForge Tiled

A Tiled extension layer focused on workflow.

Responsibilities:

- Load and save `.dun`.
- Resolve dungeon profiles.
- Validate map configuration.
- Offer subtile-aware placement tools and room-mask editing.
- Improve import/export ergonomics.

### DunForge Preview

A future companion viewer/editor for Blizzard-faithful inspection.

Responsibilities:

- 2.5D visual validation.
- Walkability and occlusion overlays.
- Debug views for tile IDs, subtile occupancy, and invalid placements.

## Scaffold layout

```text
extensions/dunforge/
  README.md
  dunforge.js
  profiles/
    l1.json
```

## Next milestones

1. Convert the current scaffold into a real `.dun` loader/saver.
2. Add round-trip tests with fixture maps.
3. Replace implicit tileset discovery with explicit profiles.
4. Add drag-and-drop import and validation reporting.
5. Stand up the preview application once format fidelity is solid.
