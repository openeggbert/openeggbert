# 🥚 OpenEggbert

**Open-source C++ game technology — 3D tooling, an XNA-style framework, compatibility layers, and game preservation.**

OpenEggbert is the open-source ecosystem of [Robert Vokáč](https://robertvokac.com): a family of modern C++ projects that build on each other — from a .NET-style runtime, through an XNA-style cross-platform framework, up to a 3D scene editor and playable game ports targeting Windows, Linux, WebAssembly, and Android.

🌐 [openeggbert.com](https://openeggbert.com) — ecosystem hub · 🎮 [speedyblupi.com](https://speedyblupi.com) — play the games in your browser · 👤 [robertvokac.com](https://robertvokac.com)

**≈560.5k lines of C++** across the projects below.¹

---

## 🔥 Projects

| Project | What it is | LOC | Web / Demo |
|---------|------------|----:|------------|
| [free-direct](https://github.com/openeggbert/free-direct) | DirectX 3 (2D) compatibility layer on SDL3 — DirectDraw/DirectSound subset for legacy games | ≈4.3k | [docs](https://freedirect.openeggbert.com) · [demo](https://speedyblupi.com/SpeedyEggbert2/) |
| [free-api](https://github.com/openeggbert/free-api) | Minimal Win32 API (circa 1998) compatibility layer on SDL3 — run legacy Windows games anywhere | ≈4.5k | [docs](https://freeapi.openeggbert.com) |
| [free-eggbert](https://github.com/openeggbert/free-eggbert) | Reverse-engineered, buildable reconstruction of Speedy Eggbert 2, made portable via free-api + free-direct | ≈28.1k | [docs](https://freeeggbert.openeggbert.com) · [demo (partial)](https://speedyblupi.com/SpeedyEggbert2/) |
| [mobile-eggbert](https://github.com/openeggbert/mobile-eggbert) | C++ port of Speedy Blupi (2013 Windows Phone XNA game) on CNA — fully playable in the browser | ≈20.5k | [docs](https://mobileeggbert.openeggbert.com) · [play](https://speedyblupi.com/SpeedyBlupi2013/) |
| [galaxy-eggbert](https://github.com/openeggbert/galaxy-eggbert) | 3D remake of Speedy Blupi / Mobile Eggbert on CNA + Easy3D — the sole implementation; the prior Simple3D/U3D path was fully retired and removed from the tree on 2026-07-25 | ≈18.5k | [docs](https://galaxyeggbert.openeggbert.com) |
| [easy-3d](https://github.com/openeggbert/easy-3d) | Small C++23 helper library beside CNA — cameras, texture atlas, billboard/cube batching, debug draw | ≈1.0k | [docs](https://easy3d.openeggbert.com) |
| [mobile-eggbert-legacy](https://github.com/openeggbert/mobile-eggbert-legacy) | Legacy C#/MonoGame preservation archive of Mobile Eggbert (ILSpy-decompiled Windows Phone XNA sources) | — | — |
| [mobile-eggbert-libgdx](https://github.com/openeggbert/mobile-eggbert-libgdx) | Java/LibGDX port of Speedy Blupi with a small XNA/.NET compatibility bridge | — | — |
| [sprite-utils](https://github.com/openeggbert/sprite-utils) | Small C++23 sprite utilities and assets (number spritesheets, web component) | ≈2.2k | — |
| [youtube-frontend](https://github.com/openeggbert/youtube-frontend) | C++23 static HTML index generator for ArchiveBox video archives (OpenCV + FFmpeg) | ≈2.3k | [web](https://youtube.openeggbert.com) |

¹ *LOC measured with cloc (August 2026): C++ sources and headers (`.cpp`/`.hpp`/`.h`), `src/` and `include/` directories only, excluding tests, vendored, and third-party code.*

---

## 🧱 How it fits together

```
mesh-craft   (3D scene editor, MC3 format)
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
