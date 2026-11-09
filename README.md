# Cyber-Kinetic Sword Formation

An interactive 3D tactical blade array and quantum energy formation powered by **Three.js**, **UnrealBloom Post-Processing**, and **MediaPipe Hands** optical gesture tracking.

---

## 🌟 Key Features (Phase 1)

* **Cinematic UnrealBloom Post-Processing**: Integrated Three.js `EffectComposer` with `UnrealBloomPass` and ACES Filmic Tone Mapping, producing radiant plasma laser glows while preserving dark metallic contrast.
* **Dual-Layer Cyber-Katana (Plasma Kinetic Blade)**:
  - **Core Spine**: Dark brushed titanium / carbon-alloy physical backbone with angular crossguard and counterweight pommel.
  - **Plasma Laser Edge**: High-intensity luminous cutting edges and ion thrusters that bloom with brilliant energy.
* **Fluid Damped Spring Physics**: Replaced stiff linear interpolation with harmonic spring-damper physics, aerodynamic banking, and velocity-aligned rolls.
* **Military-Grade Futuristic HUD (FUI)**:
  - Real-time telemetry dashboard (FPS counter, active blade count, target coordinates, optical lock status).
  - Dynamic targeting reticle with smooth tracking.
  - Interactive stance selection buttons.
  - Real-time **Plasma Frequency Tuning** (Cyan Ion, Void Violet, Solar Gold, Hyper Crimson).
* **100% English Interface**: All code, documentation, and interface elements are fully localized in standard English.

---

## 🚀 How to Test & Run

### Option 1: Direct File Open (Instant Testing with Mouse Controls)
You can directly open `sword_formation.html` in your web browser:
1. Double-click `sword_formation.html` or drag it into Chrome, Edge, or Brave.
2. **Move Mouse**: The dynamic crosshair reticle and plasma beacon follow your cursor.
3. **Left Click & Hold**: Triggers the **Hyperdrive Strike** formation.
4. **HUD Buttons**: Click any formation button (`SWARM`, `STRIKE`, `DRILL`, `VORTEX`, `DRIFT`) or select a plasma frequency color pill to test blade tuning.

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
4. Show your hand to the camera to take command of the blade array.

---

## ✋ Optical Gesture Guide

| Hand Gesture | Tactical Stance | Behavior |
| :--- | :--- | :--- |
| ✋ **Open Palm** | **Orbital Swarm Shield** | 1,200 kinetic blades expand into a protective spherical orbital shield with dynamic banking. |
| ✊ **Closed Fist** | **Hyperdrive Strike** | Blades condense into concentric railgun rings and accelerate into a high-speed piercing barrage. |
| ✌️ **Sword Stance** | **High-RPM Laser Drill** | Blades align into a tight, spinning laser drill helix piercing forward at high velocity. |
| 👐 **Dual Hands** | **Dual Yin-Yang Vortex** | Blades split into two synchronized gravitational vortexes weaving between both hands. |
| 🌊 **No Hand / Idle** | **Harmonic Drift** | Blades gently undulate in a multi-layered matrix wave with synchronized roll. |

---

## 🛠️ Tech Stack & Architecture

* **Graphics**: Three.js (r128) with `InstancedMesh` (1,200 dual-layer blades rendered in 2 draw calls for locked 60 FPS).
* **Post-Processing**: `EffectComposer`, `RenderPass`, `UnrealBloomPass`, `ShaderPass`, `LuminosityHighPassShader`.
* **Vision AI**: MediaPipe Hands (v0.4) and MediaPipe Camera Utils.
* **Typography**: Google Fonts (`Rajdhani`, `JetBrains Mono`).
