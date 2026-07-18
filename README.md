# 🥚 OpenEggbert

**Open-source C++ game technology — 3D tooling, an XNA-style framework, compatibility layers, and game preservation.**

OpenEggbert is the open-source ecosystem of [Robert Vokáč](https://robertvokac.com): a family of modern C++ projects that build on each other — from a .NET-style runtime, through an XNA-style cross-platform framework, up to a 3D scene editor, a procedural world generator, and playable game ports targeting Windows, Linux, WebAssembly, and Android.

🌐 [openeggbert.com](https://openeggbert.com) — ecosystem hub · 🎮 [speedyblupi.com](https://speedyblupi.com) — play the games in your browser · 👤 [robertvokac.com](https://robertvokac.com)

**≈444.6k lines of C++** across the projects below.¹

---

## 🔥 Projects

| # | Project | What it is | LOC | Web / Demo |
|---|---------|------------|----:|------------|
| 1 | **[mesh-craft](https://github.com/openeggbert/mesh-craft)** 🚩 | Flagship — C++23 3D scene editor for the XML-based MC3 format: primitives, CSG booleans (Manifold), PBR materials, keyframe animation, glTF/GLB + MCB export | ≈29.4k | [meshcraft3d.com](https://meshcraft3d.com) |
| 2 | [mesh-world](https://github.com/openeggbert/mesh-world) | Procedural 3D world/city generator built on Mesh Craft — 20 C++ + 11 Lua generators, a planetary map subsystem (quadtree LOD, 52-biome classification), SQLite content packs, real-time chunk-streaming explorer | ≈16.9k | [meshworld3d.com](https://meshworld3d.com) |
| 3 | [cna](https://github.com/openeggbert/cna) | Modern C++23 reimplementation of the Microsoft XNA 4.0 API on SDL3 — 12 pluggable backends (SDL_Renderer, OpenGL, Vulkan, bgfx, WebGPU, Direct3D 9/11/12, SDL_GPU, Canvas, ASCII, DX3) and cross-platform networking | ≈181.2k | [libcna.com](https://libcna.com) · [demo](https://speedyblupi.com/SpeedyBlupi2013/) |
| 4 | [cna-samples](https://github.com/openeggbert/cna-samples) | C++ ports of the official Microsoft XNA Game Studio 4.0 sample collection running on CNA — web demos coming soon | ≈48.0k | — |
| 5 | [cna-craft](https://github.com/openeggbert/cna-craft) | Minecraft-like first-person voxel-world prototype on CNA, a faithful port of fogleman/Craft — chunk-streamed terrain, ambient occlusion, world-editing commands, SQLite persistence, multiplayer; in development | ≈6.3k | — |
| 6 | [sharp-runtime](https://github.com/openeggbert/sharp-runtime) | Pragmatic subset of the .NET runtime (`System::*`) in native C++ — the foundation layer under CNA and the tools | ≈70.7k | [docs](https://sharpruntime.openeggbert.com) |
| 7 | [free-direct](https://github.com/openeggbert/free-direct) | DirectX 3 (2D) compatibility layer on SDL3 — DirectDraw/DirectSound subset for legacy games | ≈4.3k | [docs](https://freedirect.openeggbert.com) · [demo](https://speedyblupi.com/SpeedyEggbert2/) |
| 8 | [free-api](https://github.com/openeggbert/free-api) | Minimal Win32 API (circa 1998) compatibility layer on SDL3 — run legacy Windows games anywhere | ≈4.5k | [docs](https://freeapi.openeggbert.com) |
| 9 | [free-eggbert](https://github.com/openeggbert/free-eggbert) | Reverse-engineered, buildable reconstruction of Speedy Eggbert 2, made portable via free-api + free-direct | ≈28.1k | [docs](https://freeeggbert.openeggbert.com) · [demo (partial)](https://speedyblupi.com/SpeedyEggbert2/) |
| 10 | [mobile-eggbert](https://github.com/openeggbert/mobile-eggbert) | C++ port of Speedy Blupi (2013 Windows Phone XNA game) on CNA — fully playable in the browser | ≈20.5k | [docs](https://mobileeggbert.openeggbert.com) · [play](https://speedyblupi.com/SpeedyBlupi2013/) |
| 11 | [galaxy-eggbert](https://github.com/openeggbert/galaxy-eggbert) | 3D remake of Speedy Blupi / Mobile Eggbert on CNA + Easy3D (sole active target since July 2026; the prior Simple3D/U3D path is historical reference only) | ≈17.3k | [docs](https://galaxyeggbert.openeggbert.com) |
| 12 | [easy-gl](https://github.com/openeggbert/easy-gl) | Toolkit-independent C++20 RAII wrapper over OpenGL / OpenGL ES — host owns the window and GL context | ≈3.6k | [docs](https://easygl.openeggbert.com) |
| 13 | [easy-3d](https://github.com/openeggbert/easy-3d) | Small C++23 helper library beside CNA — cameras, texture atlas, billboard/cube batching, debug draw | ≈1.0k | [docs](https://easy3d.openeggbert.com) |
| 14 | [meta-gl](https://github.com/openeggbert/meta-gl) | Low-level type-safe C++23 wrapper for OpenGL ES 2.0+ / WebGL — runtime function loading, enum-class GL constants | ≈8.3k | [docs](https://metagl.openeggbert.com) |
| 15 | [mobile-eggbert-legacy](https://github.com/openeggbert/mobile-eggbert-legacy) | Legacy C#/MonoGame preservation archive of Mobile Eggbert (ILSpy-decompiled Windows Phone XNA sources) | — | — |
| 16 | [mobile-eggbert-libgdx](https://github.com/openeggbert/mobile-eggbert-libgdx) | Java/LibGDX port of Speedy Blupi with a small XNA/.NET compatibility bridge | — | — |
| 17 | [sprite-utils](https://github.com/openeggbert/sprite-utils) | Small C++23 sprite utilities and assets (number spritesheets, web component) | ≈2.2k | — |
| 18 | [youtube-frontend](https://github.com/openeggbert/youtube-frontend) | C++23 static HTML index generator for ArchiveBox video archives (OpenCV + FFmpeg) | ≈2.3k | [web](https://youtube.openeggbert.com) |

¹ *LOC measured with cloc (July 2026): C++ sources and headers (`.cpp`/`.hpp`/`.h`), `src/` and `include/` directories only, excluding tests, vendored, and third-party code.*

---

## 🧱 How it fits together

```
mesh-world   (procedural 3D worlds)
  └── mesh-craft   (3D scene editor, MC3 format)
        └── CNA   (XNA-style cross-platform framework)   ←  cna-samples · cna-craft · easy-3d
              ├── easy-gl → meta-gl   (OpenGL layers)
              └── sharp-runtime   (.NET-style foundation)

free-eggbert   (Speedy Eggbert 2 reconstruction)
  └── free-direct   (DirectX 3 subset)
        └── free-api   (Win32 subset)   — both on SDL3

games: mobile-eggbert (C++/CNA) · galaxy-eggbert (3D) · cna-craft (voxel prototype) · legacy C# / Java ports
```

---

## 🎮 Play in the browser

WebAssembly builds hosted at [speedyblupi.com](https://speedyblupi.com):

* **[Speedy Blupi 2013](https://speedyblupi.com/SpeedyBlupi2013/)** — fully playable, with save persistence (Mobile Eggbert on CNA)
* **[Speedy Eggbert 2](https://speedyblupi.com/SpeedyEggbert2/)** — partially playable (Free Eggbert on free-api + free-direct)
* **[Planet Blupi](https://speedyblupi.com/PlanetBlupi/)** — the official open-source Blupi game

---

## 📫 Author

**Robert Vokáč** — Prague, Czech Republic

* Web: https://robertvokac.com
* Personal GitHub: https://github.com/robertvokac
* Email: [robertvokac@robertvokac.com](mailto:robertvokac@robertvokac.com)
