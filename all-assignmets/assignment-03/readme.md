
# Lab 03: Drawing a Cyan Star on Yellow Background

**Course:** Computer Graphics & Multimedia Lab  
**Assignment No:** 03  
**Student ID:** 0432320005101120  
**Name:** Md. Azhar  
**Submission Date:** February 2026

## 🎯 Objective

Create a modern OpenGL application (using GLFW + GLAD) that displays:

- A bright **yellow background**  
- One **cyan-colored star** constructed only using triangles  
- Window title shows the full student ID  
- Pressing the first letter of your name (`A`) closes the window

## ✅ Requirements Checklist

- [x] Window background color: **Yellow** (RGB: 1.0, 1.0, 0.0)  
- [x] One cyan star drawn using **only triangles** (`GL_TRIANGLES`)  
- [x] Window title = **0432320005101120**  
- [x] Press **A** key → window closes  
- [x] Uses **OpenGL 3.3 Core Profile** + GLFW + GLAD  
- [x] Clean code structure with meaningful comments  
- [x] Includes README and screenshot of output

## 🖥️ Program Specifications

| Property              | Value                              |
|-----------------------|------------------------------------|
| Window size           | 800 × 600 pixels                   |
| Background color      | Yellow (1.0f, 1.0f, 0.0f, 1.0f)   |
| Window title          | 0432320005101120                   |
| Star color            | Cyan (0.0f, 1.0f, 1.0f)            |
| Rendering method      | `glDrawArrays(GL_TRIANGLES, ...)`  |
| Input handling        | GLFW keyboard callback / polling   |
| Exit condition        | Press **A** key                    |
| Graphics API          | OpenGL 3.3 Core Profile            |

## 📁 Project Structure

```
assignment-03/
├── main.cpp       # Main OpenGL program
├── glad.c         # GLAD loader (generated)
├── include/       # glad/glad.h, GLFW headers
├── lib/           # glfw library files (if needed)
├── readme.md      # This documentation
└── output.png     # Screenshot of running program
```

## 🛠️ How to Build and Run

### Linux (most common academic environment)

```bash
g++ -Wall -std=c++17 \
    -I./include \
    main.cpp glad.c \
    -o build/star \
    -L./lib -lglfw -lGL -lX11 -lpthread -lXrandr -lXi -ldl

./build/star
```

### Windows (MinGW / MSYS2)

```bash
g++ main.cpp glad.c -o star.exe -Iinclude -Llib -lglfw3 -lopengl32 -lgdi32
star.exe
```

## 📸 Program Output Description

The running application shows:

- Window title bar: **0432320005101120**
- Complete yellow background
- Centered **cyan star** made of triangles
- Clean rendering without artifacts

(Refer to attached file: `output.png`)

## 💡 Key Implementation Techniques Used

- GLFW window and context creation (OpenGL 3.3 Core)
- GLAD for loading modern OpenGL functions
- Simple vertex + fragment shaders (cyan hard-coded)
- Single VAO + VBO to store star vertices
- Star geometry created using **triangles only** (no lines or strips)
- Real-time keyboard polling with `glfwGetKey()`
- Proper resource cleanup (`glDelete…`, `glfwDestroyWindow`, `glfwTerminate`)

## 📚 Learning Outcomes

By completing this lab, I practiced and understood:

- Setting up modern OpenGL pipeline (3.3+ Core)
- Writing minimal vertex & fragment shaders
- Creating and rendering geometry using VBO/VAO
- Building complex shapes (star) from basic triangles
- Handling basic window events and keyboard input
- Organizing a small graphics project properly

## 📌 Submission Information

- **Repository**: (link will be provided)
- **Files included**:
  - `main.cpp`
  - `readme.md`
  - `output.png` (screenshot showing window + title + star)

<img src="output.png">

- **Lab Instructor**: -AC
- **Deadline**: 25-FEB-2026

Thank you.

Md. Azhar  Uddin Abeer
0432320005101120
```

