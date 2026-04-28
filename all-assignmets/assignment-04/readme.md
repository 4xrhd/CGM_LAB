
# Lab 03: Drawing a Cyan Star on Yellow Background

**Course**  
Computer Graphics & Multimedia Lab

**Assignment**  
Lab 03

**Student**  
Name: Md. Azhar Uddin Abeer  
Student ID: 0432320005101120

**Submission Date**  
February 2025 – February 2026 (as per announcement)

## Objective

Develop a modern OpenGL application using **GLFW** and **GLAD** that:

- Displays a **yellow** window background  
- Renders exactly **one cyan star** constructed using triangles only  
- Sets the window title to the full student ID: **0432320005101120**  
- Closes the window when the user presses the key **`A`** (initial of your name)

## Requirements Fulfilled

- [x] Window background: **Yellow** (RGB: 1.0f, 1.0f, 0.0f, 1.0f)  
- [x] One **cyan star** (0.0f, 1.0f, 1.0f) drawn using `GL_TRIANGLES` only  
- [x] Window title: **0432320005101120**  
- [x] Window closes on pressing **`A`** key  
- [x] Uses **OpenGL 3.3 Core Profile** + GLFW + GLAD  
- [x] Proper VAO / VBO usage  
- [x] Clean, commented code structure  
- [x] Includes screenshot (`output.png`)

## Program Specifications

| Property              | Value                                      |
|-----------------------|--------------------------------------------|
| Window size           | 800 × 600 pixels                           |
| Background color      | Yellow (1.0f, 1.0f, 0.0f, 1.0f)           |
| Star color            | Cyan   (0.0f, 1.0f, 1.0f)                 |
| Window title          | 0432320005101120                           |
| Rendering primitive   | `GL_TRIANGLES` via `glDrawArrays`          |
| Exit key              | `A` (case insensitive in most implementations) |
| OpenGL version        | 3.3 Core Profile                           |
| Input method          | `glfwGetKey()` polling                     |

## Project Structure

```
assignment-03/
├── main.cpp          Main program (OpenGL + GLFW + GLAD)
├── glad.c            GLAD source (generated)
├── include/          Headers (glad/glad.h, glfw3.h, etc.)
├── lib/              GLFW library files (if using local build)
├── build/            Output directory for executable
├── readme.md         This file
└── output.png        Screenshot of running program
```

## Build & Run Instructions

### Linux (typical university lab environment)

```bash
mkdir -p build

g++ -Wall -std=c++17 \
    -I./include \
    main.cpp glad.c \
    -o build/star \
    -L./lib -lglfw -lGL -lX11 -lpthread -lXrandr -lXi -ldl

./build/star
```

### Windows (MinGW / MSYS2)

```bash
g++ -std=c++17 main.cpp glad.c -o star.exe \
    -Iinclude -Llib -lglfw3 -lopengl32 -lgdi32

star.exe
```

## Program Output

The application displays:

- Window title: **0432320005101120**  
- Solid **yellow** background  
- Centered **cyan star** constructed from triangles  
- No flickering or rendering artifacts

**Screenshot:**

![Program Output](output.png)  
*Screenshot showing the yellow window with cyan star and correct title bar*

## Key Techniques Implemented

- GLFW window & OpenGL 3.3 Core context creation  
- GLAD function loading  
- Minimal vertex & fragment shaders (cyan color hardcoded)  
- Single VAO + VBO for star geometry  
- Star shape built entirely from triangles (no `GL_LINES`, no fan/strip shortcuts)  
- Keyboard state checking with `glfwGetKey(GLFW_KEY_A)`  
- Clean resource deallocation (`glDeleteProgram`, `glDeleteBuffers`, `glDeleteVertexArrays`, etc.)  
- `glfwTerminate()` and window destruction on exit

## Learning Outcomes

Through this assignment, I gained practical experience with:

- Modern OpenGL setup (core profile, no fixed-function pipeline)  
- Writing and linking simple GLSL shaders  
- Vertex data management using VAO/VBO  
- Constructing complex 2D shapes from basic triangles  
- Basic real-time keyboard input handling in GLFW  
- Structuring and documenting a small graphics project

## Submission Details

- **Repository**: (to be updated with GitHub link)  
- **Files included**:
  - `main.cpp`  
  - `readme.md` (this document)  
  - `output.png` (proof of correct execution)  

**Lab Instructor**: Any Chowdhury- AC  
**Deadline**: 25 February 2026

Thank you for reviewing my submission.

Md. Azhar Uddin Abeer  
0432320005101120
