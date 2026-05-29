# Luxury Dark Cinematic Web Developer Portfolio

A production-grade, single-page professional portfolio website crafted for **Shubham S Karabantnal** — Full-Stack Web Developer & UI/UX Enthusiast.

The design utilizes a **Luxury Dark Cinematic Cyberpunk** aesthetic, creating a premium product-launch visual feel. It features sharp editorial typography, hardware-accelerated fluid simulations, glassmorphism card layouts, repeating film scanlines, and an ambient background noise texture reminiscent of high-end Apple or Stripe launch pages.

---

## 💎 Design & Interactive Highlights

### 1. WebGL Fluid Simulation & Trailing Cursor
- **SplashCursor Engine**: Built on a native WebGL fluid dynamics solver mapped inside an absolute canvas layer. Swiping or clicking sweeps vibrant neon currents that disperse dynamically over the UI.
- **Branded Colors**: Configured to cycle randomly between the portfolio's custom-selected neons: **Neon Cyan (`#00F0FF`)** and **Neon Pink (`#FF2E93`)**.
- **LERP Circular Cursor**: A hardware-accelerated custom circle follows the cursor utilizing linear interpolation (LERP), styled with a `mix-blend-mode: difference` contrast inversion effect when hovering over interactive elements.
- **Passthrough Layout**: Set up at `z-index: 40` with `pointer-events: none` to guarantee all interactive cards, links, and buttons remain fully clickable.

### 2. Double-Video Fullscreen Sticky Hero
- **Double-Layer Depth**: Plays a forefront high-definition video loop, backed by a duplicated absolute canvas layer blurred heavily (`filter: blur(60px) scale(1.25)`) at `50%` opacity to cast a rich backing ambient field.
- **Scroll-to-Mute Optimization**: Uses an `IntersectionObserver` to automatically silence video tracks when the hero section scrolls out of view, preserving system memory and processor power.
- **Floating Controls**: Features a responsive glassy audio button pill in the bottom right corner with a pulsing scroll helper badge designed to grab user attention.

### 3. Tactical Filmic Gradients & Scanlines
- **Inline SVG Turbulence**: Maps a high-performance SVG noise filter over a fixed fullscreen overlay, lending a premium tactical film grain texture to every scrolling section.
- **Vignette & Scanlines**: Repetitive linear gradients emulate film scanlines at a subtle `3%` opacity overlay.

---

## 🛠️ Technology Stack

- **Core**: HTML5, Vanilla JavaScript (ES6+), WebGL, GLSL Shaders
- **Styling**: Modern CSS3 (CSS Variables, Grid, Flexbox, Scroll-Driven Animations)
- **Local Dev Server**: Vite (Hot Module Replacement)
- **Icons & Assets**: Devicons, FontAwesome CDN

---

## 📂 Project Structure

```
Portfolio/
├── index.html          # Core Single-Page Portfolio Layout & Shaders
├── package.json        # Node Scripts & Dev Dependencies (Vite)
├── package-lock.json   # Package Lock
├── vite.config.js      # Vite Configuration
├── README.md           # Documentation & Customization Guide
├── Assets/             # Videos, Images, & Profile Icons
│   └── Use_the_uploaded_image_as_the.mp4  # Cinematic Loop Video
```

---

## 🚀 Getting Started & Local Development

### Prerequisites
Make sure you have [Node.js](https://nodejs.org/) installed on your machine.

### Installation
1. Navigate to the project root directory:
   ```bash
   cd Portfolio
   ```
2. Install local development dependencies:
   ```bash
   npm install
   ```

### Run Locally
Start the local hot-reloading development server:
```bash
npm run dev
```
Open the printed local host link in your browser (usually `http://localhost:5173`).

### Production Build
Build a highly optimized production bundle:
```bash
npm run build
```
Vite will compile and compress all assets inside the `dist/` directory, ready for rapid hosting on platforms like Vercel, Netlify, or GitHub Pages.

---

## 🎨 Easy Customization Guide

All variables and configurations are structured neatly in [index.html](file:///Users/shubham/Documents/Portfolio/index.html).

### 1. Customizing Colors
To alter the primary accents or ambient glows, navigate to the `:root` pseudo-class in the HTML `<style>` section and change the HSL variables:
```css
:root {
  --bg: #080A0F;
  --surface: #0E1117;
  --accent: #00F0FF;       /* Neon Cyan Primary */
  --accent-warm: #FF2E93;  /* Neon Pink Secondary */
}
```

### 2. Tweaking Fluid Physics
Locate `(function initSplashCursor() { ... })()` near the bottom of the HTML script block. You can change velocity or dissipation rates:
```javascript
let config = {
  DENSITY_DISSIPATION: 3.5,  // Color fade rate
  VELOCITY_DISSIPATION: 2.0, // Swirl dissipation rate
  CURL: 3.0,                 // Swirling force strength
  SPLAT_RADIUS: 0.25,        // Splat spray radius
};
```

---

## 📄 License & Credits

- Created & Owned by **Shubham S Karabantnal** &copy; 2025.
- Shaders adapted from open-source React Bits `<SplashCursor />` designs.
