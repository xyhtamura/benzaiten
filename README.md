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
- **2026-08-01 — Antigravity**: Added Physics Regimes selector (`DOMAIN WARP`, `NAVIER-STOKES`, `VISCOELASTIC`). Preserved original noise warp mode as default (`Domain Warp`), while providing 2D Navier-Stokes momentum/vorticity hydrodynamics and non-Newtonian viscoelastic shear-thinning liquid presets. Verified locally over HTTP server.
- **2026-08-01 — Antigravity**: Implemented GPGPU Fluid Particle Tracer System overlay ($10,000+$ particles). Particles stream, drift, and swirl along velocity vectors with additive point sprite glowing shaders. Added panel controls for tracer count, glow size, and advection speed.
- **2026-08-01 — Antigravity**: Configured Particle Tracers to be OFF by default (`partOn = false`). Integrated Multi-Touch Fluid Vortex & Sink Injectors: single finger stirs fluid momentum; two-finger pinch-in creates a fluid black hole/sink vortex ($-\mathbf{r}/r^2$), pinch-out creates a fluid geyser source ($+\mathbf{r}/r^2$), and dual dragging spawns twin counter-rotating swirl channels.
- **2026-08-01 — Antigravity**: Added Web Audio 3-Band Frequency Flow Coupling mode toggle (`pBandToggle`). Kept `PLAIN AMP` as default. When 3-Band Coupling is enabled, FFT spectrum is split into Bass ($0-300\text{ Hz}$ $\rightarrow$ Vorticity Swirl boost), Mids ($300\text{ Hz}-3.5\text{ kHz}$ $\rightarrow$ Convection Rate / Warp Scale), and Treble ($3.5\text{ kHz}-20\text{ kHz}$ $\rightarrow$ Chromatic Hue Shift).
- **2026-08-01 — Antigravity**: Added high-resolution PNG canvas snapshot export feature (`takeSnapshot()`). Enabled `preserveDrawingBuffer: true` on WebGL context, bound snapshot triggers to Top Bar button (`📷 SNAP (PNG)`), Panel button (`📷 EXPORT PNG SNAPSHOT`), and keyboard shortcut `S`. Downloaded files are named `benzaiten-flow-YYYYMMDD-HHMMSS.png`.
- **2026-08-01 — Antigravity**: Implemented 2D Magnetohydrodynamics (MHD) physics regimes (`u_phys_regime = 3` and `4`): `⚡ MHD PLASMA` (evaluates 2D magnetic vector potential $A_z$, current density $J_z = \nabla \times \mathbf{B}$, and Lorentz tension force $\mathbf{F}_L = \mathbf{J} \times \mathbf{B}$ with Alfven wave oscillations) and `☀️ SOLAR RECONNECTION` (simulates magnetic field line snapping and explosive coronal flare bursts). Added `MHD PLASMA` and `SOLAR FLARE` presets. Promoted 2D MHD gap in `physics/GAPS.md`.
- **2026-08-01 — Antigravity**: Fixed static `GRAD MAP` (Mode 2) shader issue where mapping only sampled static texture luminance. Coupled media luminance with dynamic fluid noise drift (`fract(lum + nv * 0.5)`), causing gradient color ramps to continuously flow through media contours and respond to mouse/touch fluid stirring.
