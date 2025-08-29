# AR Card Game (ARCardGame)

An augmented reality card game project based on MindAR.js and A-Frame, enhancing traditional card game interactions through AR technology.

## 🎯 Project Introduction

This project utilizes MindAR.js image recognition technology to combine traditional card games with augmented reality. Players can scan specific target cards to see 3D models and related image content in the real world, creating an immersive gaming experience.

## ✨ Main Features

- **Multi-target Recognition**: Supports simultaneous recognition of multiple different target cards
- **3D Model Display**: Each target card corresponds to a unique 3D model
- **Dynamic Image Display**: Each target also contains related 2D image content
- **Interactive Scaling**: 
  - Desktop: Mouse wheel scaling
  - Mobile: Two-finger pinch scaling
- **Responsive Design**: Adapts to desktop and mobile devices
- **Real-time AR Rendering**: Real-time augmented reality experience based on WebXR technology

## 🛠️ Technical Architecture

- **Frontend Framework**: A-Frame 1.2.0
- **AR Engine**: MindAR.js
- **3D Model Format**: GLB/GLTF
- **Image Recognition**: MindAR image target detection
- **Responsive Interaction**: Custom A-Frame components

## 📁 Project Structure

```
ARCardGame/
├── index.html          # Main page file
├── targets.mind        # MindAR target configuration file
├── models/             # 3D models folder
│   ├── model0.glb      # First 3D model
│   ├── model1.glb      # Second 3D model
│   └── model2.glb      # Third 3D model
├── img/                # Original image resources
│   ├── 11.png
│   ├── 22.png
│   └── 33.png
├── imgPresent/         # Display image resources
│   ├── chair.jpg       # Chair image
│   ├── light.jpg       # Lamp image
│   └── sofa.jpg        # Sofa image
└── README.md           # Project documentation
```

## 🚀 Quick Start

### Requirements

- Modern browser (supports WebXR)
- HTTPS-enabled server environment (AR features require secure context)
- Camera permission

### Installation Steps

Method A:
Direct link: https://newsunny2004.github.io/ARCardGame/

Method B:
1. **Clone Project**
   ```bash
   git clone [project address]
   cd ARCardGame
   ```

2. **Start Local Server**
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Or using Node.js
   npx http-server -p 8000
   
   # Or using PHP
   php -S localhost:8000
   ```

3. **Access Application**
   - Open `http://localhost:8000` in browser
   - Allow camera permission
   - Prepare target cards for scanning

## 🎮 Usage

### Basic Operations

1. **Start AR Experience**
   - After opening the webpage, the system will automatically request camera permission
   - After allowing permission, the AR scene will begin initializing

2. **Scan Target Cards**
   - Point the camera at target cards
   - The system will automatically recognize and display corresponding 3D models and images

3. **Interactive Operations**
   - **Desktop**: Use mouse wheel to scale 3D models
   - **Mobile**: Use two-finger pinch gestures to scale 3D models

### Target Card Description

- **Target 0**: Displays model2.glb 3D model + chair.jpg image
- **Target 1**: Displays model0.glb 3D model + light.jpg image  
- **Target 2**: Displays model1.glb 3D model + sofa.jpg image

## 🔧 Custom Configuration

### Adding New 3D Models

1. Place GLB files in the `models/` folder
2. Add resource references in the `<a-assets>` section of `index.html`
3. Create corresponding target entities

### Changing Target Images

1. Place new images in the appropriate folder
2. Modify the `src` attribute of `<a-image>` tags
3. Adjust position, size, and other parameters

### Modifying Target Count

1. Update the `maxTrack` attribute of the `mindar-image` component
2. Add or delete corresponding target entities
3. Update the `targets.mind` configuration file

## 📱 Compatibility

- **Desktop Browsers**: Chrome 79+, Firefox 72+, Safari 13+
- **Mobile Browsers**: iOS Safari 13+, Chrome Mobile 79+ (Mobile Safari only supports desktop websites)
- **AR Support**: Requires WebXR-capable devices

## 🐛 Common Issues

### Q: Camera cannot start
A: Ensure HTTPS protocol is used and allow browser camera permission

### Q: 3D models not displaying
A: Check if model file paths are correct and ensure GLB file format compatibility

### Q: Target recognition not accurate
A: Ensure target cards are clearly visible with adequate lighting and avoid reflections

### Q: Mobile performance issues
A: Reduce model complexity, optimize image sizes, and disable unnecessary features

## 🙏 Acknowledgments

- [MindAR.js](https://github.com/hiukim/mind-ar-js) - AR image recognition engine
- [A-Frame](https://aframe.io/) - WebVR/AR framework
- [Three.js](https://threejs.org/) - 3D graphics library

---

**Note**: This project requires camera permission and HTTPS environment to run AR features normally.
