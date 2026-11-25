# Development roadmap

## Stage 0 — Bootstrap

- [x] Confirm the destination repository and write down the product goals.
- [x] Establish milestones and implementation rules.
- [ ] Record the upstream OpenToonz revision to use.
- [ ] Import or fork upstream source without losing its license notices and history.
- [ ] Verify the source tree and required submodules/assets.

## Stage 1 — Reproducible baseline build

- [ ] Read the current upstream Windows build instructions.
- [ ] Pin compiler, Qt, third-party dependencies and build configuration.
- [ ] Build unmodified OpenToonz on Windows 10/11 x64.
- [ ] Launch the application and open/save a sample scene.
- [ ] Record build steps, known issues and baseline performance.

**Exit condition:** a reproducible baseline build exists before feature work begins.

## Stage 2 — UX foundation

- [ ] Audit current Qt main-window, toolbar, panel and workspace code.
- [ ] Add saved workspace layouts without removing existing layouts.
- [ ] Add beginner/pro workspace presets.
- [ ] Add UI scaling and theme checks.

## Stage 3 — Drawing workflow

- [ ] Audit MyPaint brush integration and shipped brush assets.
- [ ] Organize brush presets by drawing purpose.
- [ ] Test pressure, tilt (where supported), Windows Ink and tablet devices.
- [ ] Improve stabilization and brush discoverability.
- [ ] Profile memory use with large canvases.

## Stage 4 — Animation workflow

- [ ] Audit Xsheet/timeline and keyframe editing.
- [ ] Design reusable asset/symbol workflow compatible with existing levels.
- [ ] Prototype symbol-like reusable animation assets only after compatibility review.
- [ ] Test nested scenes, timing, transforms and editing behavior.

## Stage 5 — Video workflow

- [ ] Add/document 9:16 and 16:9 project presets.
- [ ] Audit audio tracks, waveform display and synchronization.
- [ ] Audit FFmpeg integration and export presets.
- [ ] Test voice-over, subtitles/safe areas and final renders.

## Stage 6 — Effects and compositing

- [ ] Audit FX schematic and existing effects before adding duplicates.
- [ ] Identify high-value missing effects and implement incrementally.
- [ ] Test render quality, caching and low-memory behavior.

## Stage 7 — Windows packaging

- [ ] Create a clean offline-capable installer with required redistributables.
- [ ] Create a portable package where licensing and dependencies permit.
- [ ] Add uninstaller and install/upgrade tests.
- [ ] Test on a clean Windows machine with network disconnected.
- [ ] Publish checksums, version number and known limitations.

## Definition of done

A feature is done only when code is committed, builds successfully, relevant tests pass, manual behavior is checked, and user-facing documentation matches the actual behavior.
