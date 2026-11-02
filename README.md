# 万剑归宗 (Cyber Xianxia Sword Formation)

An interactive 3D celestial flying sword formation powered by **Three.js** and **MediaPipe Hands** gesture recognition.

---

## 🚀 Quick Start

### Option 1: Direct File Open (Quick Preview with Mouse Controls)
You can directly double-click `sword_formation.html` in your browser.
- **Mouse Movement**: Moves the celestial focal point (Qi center).
- **Mouse Click & Hold**: Triggers the **万剑归宗 (Gather & Strike)** attack formation.
- **HUD Buttons**: Click buttons to switch formations anytime.

### Option 2: Run with Local Web Server (For AI Webcam Gesture Tracking)
Browsers require a secure context (`localhost` or `https`) for webcam access:

```bash
# Using Python
python -m http.server 8000

# Or using Node.js
npx serve .
```

Then open `http://localhost:8000/sword_formation.html` in Chrome or Edge and allow camera access.

---

## ✋ Hand Gestures & Stances

| Gesture | Stance | Formation Behavior |
| :--- | :--- | :--- |
| ✋ **Open Palm** | **天罡剑阵 (Celestial Swarm)** | Swords expand into a rotating spherical orbital shield |
| ✊ **Clenched Fist** | **万剑归宗 (Gather & Strike)** | Swords condense into a high-speed piercing cone barrage |
| ✌️ **Sword Finger** *(Taoist 剑指)* | **穿云剑诀 (Piercing Drill)** | Swords tighten into a rapid rotating laser drill helix |
| 👐 **Dual Hands** | **两仪剑阵 (Tai Chi Vortex)** | Swords split and weave between both hands in a dual vortex |
| 🌊 **No Hand / Idle** | **游剑海 (Cosmic Idle Drift)** | Swords gracefully undulate in 3D wave ripples |

---

## 🛠️ Issues Resolved

1. **Broken CDN script links**: Fixed invalid CDN endpoints (`cloudflare.com`, `jsdelivr.net`) to official Three.js r128 and MediaPipe libraries.
2. **MediaPipe asset loading path**: Fixed `locateFile` URL interpolation and path.
3. **Sword visibility & model**: Replaced wireframe cones with detailed double-edged flying swords (双刃飞剑) featuring diamond facets, crossguards, hilts, and dynamic glowing celestial colors (neon cyan, electric azure, imperial gold, and ethereal violet).
4. **Orientation alignment**: Fixed the 90-degree sideways orientation bug by aligning the sword geometry along the `+Z` forward axis.
5. **Formation collapsing**: Fixed attack and swarm formations so swords form majestic arrays instead of collapsing to a single point.
6. **Graceful fallback**: Added mouse/touch controls and HUD buttons so the swords are always interactive even if webcam access is denied or unavailable.
