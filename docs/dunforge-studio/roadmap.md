# DunForge Studio Roadmap

## Phase 1: Format hardening

- Isolate map parsing and writing behind a small core module.
- Preserve unknown and skipped sub-layers instead of zeroing or dropping them.
- Add binary round-trip tests using known fixture maps.
- Create a validation report that flags lossy edits before export.

## Phase 2: Profile-driven Tiled workflow

- Add dungeon profile JSON files for each supported tileset family.
- Resolve tilesets from profile metadata instead of open-editor state.
- Add actions for binding, inspecting, and validating a map profile.
- Add subtile-aware helpers for monsters, objects, and room masks.

## Phase 3: Import and export ergonomics

- Add drag-and-drop map import.
- Auto-detect profile candidates from file path and map dimensions.
- Generate import and export diagnostics.
- Add a configurable handoff for testing maps outside the editor.

## Phase 4: DunForge Preview

- Build a separate 2.5D inspection surface.
- Live-reload from saved Tiled maps.
- Show walkability, occlusion, transparency, and room-mask overlays.
- Add debug camera modes and invalid-placement highlighting.

## Phase 5: Modding polish

- Support custom profile overrides.
- Add setpiece stamping.
- Add profile migration tooling.
- Publish extension packaging and contributor docs.
