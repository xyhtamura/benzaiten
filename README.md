# Benzaiten (弁財天) — Speculative Flow & Fluid Matter Engine

Standalone speculative instrument named after Benzaiten—the goddess of everything that flows (water, sound, time, eloquence, fluid matter).

- **Mechanism**: 2D GPGPU Navier-Stokes fluid dynamics solver + multi-scale noise domain warp + Web Audio FFT reactivity.
- **Substrates**:
  - `Mode 0`: Procedural Color Field (drifting 8-stop color ramp editor, stop locking/capture, presets).
  - `Mode 1`: Media Substrate (image / looping video / live webcam feed).
  - `Mode 2`: Hybrid Gradient Map (real-time colorization of media substrate via procedural color field).
- **Interface**: Mobile-friendly cybernetic HUD, responsive touch sliders, drag/touch fluid velocity stirring, dark mode (`U`), freeze (`Space`), drawer panel (`H`), fullscreen (`F`), media file load (`O`).

---

## Log

- **2026-08-01 — Antigravity**: Initialized standalone `benzaiten` project and repository. Built unified WebGL engine with Navier-Stokes fluid advection, multi-scale noise domain warp (`u_warp_scale_var`), procedural 8-stop color fields, media substrate upload, and hybrid gradient mapping. Reconfigured UI to be fully mobile-responsive with enlarged touch slider handles, responsive font scaling (`clamp()`), and launch defaulting to Mode 0 (Procedural Color Field). Verified locally over root HTTP server on port 8000 (`http://localhost:8000/benzaiten/`). Earmarked 2D MHD solver in `physics/GAPS.md`.
- **2026-08-01 — Antigravity**: Optimized flow engine for non-audio operation (`FLOW VELOCITY` baseline `0.10`), enabling rich, dynamic liquid flow on launch without microphone input. Added high-visibility desktop/mobile drawer tab handle (`CONTROLS`) and glowing pill button (`◈ SHOW UI`) in dark mode (`U`) for instant panel recovery.
- **2026-08-01 — Antigravity**: Fixed static `GRAD MAP` (Mode 2) shader issue where mapping only sampled static texture luminance. Coupled media luminance with dynamic fluid noise drift (`fract(lum + nv * 0.5)`), causing gradient color ramps to continuously flow through media contours and respond to mouse/touch fluid stirring.
