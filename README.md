# AnantBoard

AnantBoard is a lightweight, web-based drawing application built as a single HTML file, designed for quick sketching, note-taking, and creative expression. It leverages Fabric.js for canvas manipulation, providing an intuitive interface with essential drawing tools, dark mode, infinite zoom/pan, and export capabilities. As a Progressive Web App (PWA), it supports offline use and can be installed on devices for a native app-like experience.

## Features

- **Drawing Tools**: Freehand pen tool with customizable color (via color picker) and brush thickness (1-50px via slider).
- **Eraser**: Dedicated eraser tool that paints with the current background color for seamless removal.
- **Pan Mode**: Hand tool for navigating the canvas; also activated by holding Alt key during drag.
- **Dark Mode**: Toggle between light and dark themes; automatically inverts existing strokes and adjusts brush colors for consistency.
- **Infinite Zoom & Pan**: Mouse wheel zoom (limited to 0.01x to 20x) with smooth panning; zoom resets temporarily for export.
- **Export**: Download drawings as high-resolution PNG images (multiplier: 2x for crisp output).
- **Auto-Save**: Real-time saving to browser localStorage on every stroke or modification; restores on page reload.
- **PWA Support**: Installable as a standalone app; includes install prompt and manifest for offline access.
- **Responsive Design**: Adapts to window resize; full-screen canvas with floating toolbar.

## Installation and Setup

### Basic Usage
1. Download or clone the repository.
2. Open `anantBoard.html` directly in any modern web browser (Chrome, Firefox, Safari, Edge recommended for full PWA support).
3. Start drawing immediately—no server or additional setup required.

### PWA Installation
AnantBoard is designed as a PWA for offline functionality:
- **On Mobile (Android/iOS)**: Visit the page in your browser; an install prompt may appear automatically. Alternatively, tap the "⬇ App" button in the toolbar when it appears.
- **On Desktop**: Use your browser's install option (e.g., Chrome's "Install AnantBoard" in the address bar) or click the "⬇ App" button.
- **Offline Access**: Once installed, the app works without internet, with drawings saved locally.

### Requirements
- Modern browser with ES6+ support.
- Internet connection for initial load (Fabric.js is loaded from CDN).
- No dependencies beyond the browser; all code is self-contained in the HTML file.

## How It Works

AnantBoard operates as a single-page application:
- **Canvas Setup**: Uses Fabric.js Canvas with drawing mode enabled by default.
- **Brushes**: PencilBrush for drawing/eraser; eraser matches background color dynamically.
- **Event Handling**: Mouse events for drawing, panning, and zooming; keyboard shortcuts (Alt for pan).
- **State Management**: LocalStorage for persistence; dark mode state and canvas JSON data.
- **PWA Features**: Service worker-ready (via manifest); install prompt triggered by browser events.
- **Performance**: Efficient rendering with Fabric.js; zoom/pan optimized for smooth interaction.

## Usage Guide

1. **Select Tools**: Click toolbar buttons to switch modes (Pen, Eraser, Pan).
2. **Customize Brush**: Use color picker for hue and slider for size.
3. **Draw/Erase**: Click and drag on canvas; eraser removes strokes by overwriting.
4. **Navigate**: Zoom with mouse wheel; pan by dragging in Pan mode or Alt+drag.
5. **Toggle Themes**: Click moon icon to switch dark/light mode (inverts canvas and strokes).
6. **Export Work**: Click camera icon to download PNG; zoom resets for full-canvas capture.
7. **Clear Canvas**: Click trash icon (with confirmation) to reset; dark mode toggles twice to restore background.
8. **Persistence**: Drawings auto-save; reload page to resume.

## Technologies Used

- **HTML5 Canvas**: Core drawing surface.
- **CSS3**: Floating toolbar with backdrop blur; responsive, dark-mode styles.
- **Vanilla JavaScript**: All logic, event handling, and PWA integration.
- **Fabric.js (v5.3.1)**: Advanced canvas library for paths, brushes, and object manipulation.
- **PWA Manifest**: Defines app metadata for installation and theming.

## Contributing

Contributions are welcome! Fork the repo, make changes, and submit a pull request. Focus areas: performance optimizations, new tools, or accessibility improvements.

## License

This project is open-source under the MIT License. Feel free to use, modify, and distribute.
