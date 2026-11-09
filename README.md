# Valyrian Kinetic Sword Formation

An interactive 3D tactical blade array and mastercraft sword formation powered by **Three.js**, **UnrealBloom Post-Processing**, and **MediaPipe Hands** optical gesture tracking.

---

## 🌟 Key Features

* **Mastercraft Valyrian Bastard Sword 3D Model**:
  - **Forged Blade & Fuller**: Extruded beveled high-carbon blade with blood groove fuller centerline.
  - **Gilded Crossguard & Arms**: High-detail center block with dual curved cylindrical arms.
  - **Leather Grip & 6 Gold Rings**: Dark leather-wrapped hilt fitted with 6 individual gold grip rings.
  - **Dodecahedron Pommel & Ruby Gem**: Gilded counterweight pommel inset with a glowing translucent ruby jewel.
* **Interactive Steel Finish Tuning**:
  - **Damascus Steel**: High-carbon forged steel (`metalness: 0.95`, `roughness: 0.15`).
  - **Obsidian**: Deep volcanic glass (`metalness: 0.70`, `roughness: 0.05`).
  - **Gilded Gold**: Solid gold ceremonial blade (`metalness: 0.90`, `roughness: 0.20`).
  - **Cyan Plasma**: Luminous radiant energy blade with UnrealBloom laser glow.
* **Concentric Planetary Orbital Physics**:
  - Swords glide along 3 inclined concentric planetary rings in **ORBITAL SWARM** mode, oriented along flight tangent paths with aerodynamic banking.
  - Damped harmonic spring physics for natural kinetic momentum and responsiveness.
* **Futuristic HUD (FUI) & Real-Time Telemetry**:
  - Real-time telemetry dashboard (FPS counter, blade count, target coordinates, optical lock status).
  - Dynamic targeting reticle tracking cursor and gesture focus.
  - Quick stance buttons (`SWARM`, `STRIKE`, `DRILL`, `VORTEX`, `DRIFT`).
  - Real-time blade finish switcher.
* **100% English Interface**: All code, documentation, and UI elements are in standard English.

---

## 🚀 How to Test & Run

### Option 1: Direct File Open (Instant Testing with Mouse Controls)
You can directly open `sword_formation.html` in your web browser:
1. Double-click `sword_formation.html` or drag it into Chrome, Edge, or Brave.
2. **Move Mouse**: The dynamic crosshair reticle and beacon track your cursor.
3. **Left Click & Hold**: Triggers the **Hyperdrive Strike** formation.
4. **HUD Buttons**: Click any stance button or steel finish button to test sword variations.

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
4. Show your hand to the camera to command the blade array.

---

## ✋ Optical Gesture Guide

| Hand Gesture | Tactical Stance | Behavior |
| :--- | :--- | :--- |
| ✋ **Open Palm** | **Orbital Swarm Shield** | Swords expand into 3 concentric rotating planetary rings with dynamic banking. |
| ✊ **Closed Fist** | **Hyperdrive Strike** | Swords condense into concentric railgun tiers and accelerate forward in a piercing barrage. |
| ✌️ **Sword Stance** | **High-RPM Laser Drill** | Swords align into a spinning dual-helix drill piercing forward at high velocity. |
| 👐 **Dual Hands** | **Dual Yin-Yang Vortex** | Swords split into two synchronized gravitational vortexes weaving between both hands. |
| 🌊 **No Hand / Idle** | **Harmonic Drift** | Swords gently undulate across a multi-layered matrix wave with synchronized roll. |

---

## 🛠️ Tech Stack & Architecture

* **Graphics**: Three.js (r128) with procedural 3D Valyrian sword groups (extruded beveled blades, fullers, crossguards, leather wraps, gold rings, pommels, and ruby gems).
* **Post-Processing**: `EffectComposer`, `RenderPass`, `UnrealBloomPass`, `ShaderPass`, `LuminosityHighPassShader`.
* **Vision AI**: MediaPipe Hands (v0.4) and MediaPipe Camera Utils.
* **Typography**: Google Fonts (`Rajdhani`, `JetBrains Mono`).
