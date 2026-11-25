# Architecture and upstream integration

## Starting point

OpenToonz is a mature C++/Qt animation application. The intended approach is to extend its existing systems rather than create a separate animation engine.

Previously inspected upstream areas include:

- Xsheet/timeline: `toonz/sources/common/txsheet` and public headers such as `toonz/sources/include/toonz/txsheet.h`.
- Drawing tools and brushes: `toonz/sources/tnztools`, including MyPaint-related brush tools.
- Brush assets: `stuff/library/mypaint brushes`.
- FX/compositing UI: FX schematic and stage schematic Qt components.
- Scene and palette APIs: public headers under `toonz/sources/include/toonz`.

These are initial repository reconnaissance notes, not a complete code audit. Paths and APIs must be verified against the exact upstream revision selected for this project.

## Integration rules

- Keep upstream license files and copyright notices intact.
- Track the exact upstream commit used as the base.
- Prefer small patches and separate modules over invasive rewrites.
- Avoid changing the native scene format unless there is a documented migration and compatibility plan.
- Do not bundle third-party libraries or media assets until their licenses and redistribution terms are checked.
- Keep network access optional for normal editing; offline installation and offline use are separate acceptance tests.

## Proposed feature boundaries

| Area | Preferred integration point | Main risk |
|---|---|---|
| Workspaces and themes | Existing Qt main-window/UI settings | UI regressions and settings migration |
| Brush organization | Existing MyPaint brush support and asset library | Tablet compatibility and memory use |
| Timeline improvements | Existing Xsheet/timeline model and widgets | Breaking established animation behavior |
| Reusable symbols | Scene/level/column abstractions after design review | Scene format compatibility |
| Audio/video workflow | Existing audio and FFmpeg pipeline | Codec licensing and platform differences |
| FX improvements | Existing FX graph/schematic | Render performance and project compatibility |
| Installer | Windows build and packaging pipeline | Missing runtime dependencies and licenses |

## Build gate

No feature work should be advertised as a working Windows application until the unmodified upstream project has been built and smoke-tested on Windows. This repository currently contains planning documents only.
