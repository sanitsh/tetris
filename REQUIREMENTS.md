Laptop 3D Tetris Requirements

Gameplay: Classic 7 tetrominoes with rotation, soft/hard drop, hold, preview queue, scoring/level/speed curve, pause, restart, keyboard-only and optional gamepad.
Visuals: Hardware-accelerated rendering (60fps target) with simple shaders, shadows/highlights for depth, grid/ghost piece, screen shake and particle bursts togglable for accessibility.
Audio: Music loop, SFX for drop/clear/rotate/level-up, volume sliders and mute toggles, audio latency under ~50ms.
UX/Accessibility: Rebindable controls, colorblind-safe palette, high-contrast mode, adjustable drop speed/delay windows, windowed/fullscreen toggle, resolution scaling, readable UI, seizure-safe effects option.
Persistence: Local highscores and settings saved to disk; no network dependency.
Stability/Perf: Runs on integrated laptop GPUs (e.g., Intel/AMD iGPUs), 1080p low preset at 60fps; memory footprint <200MB; startup <3s on SSD.
Testing/Quality: Unit tests for rotation/kicks, line clears, scoring; input lag checks; performance budget per frame; packaged build for Windows/macOS/Linux.
Tech Stack (balanced choice)

Engine: Godot 4 (GDScript/C#) – built-in 3D, cross-platform export, fast iteration, light footprint, good input/audio/UI pipeline.
Alternative native: Unity (C#) if you want richer tooling/asset store; set URP, disable heavy post-processing for laptops.
Low-level option: C++ + SDL2 for window/input/audio + bgfx for rendering, if you want minimal dependencies and tight control (higher dev effort).
Why Godot 4

Open-source, no royalties, straightforward 3D scene graph and shaders, export templates for all desktop platforms, responsive editor on laptops, solid input remapping and settings UI.
Next Steps

Decide engine (Godot vs Unity vs custom).
Prototype core loop: spawn/queue/hold, movement, wall kicks, line clears, scoring.
Add rendering pass: lit blocks, ghost, basic particles, simple post-processing toggle.
Implement settings/save system and key remapping; add tests for rotation/kicks logic.