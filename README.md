# OpenTooz 2027

An ambitious Windows-focused animation workstation built on the OpenToonz codebase.

> **Current status: planning and repository bootstrap.** This repository is currently a clean, empty project. It does not yet contain OpenToonz source code, a Windows executable, or a tested installer. Features listed below are targets, not claims that they are implemented.

## Project goals

- Preserve the original OpenToonz animation workflow and project compatibility.
- Improve the drawing experience with brush organization, tablet support, and accessible workspaces.
- Make reusable animation assets and symbol-like workflows easier to manage.
- Improve timeline, scene, audio, compositing, and export workflows.
- Provide practical presets for vertical 9:16 and landscape 16:9 video.
- Keep performance usable on modest Windows PCs, including systems with 8 GB RAM and integrated graphics.

## Development principles

1. Build on the upstream OpenToonz project; do not rewrite its animation engine unnecessarily.
2. Keep new features modular and optional.
3. Preserve compatibility with existing OpenToonz scenes wherever possible.
4. Make small, reviewable changes and test each change.
5. Never describe a feature or Windows build as complete until it has been implemented and verified.

## Planned milestones

| Milestone | Scope | Status |
|---|---|---|
| 0. Repository bootstrap | Project goals, architecture notes, development plan | In progress |
| 1. Upstream integration | Pin an upstream revision and establish a reproducible Windows build | Not started |
| 2. UX foundation | Workspaces, panel layouts, beginner/pro modes | Not started |
| 3. Drawing workflow | Brush presets, tablet behavior, drawing workspace improvements | Not started |
| 4. Animation workflow | Timeline usability, reusable asset/symbol workflow | Not started |
| 5. Video workflow | Shorts/landscape presets, audio workflow, export presets | Not started |
| 6. Packaging | Offline Windows installer, portable build, uninstaller and documentation | Not started |

## Hardware target

Initial optimization target: Windows 10/11 64-bit, 8 GB RAM, integrated graphics. Actual minimum requirements will be published only after profiling real builds.

## Important

The first engineering task is to bring in a pinned copy of upstream OpenToonz and reproduce its existing Windows build before modifying application behavior. See [the development roadmap](docs/ROADMAP.md) and [the architecture notes](docs/ARCHITECTURE.md).
