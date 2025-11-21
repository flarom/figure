# VRM Viewer with VRMA Animation

[English](README.md) | [日本語](README-jp.md)

A web-based VRM (Virtual Reality Model) viewer with VRMA (VRM Animation) support built using Three.js and the three-vrm library.

## 🎮 Live Demo

**[Try the Demo →](https://tk256ailab.github.io/vrm-viewer/)**


## Features

- 📱 **Responsive Design**: Works on desktop and mobile devices
- 🎭 **VRM Model Support**: Load and display VRM 1.0 models
- 🎬 **VRMA Animation**: Play custom VRMA animation files
- 🎮 **Interactive Controls**: Play, pause, and stop animations
- 🎨 **Modern UI**: Clean, gradient-based interface
- ⚡ **Fast Performance**: Optimized rendering and animations

## Demo

Open `index.html` in a web browser to see the demo. The viewer includes:

- A sample VRM model (sample.vrm)
- Eleven VRMA animation examples:
  - **Angry**: Angry emotion animation
  - **Blush**: Blushing emotion animation
  - **Clapping**: Clapping hands animation
  - **Goodbye**: Waving goodbye animation
  - **Jump**: Jumping action animation
  - **LookAround**: Looking around animation
  - **Relax**: Relaxed pose animation
  - **Sad**: Sad emotion animation
  - **Sleepy**: Sleepy emotion animation
  - **Surprised**: Surprised emotion animation
  - **Thinking**: Thinking pose animation

## Project Structure

```
vrm_viewer/
├── index.html              # Main viewer application
├── VRM/
│   └── sample.vrm     # Sample VRM model
├── VRMA/
│   ├── Angry.vrma          # Angry emotion animation
│   ├── Blush.vrma          # Blushing emotion animation
│   ├── Clapping.vrma       # Clapping hands animation
│   ├── Goodbye.vrma        # Waving goodbye animation
│   ├── Jump.vrma           # Jumping action animation
│   ├── LookAround.vrma     # Looking around animation
│   ├── Relax.vrma          # Relaxed pose animation
│   ├── Sad.vrma            # Sad emotion animation
│   ├── Sleepy.vrma         # Sleepy emotion animation
│   ├── Surprised.vrma      # Surprised emotion animation
│   └── Thinking.vrma       # Thinking pose animation
├── README.md               # This file
└── README-jp.md           # Japanese documentation
```

## Quick Start

### Method 1: GitHub Pages (Recommended)

1. **Fork or upload** this repository to GitHub
2. **Enable GitHub Pages**:
   - Go to your repository's Settings
   - Scroll down to "Pages" section
   - Under "Source", select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click "Save"
3. **Access your demo** at `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY-NAME/`

### Method 2: Local Development

1. **Clone or download** this repository
2. **Start a local web server** (required for loading files):
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve .
   
   # Using PHP
   php -S localhost:8000
   ```
3. **Open your browser** and navigate to `http://localhost:8000`
4. **Load the VRM model** (automatically loads on page load)
5. **Select animations** using the VRMA buttons
6. **Control playback** with Play, Pause, and Stop buttons

## Usage

### Loading VRM Models

The viewer automatically loads the VRM model specified in `index.html`. To use your own model:

1. Place your `.vrm` file in the `VRM/` directory
2. Update the `VRM_MODEL_URL` variable in `index.html`

### Playing VRMA Animations

1. Wait for the VRM model to load completely
2. Click any of the VRMA animation buttons to select an animation (Angry, Blush, Clapping, Goodbye, Jump, LookAround, Relax, Sad, Sleepy, Surprised, or Thinking)
3. Use the playback controls to manage animation

### Camera Controls

- **Rotate**: Left-click and drag to rotate the camera around the model
- **Pan**: Right-click and drag to move the camera horizontally/vertically
- **Zoom**: Scroll with mouse wheel to zoom in/out

### Controls

- **VRMA Animation Buttons**: Select and load different animations
- **Play**: Start or resume animation playback
- **Pause**: Pause/unpause the current animation
- **Stop**: Stop animation and reset to default pose

## Technical Details

### Dependencies

- [Three.js](https://threejs.org/) - 3D graphics library
- [@pixiv/three-vrm](https://github.com/pixiv/three-vrm) - VRM model support
- [@pixiv/three-vrm-animation](https://github.com/pixiv/three-vrm-animation) - VRMA animation support

### Animation Specifications

- **Format**: VRMA (VRM Animation) files in glTF binary format
- **Humanoid Bones**: Compatible with VRM 1.0 humanoid specification
- **Frame Rate**: 60 FPS with linear interpolation
- **Duration**: Variable (4-12 seconds for included animations)

### Browser Compatibility

- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 14+
- ✅ Edge 80+

## Customization

### Adding New Animations

1. Create or obtain VRMA animation files
2. Place them in the `VRMA/` directory
3. Update the `VRMA_ANIMATION_URLS` array in `index.html`
4. Add corresponding buttons in the HTML

### Styling

The interface uses CSS custom properties for easy theming. Key variables:

- Background colors and gradients
- Button styling and hover effects
- Control panel appearance
- Responsive breakpoints

## License

This project is for demonstration purposes. Please ensure you have appropriate rights for any VRM models and animations you use.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## Acknowledgments

- [three-vrm](https://github.com/pixiv/three-vrm) - VRM support for Three.js
- [Three.js](https://threejs.org/) - 3D graphics foundation
- VRM Consortium - VRM format specification
