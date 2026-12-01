# Valyrian Kinetic Sword Formation (万剑归宗)

An interactive 3D celestial flying sword formation and mastercraft blade array powered by **Three.js**, **UnrealBloom Post-Processing**, **MediaPipe Hands** optical gesture tracking, and real-time **Web Audio API** procedural sound synthesis.

---

## 🌟 Key Features

* **Mastercraft Valyrian Bastard Sword 3D Model**:
  - **Forged Blade & Fuller**: Extruded beveled high-carbon blade with blood groove fuller centerline.
  - **Gilded Crossguard & Arms**: High-detail center block with dual curved cylindrical quillons.
  - **Leather Grip & 6 Gold Rings**: Dark leather-wrapped hilt fitted with 6 individual gold grip rings.
  - **Dodecahedron Pommel & Ruby Gem**: Gilded counterweight pommel inset with a glowing translucent ruby jewel.
* **1,000+ Blade Array (Scalable up to 1,500 Swords)**:
  - High-performance multi-part `InstancedMesh` rendering delivering 1,000+ fully-featured 3D Valyrian swords at locked 60 FPS in just 4 GPU draw calls.
  - Array count selector: **500 SQUAD**, **1,000 LEGION**, **1,500 ARMADA**.
* **Boid Flocking & Organic Swarm Physics**:
  - Boid-inspired murmuration flocking with dynamic fluid air drag. Swords swoop, bank, and chase hand movements organically like a living magical cloud.
  - Velocity-aligned aerodynamic banking: blades roll and yaw into their flight velocity curve.
* **Staggered Liquid-Metal Morphing**:
  - Transitions between formations utilize cubic Bézier easing with per-blade wave delay. Swords peel out of one formation and swoop into the next rather than abruptly snapping.
* **Procedural Web Audio API Sound Synthesizer**:
  - 100% client-side sound synthesis — **zero external audio files required**.
  - **Ethereal Qi Drone**: Harmonic low-frequency ambient hum.
  - **Velocity-Reactive Whooshes**: Aerodynamic blade swooshing that dynamically pitches up with hand speed.
  - **Metallic Formation Clash**: Resonant Valyrian steel chime when formations lock.
  - Audio mute/unmute toggle in the top telemetry bar.
* **Perspective View Switcher & 360° Free Orbit**:
  - Quick perspective view presets in the tactical HUD:
    - **`SIDE VIEW`**: Pure side profile revealing full blade lengths and silhouettes.
    - **`3/4 ISOMETRIC`**: Angled 3D depth perspective.
    - **`TOP DOWN`**: Overhead view of planetary rings.
    - **`FRONT`**: Head-on tunnel view.
  - **Right-Click Drag** (or **Shift + Left-Click Drag**): 360° free orbit in 3D around the formation.
  - **Mouse Wheel Zoom**: Smoothly zoom in to inspect blade detailing or zoom out to view the entire legion.
* **Interactive Steel Finish Tuning**:
  - **Damascus Steel**: High-carbon forged steel (`metalness: 0.95`, `roughness: 0.15`).
  - **Obsidian**: Deep volcanic glass (`metalness: 0.70`, `roughness: 0.05`).
  - **Gilded Gold**: Solid gold ceremonial blade (`metalness: 0.90`, `roughness: 0.20`).
  - **Cyan Plasma**: Luminous radiant energy blade with UnrealBloom laser glow.
* **Futuristic HUD (FUI) & Real-Time Telemetry**:
  - Real-time telemetry dashboard (FPS counter, blade count, view mode, speed multiplier, target coordinates, optical lock status, audio status).
  - Dynamic targeting reticle tracking cursor and gesture focus.
  - Stance override buttons (`SWARM`, `STRIKE`, `DRILL`, `HALO`, `VORTEX`, `DRIFT`).
* **100% English Interface**: All code, documentation, and UI elements are in standard English.

---

## ✋ Optical Gesture Guide

| Hand Gesture | Tactical Stance | Behavior |
| :--- | :--- | :--- |
| ✋ **Open Palm** | **Orbital Swarm Shield** | 1,000 swords expand into 4 concentric rotating planetary rings with dynamic banking. |
| ✊ **Closed Fist** | **Wan Jian Gui Zong Strike** | Swords violently accelerate and converge into a massive railgun spearhead thrusting forward. |
| ✌️ **Sword Finger** *(Taoist 剑指)* | **Laser Drill Helix** | Swords align into a high-RPM spinning dual-helix drill locked along finger direction. |
| 🤏 **Pinch Gesture** | **Blade Halo Disc** | Swords compress into a tight, high-speed circular blade halo disc hovering above fingertips. |
| 👐 **Dual Hands** | **Dual Yin-Yang Vortex** | Swords split into two synchronized gravitational vortexes weaving between both hands. |
| 🌊 **No Hand / Idle** | **Harmonic Drift** | Swords gently undulate across a multi-layered matrix wave with synchronized roll. |

---

## 🚀 How to Test & Run

### Option 1: Direct File Open (Instant Testing with Mouse Controls)
You can directly open `sword_formation.html` in your web browser:
1. Double-click `sword_formation.html` or drag it into Chrome, Edge, or Brave.
2. **Move Mouse**: The dynamic crosshair reticle and beacon track your cursor, while the swords swoop and flock towards it.
3. **Left Click & Hold**: Triggers the **Wan Jian Gui Zong Strike** at supersonic speed.
4. **Right-Click Drag**: Freely orbit 360° around the formation in 3D.
5. **Mouse Wheel**: Zoom camera in and out.
6. **HUD Controls**:
   - Change formation: `SWARM`, `STRIKE`, `DRILL`, `HALO`, `VORTEX`, `DRIFT`.
   - Change perspective: `SIDE VIEW`, `3/4 ISOMETRIC`, `TOP DOWN`, `FRONT`.
   - Toggle audio: Click `AUDIO: ONLINE` in the top bar.
   - Change finish: `Damascus`, `Obsidian`, `Gilded Gold`, `Cyan Plasma`.
   - Change blade count: `500`, `1,000`, `1,500`.

### Option 2: Run with a Local Web Server (For AI Webcam Gesture Tracking)
Browsers require a secure origin (`localhost` or `https`) to access the webcam via `navigator.mediaDevices.getUserMedia`:

1. Open your terminal in this repository directory (`d:\sword_formation`):
   ```bash
   # Using Python 3:
   python -m http.server 8000

   # Or using Node.js:
   npx serve .
   ```
2. Open your browser and navigate to:
   ```
   http://localhost:8000/sword_formation.html
   ```
3. Click **Allow** when the browser prompts for camera permissions.
4. Show your hand to the camera to command the blade array using natural hand gestures.

---

## 🛠️ Tech Stack & Architecture

* **Graphics**: Three.js (r128) with `THREE.InstancedMesh` (1,000 to 1,500 Valyrian swords rendered in 4 draw calls).
* **Post-Processing**: `EffectComposer`, `RenderPass`, `UnrealBloomPass`, `ShaderPass`, `LuminosityHighPassShader`.
* **Vision AI**: MediaPipe Hands (v0.4) and MediaPipe Camera Utils.
* **Audio Synthesis**: Web Audio API (procedural low-frequency Qi drone, velocity noise whoosh, resonant steel clash).
* **Typography**: Google Fonts (`Rajdhani`, `JetBrains Mono`).

<!-- Milestone verified: 2026-12-01 11:00:00 +0530 -->
