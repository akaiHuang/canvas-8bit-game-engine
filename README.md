# Canvas 8-Bit Game Engine

**Narrative-Driven Space Invaders with Pixel Art, CRT Effects, and Visual Evolution**

---

## About

Canvas 8-Bit Game Engine 是一個以原生 JavaScript 與 HTML5 Canvas 從零打造的復古遊戲引擎與示範遊戲。適合用於學習遊戲迴圈、碰撞偵測、粒子/特效與像素美術渲染，也可作為教學與作品集專案。

## About (EN)

Canvas 8-Bit Game Engine is a from-scratch JavaScript and HTML5 Canvas engine with a complete retro game implementation. It is a practical learning project for game loops, collision systems, sprite rendering, and visual effects.

## 📋 Quick Summary

> 🎮 這是一款**純手工打造的 8-bit 復古遊戲引擎**，不使用任何遊戲框架，僅靠 HTML5 Canvas 2D API 和原生 JavaScript 構建完整的 Space Invaders 風格遊戲。🌟 最大亮點是**敘事驅動的視覺進化系統**——玩家從黑白 CRT 濾鏡世界起步，隨著分數推進，畫面逐步從單色演變為彩色、最終進入全霓虹特效，遊戲本身就是一場視覺變革的隱喻。👾 引擎包含像素藝術精靈定義（螃蟹、烏賊、章魚外星人，11x8 二進位矩陣）、**四種武器系統**（含過熱機制與彈藥管理）、寶石掉落概率表、徽章/成就解鎖系統，以及完整的故事對話序列。📺 CRT 效果包含掃描線、故障文字特效和老電視閃爍動畫。🎨 伴隨的特效檔案展示了 Three.js 3D 文字陣列（含霧效）和有機形態變形幾何視覺化。⚡ 每個檔案完全獨立，無需建置步驟、無需安裝套件、無需伺服器。適合對**遊戲引擎原理、Canvas 渲染、復古像素藝術**有興趣的開發者學習。

---

## 🤔 Why This Exists

Most game demos on the web are either trivial toys or heavy Unity/Unreal exports. There is a gap: where do you find a hand-crafted game engine that demonstrates real interactive development skill -- collision systems, sprite animation, particle effects, state machines, narrative design -- without hiding behind a framework?

Canvas 8-Bit Game Engine is that proof of concept. It is a complete Space Invaders-style game built from scratch with a twist: the game tells a story. Players start in a monochrome, CRT-filtered world. As they progress, the visuals evolve -- from grayscale to color to full neon. The game itself is a metaphor for brand transformation, originally designed as an interactive demo for Universal FAW Labs' brand experience platform.

The engine includes pixel-art sprite definitions (crab, squid, octopus aliens), weapon systems with overheating mechanics, a badge/achievement system, power-up drops, and a full story progression with dialog sequences. The companion effect files demonstrate Three.js 3D text arrays with fog, and organic morphing geometry visualizations.

No game libraries. No frameworks. Just Canvas, JavaScript, and the craft of making things move on screen.

---

## 🏗️ Architecture

```
canvas-8bit-game-engine/
|
|-- game_v1.html         Game Engine v1
|                        - Core Space Invaders mechanics
|                        - Pixel-art alien sprites (11x8 grids)
|                        - CRT scanline + glitch text effects
|                        - Canvas-based rendering loop
|                        - Collision detection
|
|-- game_v2.html         Game Engine v2 (Main Engine, 1330+ lines)
|                        - Full narrative progression system
|                        - Three visual stages: Mono -> Color -> Neon
|                        - Weapon system (default, red, green, blue, gold)
|                        - Overheating mechanics + ammo management
|                        - Badge/achievement unlock system
|                        - Power-up drops with probability tables
|                        - Configurable alien assets and weapons
|                        - Settings panel + pixel editor integration
|                        - Old-TV CRT filter with flicker animation
|                        - Level-clear and game-over sequences
|
|-- effect.html          Three.js 3D Text Array
|                        - 3D text rendering with depth and fog
|                        - Dynamic camera controls
|                        - Loading state management
|
|-- bgeffect.html        Three.js Organic Geometry
|                        - Multiple morphing 3D shapes
|                        - Shape switching UI
|                        - Real-time parameter controls
|
|-- demo-index.html      Brand Landing Page
|                        - Industrial blueprint aesthetic
|                        - Service showcase layout
|                        - Module pricing grid
```

### Game Engine Features (v2)

**Rendering**
- Canvas 2D context with requestAnimationFrame game loop
- Pixel-perfect sprite rendering from 11x8 binary grid definitions
- Two-frame sprite animation for alien movement
- Dynamic canvas resizing to parent container

**Visual Progression**
- Stage 0: Monochrome with old-TV grayscale filter
- Stage 1: Color unlocked, CRT effects remain
- Stage 2: Full neon with enhanced visual effects
- Transitions triggered by score thresholds with story dialog

**Combat System**
- Four weapon types with distinct behaviors
- Red weapon: high damage, limited ammo with overheating cooldown
- Green/Blue/Gold: varied fire rates and damage profiles
- Power-up gem drops from defeated aliens with configurable probability

**Game State**
- Score tracking, level progression, pause/resume
- Badge system with unlock conditions
- Alien descent timer with escalating difficulty
- Configurable game assets (sprites, weapons, badges) through settings panel

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Game Engine | HTML5 Canvas 2D API, requestAnimationFrame |
| UI Framework | React (for game chrome, menus, dialogs) |
| 3D Effects | Three.js (effect pages only) |
| Sprite System | Binary grid definitions (11x8 matrices) |
| Styling | Tailwind CSS (utility classes), custom CSS animations |
| Fonts | Press Start 2P (retro), Rajdhani (tech), JetBrains Mono (code) |
| Visual Effects | CRT scanlines, glitch text, old-TV filter, flicker animation |

---

## 🚀 Quick Start

Each file is self-contained. Open any HTML file directly in a browser:

```bash
# Open the main game engine
open game_v2.html

# Open the first version
open game_v1.html

# View 3D text effect
open effect.html

# View organic geometry effect
open bgeffect.html
```

No build step. No dependencies to install. No server required.

---

## 👤 Author

**Huang Akai (Kai)** -- Founder @ Universal FAW Labs | Creative Technologist | Ex-Ogilvy | 15+ years in digital creative and marketing technology.
