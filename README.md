# 🏭 IndustrialWorld

[![Engine](https://img.shields.io/badge/Unreal%20Engine-5.5+-black.svg?style=flat-square&logo=unrealengine&logoColor=white)](https://www.unrealengine.com/)
[![Focus](https://img.shields.io/badge/Design-Sleek%20%7C%20Minimal%20%7C%20Premium-E0A96D.svg?style=flat-square)](#)
[![Target](https://img.shields.io/badge/AI--Optimized-Context%20Ready-00ADB5.svg?style=flat-square)](#-ai-agent-system-prompt--execution-guidelines)

`IndustrialWorld` is a next-generation automation and industrial simulation project built from the ground up on **Unreal Engine 5.5+**. The project is architected with a strict core philosophy: **radical simplicity in execution, absolute premium quality in aesthetics, and incredibly fluid, responsive user experiences.** Instead of overwhelming players with visual clutter, `IndustrialWorld` focuses on minimal, sleek, high-fidelity UI/UX design, micro-interactions, and pristine production quality to deliver a deeply satisfying and complete game feel.

---

## 🧭 Project Blueprint & Core Pillars

When building or modifying features for this project, always adhere to our three core execution pillars:

┌─────────────────────────────────────────────────────────────────┐
│                       INDUSTRIAL WORLD                          │
├───────────────────┬───────────────────────┬─────────────────────┤
│   1. SIMPLICITY   │   2. SLEEK AESTHETICS │ 3. PRODUCTION VALUE │
│ Lean code systems │ Minimalist HUD & UIs  │ Micro-interactions  │
│ Modular design    │ High-contrast layouts │ Absolute completeness│
└───────────────────┴───────────────────────┴─────────────────────┘

1. **Simplicity First:** Code architecture must be clean, highly decoupled, and easily readable. Game mechanics should be intuitive but possess deep systemic emergence. Avoid over-engineering.
2. **Sleek & Pretty Visuals:** UIs must feature plenty of breathing room (negative space), elegant typography, smooth transitions, and monochromatic/muted corporate-industrial color palettes accented with subtle glowing indicators.
3. **Flawless Quality ("Game Feel"):** Every click, hover, drag, and state change must feel tactile. Use subtle juice—easing functions, camera shakes, particle bursts, and UI interpolation—to make the game feel polished and finished.

---

## 🤖 AI Agent System Prompt & Execution Guidelines

> **🚨 CRITICAL INSTRUCTION FOR REASONING LLMs & LLMs AUTOMATIONS:**
> You are acting as an expert Senior Unreal Engine Systems Architect and High-Fidelity Technical UI/UX Designer. Read this section before generating code, proposing features, or refactoring classes within this codebase.

### 🧠 1. Cognitive Operational Constraints
* **Efficiency First:** Write highly optimized C++ code conforming to **modern Unreal Engine standards (UE 5.5+)**. Leverage Unreal's memory management (`UPROPERTY()`), TArrays, TMaps, and minimize heavy operations inside `Tick()`.
* **Zero Bloat:** Never provide repetitive or boilerplate logic unless explicitly requested. Prefer concise, modular, and self-documenting code using appropriate engine patterns (Subsystems, Actor Components, Interfaces).
* **The "Finished Product" Rule:** When generating code, never write half-finished placeholders (`// TODO: Implement later`). Every piece of code must be fully fleshed out, safe against null pointers (`IsValid()`), and complete.

### 🎨 2. UI & Interaction Philosophy (Strict Requirements)
Our UI is **not** a traditional cluttered industrial spreadsheet. It is closer to a luxury premium OS dashboard.
* **Component Preference:** Use **UMG (Unreal Motion Graphics)** backed by robust **C++ UserWidget classes** (`UUserWidget`), or raw **Slate** for editor tooling.
* **Animation & Motion:** Never let UI elements appear or disappear instantly. Always animate transitions programmatically using UMG Animations, `FInterpTo`, or `FRuntimeFloatCurve` data tracks with professional easing functions (e.g., Ease In/Out).
* **Micro-interactions:** Every UI button must have distinctive, beautiful visual states for `Normal`, `Hovered`, `Pressed`, and `Disabled`. Use slight scale shifts (e.g., scale to `1.03x` on hover via Render Transform) and linear color interpolation over `0.1s`.

### 💻 3. Coding Style Guide
* Follow standard **Unreal Engine C++ Coding Standards**:
  * PascalCase for all classes, functions, and variables.
  * Prefix rules: `A` for Actors (e.g., `AIndustrialNode`), `U` for Objects/Components (e.g., `USimulationEngine`), `F` for Structs, `I` for Interfaces, and `E` for Enums.
* Implement structured event-driven code using **Dynamic Single/Multi-cast Delegates** (`DECLARE_DYNAMIC_MULTICAST_DELEGATE`) to keep core logic strictly decoupled from visual UI systems.
* Keep standard module/folder structures clean and matching engine patterns: `Source/IndustrialWorld/Core`, `Source/IndustrialWorld/Simulation`, `Source/IndustrialWorld/UI`.

---

## 🛠️ Step-by-Step AI Development Workflow

When tasked to build a feature or fix a bug in `IndustrialWorld`, execute the following loop:

  [1] ANALYZE   ──> Review current systems, dependencies, and scene hierarchy.
       │
  [2] MINIMIZE  ──> Strip out unnecessary steps. Design the cleanest code possible.
       │
  [3] BEAUTIFY  ──> Ensure visual feedback, UI styling, and animations look pristine.
       │
  [4] HARDEN    ──> Add robust error handling, null-checks, and performance validation.

  1. **Analyze Requirements:** Understand how the feature interacts with existing world-state subsystems and the global GameState.
2. **Design For Simplicity:** Keep data structures simple. Use `UDataAsset` for configuration and data-driven designs wherever applicable.
3. **Execute High-Fidelity UI/UX:** Proactively add UI handling code, juice, and sound triggers via C++ controllers to match our high-quality guidelines.
4. **Harden & Format:** Clean up the script, ensure proper encapsulation (`private`/`protected` with `meta = (AllowPrivateAccess = "true")`), and eliminate compiler warnings.

---

## 🏗️ Technical Architecture Matrix

The project structure is broken down into clean, single-responsibility domains:

| Module / Path | Primary Target / Purpose | Style Guidance |
| :--- | :--- | :--- |
| **`IndustrialWorld/Core`** | Global `UGameInstanceSubsystem`, custom `AGameState`, and bootstrapper code. | Robust, performant, persistent across map travels. |
| **`IndustrialWorld/Simulation`** | Processing nodes, resource logistics, pathfinding (`AActor`, `UActorComponent`). | Lightweight data types, deterministic, minimized ticking. |
| **`IndustrialWorld/UI`** | Menus, contextual overlays, building HUDs (`UUserWidget`, `AHUD`). | Sleek layout, responsive vector brushes, elegant widget animations. |
| **`IndustrialWorld/FX`** | Niagara particle systems, post-processing materials, audio cues. | Subtle, premium look using Lumen, Virtual Shadows, and strict color grading. |

---

## 🚀 Getting Started with Unreal Engine 5.5+

### Prerequisites
* **Epic Games Launcher** with **Unreal Engine 5.5.x** installed.
* **IDE:** Visual Studio 2022 (with Game Development with C++ workload) or JetBrains Rider.
* **Rendering Settings:** Lumen and Virtual Shadow Maps enabled. Keep modern post-processing active (Bloom, Film Tonemapping) to support the sleek look.

### Repository Conventions
* **Main Branch:** Protected. All work must be done via clean feature branches (`feature/your-feature-name`).
* **Commit Messages:** Must be descriptive and semantic (e.g., `feat(ui): add sleek contextual radial menu for machine upgrades`).

---

<p align="center">
  Designed with absolute precision. Focused on simplicity. Built for pure quality.
</p>
