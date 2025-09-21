# KAGE Soft3D – Wireframe Renderer  

**KAGE Soft3D** is the **software rendering module** of the **KAGE 1.0 Game Engine**.  
It implements a minimal **3D graphics pipeline** from scratch using Python, NumPy, and Pygame — no OpenGL, DirectX, or shaders required.  

This component projects and animates a **rotating 3D cube** in real-time, serving as the foundation of the rendering system in **KAGE 1.0**.  

---

## Features  

- Part of **KAGE 1.0 Game Engine**  
- CPU-based **3D → 2D projection system** (no GPU shaders)  
- **Wireframe rendering** of a cube  
- Real-time **rotation around X, Y, Z axes** using matrix math  
- Runs at a smooth **60 FPS** with Pygame  

---

## How It Works  

### 1. 3D Model (Cube)  
The cube’s **8 vertices** are defined in 3D coordinates.  

### 2. Transformation Pipeline  
- Rotation matrices (X, Y, Z) update the cube’s orientation.  
- A **projection matrix** reduces 3D → 2D coordinates.  
- Coordinates are scaled and centered in the Pygame window.  

### 3. Rendering  
- Vertices are drawn as **red points**.  
- Edges are connected with **black lines**.  
- Creates a continuous **rotating wireframe cube**.  

---

##  Installation & Running  

### Requirements  
- Python 3.8+  
- Pygame  
- NumPy  

### Install dependencies  

```bash
pip install pygame numpy
```
Run
```
python main.py
```
### Controls

ESC → Quit program

Cube rotates automatically

### Is This a Shader?

No.
This module is a software 3D renderer, not a GPU shader.

All math is handled on the CPU (via NumPy).

Rendering is done with Pygame’s 2D drawing functions.

Shaders (in OpenGL/DirectX) run on the GPU — this is the software equivalent for learning and prototyping.

#### Roadmap for KAGE
This module lays the groundwork for more advanced KAGE features:

## Wireframe rendering (this project)

⬜ Perspective projection (depth, FOV)

⬜ Camera movement & view matrices

⬜ Hidden surface removal (Z-buffer)

⬜ Basic lighting & shading models

⬜ Transition to GPU-accelerated rendering in KAGE 2.0

### License

MIT License.




