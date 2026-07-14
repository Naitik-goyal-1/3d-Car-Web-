# 3D-Cars 
# 🏎️ 3D Cars Viewer & Customizer
- [Watch DEMO](https://leonid-yakovlev-car-preview.netlify.app/)
An interactive 3D WebGL application showcasing highly detailed car models, built with **React**, **Three.js**, and **React Three Fiber (R3F)**. The app features real-time lighting, shadows, studio environment mapping, post-processing, and smooth OrbitControls rotation for a premium showroom experience.
1)copy repo
2)npm i
3)npm run dev
🌐 **[Live Demo](https://leonid-yakovlev-car-preview.netlify.app/)**
---
## ✨ Features
- **🚗 Multiple Car Models**: Select and view various detailed 3D sports cars including:
  - Ferrari SF90 Stradale
  - Lamborghini Huracán, SVJ, and Gallardo
  - BMW M3, M4, i8, and Legend
  - Porsche Taycan
  - Nissan GT-R
- **🎮 Interactive Showroom**:
  - Full 360° camera rotation restricted to realistic showroom angles using `OrbitControls`.
  - Automatic model rotation on the Y-axis.
  - Realistic contact shadows (`ContactShadows`) under the car.
- **💡 Professional Studio Lighting**:
  - Configured with `Environment` and several rectangular `Lightformer` elements to simulate a photo studio box.
  - High-intensity light ring reflection on the car paint.
- **✨ Post-Processing Effects**:
  - Real-time `Bloom` post-processing for neon/glowing light reflections.
  - Performance-optimized depth buffer settings.
- **📊 Real-time Performance Monitor**: Built-in stats window for tracking frames per second (FPS) and rendering performance.
---
## 🛠️ Tech Stack
- **React** (v18)
- **Three.js** (WebGL 3D Library)
- **React Three Fiber** (React wrapper for Three.js)
- **@react-three/drei** (Useful helpers for R3F)
- **@react-three/postprocessing** (Post-processing effects)
- **CSS3** (Styling & Layout)
---
## 📁 Project Structure
```text
├── public/                 # Static assets (3D GLB Models & LUT texture)
│   ├── bmw-1.glb to bmw-4.glb
│   ├── ferrari_2021.glb
│   ├── lambo-1.glb to lambo-3.glb
│   ├── nissan.glb
│   ├── porshe.glb
│   ├── F-6800-STD.cube     # Color Look-Up Table (LUT)
│   └── index.html
├── src/
│   ├── index.js            # Entry point & Main canvas/scene setup
│   ├── models.js           # GLTF Loader & Model rotation logic
│   ├── effects.js          # Bloom & post-processing settings
│   └── style.css           # UI & layout styling
├── package.json            # Scripts & dependencies
└── README.md               # Documentation (this file)
```
---
## 🚀 Getting Started
### Prerequisites
Make sure you have [Node.js](https://nodejs.org/) installed on your machine.
### Installation
1. Clone or download the repository:
   ```bash
   git clone <repository-url>
   cd 3D-Cars-main
   ```
2. Install the project dependencies:
   ```bash
   npm install
   ```
### Running Locally
To start the development server:
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser to view the application.
### Building for Production
To create a production-ready build of the application:
```bash
npm run build
```
This builds the application for production to the `build` folder. It correctly bundles React in production mode and optimizes the build for the best performance.
---
## 🎨 Asset Credits
- 3D models (`.glb` files) are served statically from the `public` directory.
- Studio environment lights and reflection maps are configured dynamically using `@react-three/drei`'s `<Lightformer />`.
