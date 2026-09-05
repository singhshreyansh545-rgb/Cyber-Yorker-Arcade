# Cyber Yorker: Arcade Edition 🏏

A high-octane, single-file HTML5 Canvas arcade game featuring custom physics, procedural audio, and a retro cyberpunk aesthetic. 

Built entirely from scratch without external game engines or asset libraries, this project serves as a demonstration of vanilla JavaScript mechanics, applied trigonometry, and native browser APIs.

## 🚀 Play It Now
[**Play the Live Demo Here**](https://your-username.github.io/your-repo-name) *(Update this link once GitHub Pages is enabled)*

## 🎮 Gameplay Mechanics
- **Pointer Tracking Launcher:** The cannon smoothly tracks the user's mouse or touch position, allowing for precise 360-degree aiming.
- **Combo Multiplier:** Consecutive hits without missing build a streak, increasing target speed and point yield.
- **The Sweeper Shield:** A dynamic, orbiting obstacle that blocks shots and breaks combos upon impact.
- **Juice & Game Feel:** Features screen shake, kinetic particle explosions, floating combat text, and motion-blur trails.

## 🛠️ Technical Implementation

### Trigonometric Projectile Motion
Directional velocity is calculated dynamically using `Math.atan2()` to find the angle between the pivot point of the launcher and the user's pointer. The resulting trajectory is derived using sine and cosine functions:
```javascript
let angle = Math.atan2(pointer.y - pivotY, pointer.x - pivotX);
ball.vx = Math.cos(angle) * ball.speed;
ball.vy = Math.sin(angle) * ball.speed;
