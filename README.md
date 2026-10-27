# 🌿 Smart Waste Segregation & Recycling System — AI Powered

## Quick Start (No Build Step Required)

This is a **single-file** application. Just open it in any modern browser:

```
File → Open → smart_waste_app.html
```

Or double-click the file in Windows Explorer. That's it — no Node.js, no npm, no build process needed.

> **Requires an internet connection** on first load to download CDN assets:
> - React 18, ReactDOM (unpkg.com)
> - Tailwind CSS (cdn.tailwindcss.com)
> - Chart.js v4.4 (cdn.jsdelivr.net)
> - Google Fonts (fonts.googleapis.com)
> - Babel Standalone (unpkg.com)

---

## Optional: Run with a Local HTTP Server

If you prefer a proper dev server (avoids any browser `file://` quirks):

```bash
# Using Python (built into Windows/Mac/Linux)
python -m http.server 3000

# Then open: http://localhost:3000/smart_waste_app.html
```

Or with Node.js (if installed):
```bash
npx serve .
# Then open: http://localhost:3000
```

---

## Features

| Section | Description |
|---|---|
| 🏠 **Hero** | Animated hero with floating icons, CTA buttons, key metrics |
| 📖 **Intro** | 4 feature cards explaining the system |
| 📊 **Dashboard** | 6 live stat cards (total, recyclable, organic, non-recyclable, CO₂, points) |
| 🔍 **AI Detection** | Drag-and-drop upload or 6 quick-demo buttons; 2s simulated AI analysis; confidence bar; bin recommendation; eco tips; points earned |
| 🗑️ **Bins** | 6 colour-coded bins (blue=plastic, yellow=paper, grey=metal, green=organic, purple=glass, red=non-recyclable); active bin glows after detection |
| 📈 **Statistics** | Doughnut chart, bar chart, line chart (Chart.js); CO₂ saved, eco points, trees equivalent |
| 🎮 **Simulation** | 8 waste items to sort individually or all at once; progress bar; 🎉 confetti on completion |
| 📋 **History** | Filterable log of all classified items; LocalStorage persistence; clear button |
| 🔔 **Toasts** | Success / info / warning / error notifications |
| 📱 **Responsive** | Works on mobile, tablet, and desktop |

---

## Waste Categories

| Category | Bin Colour | Eco Points | CO₂ Saved |
|---|---|---|---|
| 🧴 Plastic | Blue | 15 pts | 2.5 kg |
| 📄 Paper | Yellow | 10 pts | 1.2 kg |
| 🥫 Metal | Grey | 20 pts | 4.0 kg |
| 🥦 Organic | Green | 8 pts | 0.8 kg |
| 🍾 Glass | Purple | 12 pts | 1.8 kg |
| 🚫 Non-Recyclable | Red | 0 pts | 0 kg |

---

## How the Demo Classifier Works

> ⚠️ **This is an educational demo — no real AI model or hardware is connected.**

The classifier simulates AI behaviour using two signals:
1. **Filename matching** — if your image file is named `plastic_bottle.jpg`, it detects "plastic" from the filename.
2. **Fallback** — if no keyword matches, it picks a category based on the file size modulo (deterministic but pseudo-random).

A 2.2-second artificial delay simulates inference time, and a confidence score in the range 82–98% is generated randomly.

To trigger specific results, name your image files with keywords:
- `plastic`, `bottle`, `bag` → Plastic
- `paper`, `card`, `news` → Paper
- `metal`, `can`, `tin`, `alum` → Metal
- `organic`, `food`, `fruit`, `veg`, `banana` → Organic
- `glass`, `jar`, `wine` → Glass
- anything else → Non-Recyclable

---

## Tech Stack

- **React 18** — UI components and state management (via CDN, no build needed)
- **Tailwind CSS** — utility-first styling with custom eco colour palette
- **Chart.js 4.4** — doughnut, bar, and line charts for statistics
- **Babel Standalone** — JSX transpilation in the browser
- **LocalStorage** — persistent classification history
- **CSS Animations** — float, shimmer, scan-line, confetti, pulse, slide-in effects

---

## Project Structure

```
smart_waste_app.html    ← Complete application (single file)
README.md               ← This file
```

All components live inside `smart_waste_app.html`:

```
App (root)
├── Navbar
├── Hero
├── Intro
├── Dashboard
├── WasteDetection
├── BinsSection
├── Statistics
├── Simulation
├── History
├── Footer
├── Toast (notification system)
└── Confetti (celebratory animation)
```

---

## Screenshots Guide

After opening in browser you should see:
1. **Dark green hero** with animated floating emojis and two CTA buttons
2. **White intro section** with 4 feature cards
3. **Green gradient dashboard** with 6 coloured stat cards
4. **White detection section** with upload zone + 6 quick demo buttons
5. **Light green bins row** with 6 colour-coded animated bins
6. **White statistics** with 3 Chart.js charts
7. **Light green simulation** with draggable waste items and sorted bins grid
8. **White history** with filterable log table
9. **Dark green footer** with quick links

---

*© 2025 Smart Waste Segregation & Recycling System — Educational Prototype*
