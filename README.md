# 🎮 Praxo Render Engine

A lightweight 3D **render engine** written in **C++** with **OpenGL**. It focuses on real-time rendering and comes with a fly-through camera, an in-engine UI built with Dear ImGui, object picking and transform gizmos, real-time lighting, texture import and a built-in console.

> It is a rendering project, not a full game engine: there is no physics, audio or scripting system.

![Language](https://img.shields.io/badge/C%2B%2B-17-00599C?logo=cplusplus&logoColor=white)
![OpenGL](https://img.shields.io/badge/OpenGL-3.3%20Core-5586A4?logo=opengl&logoColor=white)
![Platform](https://img.shields.io/badge/platform-Windows-0078D6?logo=windows&logoColor=white)
![Status](https://img.shields.io/badge/status-in%20development-orange)

## ✨ Features

- **3D rendering** with OpenGL 3.3 Core (cube, pyramid and light-source objects)
- **Free-fly camera** with keyboard movement and mouse look
- **Object picking**: click an object in the scene to select it (ray / oriented-box intersection)
- **Transform gizmos** (ImGuizmo): move, rotate and scale the selected object
- **Lighting**: ambient, diffuse and specular, with an adjustable light color
- **Materials**: solid color, two-color gradient, or an imported texture
- **Texture import** (`.png`, `.jpg`) through a file dialog
- **Editor UI** (Dear ImGui): shader panel, texture panel, and a scene-object list
- **Built-in console** that captures engine output and accepts commands

## 🎛 Controls

| Action                  | Input                     |
| ----------------------- | ------------------------- |
| Move forward / back     | `W` / `S`                 |
| Move left / right       | `A` / `D`                 |
| Move up / down          | `Space` / `Left Ctrl`     |
| Move faster             | Hold `Left Shift`         |
| Look around             | Hold **Right Mouse Button** |
| Select an object        | **Left click** on it, or pick it from the list |
| Gizmo: translate        | `T`                       |
| Gizmo: rotate           | `G`                       |
| Gizmo: scale            | `H`                       |

### Console commands

| Command     | Description                      |
| ----------- | -------------------------------- |
| `clear`     | Clears the console               |
| `Debug`     | Debug message                    |
| `StopDebug` | Restores standard output         |

## 🛠 Tech Stack

| Purpose            | Library                                  |
| ------------------ | ---------------------------------------- |
| Language           | C++17                                    |
| Graphics API       | OpenGL 3.3 Core                          |
| Window & input     | [GLFW](https://www.glfw.org/)            |
| OpenGL loader      | [GLAD](https://glad.dav1d.de/)           |
| Math               | [GLM](https://github.com/g-truc/glm)     |
| UI                 | [Dear ImGui](https://github.com/ocornut/imgui) |
| Gizmos             | [ImGuizmo](https://github.com/CedricGuillemet/ImGuizmo) |
| File dialog        | [ImGuiFileDialog](https://github.com/aiekick/ImGuiFileDialog) |
| Image loading      | [stb_image](https://github.com/nothings/stb) |
| IDE / Toolset      | Visual Studio 2022 (MSVC v143)           |

## 🚀 Getting Started

**Requirements:** Windows 10 or 11 and [Visual Studio 2022](https://visualstudio.microsoft.com/) with the **Desktop development with C++** workload.

1. **Clone the repository**

   ```bash
   git clone https://github.com/Khaledabdsalame/Praxo-Game-Engine.git
   ```

2. **Open** `Praxo Game Engine.sln` in Visual Studio.

3. **Check the include and library paths.** The project file currently points to absolute paths (`C:\Users\lenovo\source\repos\Praxo Game Engine\include` and `...\lib`). Change them to your own clone location in:
   *Project → Properties → VC++ Directories* (and *C/C++ → Additional Include Directories*).

4. Select the **Debug | x64** configuration and press **F5**.

> Run the engine from the project folder so it can find the `Shaders/Glsl` files and other assets.

## 📂 Project Structure

```
├── Buffers/          # VAO, VBO and EBO wrappers
├── Models/           # Vertex data for built-in shapes
├── Shaders/          # Shader class and GLSL files (Glsl/)
├── Textures/         # Texture loading and binding
├── imgui/            # Dear ImGui, ImGuizmo and ImGuiFileDialog
├── include/          # Headers: GLM, GLAD, GLFW, stb
├── lib/              # Libraries (glfw3.lib)
├── test/             # Experiments and tests
├── Camera.cpp / .h   # Fly camera, mouse picking, ray intersection
├── Console.cpp / .h  # In-engine console
├── Rendere.cpp       # Entry point: window, render loop and editor UI
├── glad.c            # OpenGL loader
└── Praxo Game Engine.sln
```

## 🤝 Contributing

Contributions are welcome. Fork the repository, create a feature branch, commit your changes and open a Pull Request.

## 📄 License

[MIT License](https://choosealicense.com/licenses/mit/).

## 👤 Author

**Khaled Abdsalame** · [GitHub](https://github.com/Khaledabdsalame)
