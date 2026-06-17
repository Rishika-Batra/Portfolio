# Cyberpunk Storytelling Portfolio — Rishika Batra

A premium, interactive single-page portfolio landing page crafted with modern frontend technologies. It features a custom 3D Canvas-based skeleton plexus globe, a velocity-responsive magnetic cursor, and scroll-driven storytelling animations.

---

## 🎨 Key Features

1. **3D Skeleton Plexus Globe**
   - **Performance-First Design**: Rendered entirely on a lightweight HTML5 `<canvas>` element (zero WebGL context overhead or dependencies).
   - **Fibonacci Lattice Distribution**: Spaced 135 vertices uniformly across a 3D sphere using the golden spiral algorithm.
   - **Stable Edge Network**: Precomputes and connects neighboring nodes to form a stable geodesic skeleton structure.
   - **Depth Projection & Painter's Algorithm**: Rotates vertices in 3D space, sorts them by depth ($Z$-coordinate), and dynamically updates styling (translucent cyan lines, glowing pink points, variable line widths, and glowing drop-shadows) to create an immersive 3D illusion.
   - **Smooth LERP Physics**: Smooths scrolling movements by interpolating the rotation angles using Linear Interpolation (LERP) with a `0.08` dampening factor, combined with continuous slow auto-rotation.

2. **Premium Velocity Cursor**
   - **Organic Inertia**: Custom cursor ring that follows mouse coordinates with a smooth lag.
   - **Velocity Stretching**: Dynamically squashes and stretches the outer ring into an oval shape matching the direction and speed of mouse movement.
   - **Interactive States**: Snaps to elements on hover (expanding and showing a soft neon pink fill), pauses color cycles, and shifts colors organically on idle.

3. **Fluid Layout & Scroll Animation**
   - Driven by **GSAP** and **ScrollTrigger** over a structured `400vh` scroll height.
   - The globe smoothly glides horizontally (`-18vw` to `+16vw`), tilts, and fades to sit behind call-to-action cards as the scroll progresses.
   - Background typographic nodes glide and scale proportionally to create a deep, layered parallax landscape.

4. **Iridescent Cyberpunk Color Scheme**
   - Built on a deep black canvas (`#000008`) with highly saturated neon accents:
     - Hot Pink (`#FF0090`)
     - Electric Cyan (`#00F0FF`)
     - Fire Orange (`#FF4500`)
     - Acid Lime (`#AAFF00`)
     - Deep Violet (`#8800FF`)

---

## 🛠️ Technology Stack

- **Structure**: Semantic HTML5 markup
- **Styling**: Tailwind CSS (loaded via CDN) & custom variables
- **Logic**: Vanilla ES6+ JavaScript
- **Animations**: GSAP 3 & GSAP ScrollTrigger
- **Graphics**: HTML5 2D Canvas (3D projection mathematics)

---

## 📂 Project Structure

```bash
portfolio/
├── index.html   # Main entry point (HTML, CSS, JS and 3D Canvas engine)
└── README.md    # Documentation
```

---

## 🚀 Getting Started

### Prerequisites

You only need a modern web browser to open the file. To prevent any local file sharing security flags from blocking external CDNs, it is recommended to run the project using a simple local HTTP server.

### Running Locally

1. **Using Python**:
   Run the following command in your terminal inside the project directory:
   ```bash
   python -m http.server 8000
   ```
   Open `http://localhost:8000` in your web browser.

2. **Using Node.js (npx)**:
   ```bash
   npx serve .
   ```
   Open the address provided by `serve` in your web browser.

3. **Direct Open**:
   Alternatively, double-click or drag `index.html` into any web browser.
