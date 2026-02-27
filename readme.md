# 🎨 CGM_LAB - Computer Graphics and Multimedia Lab

Welcome to the **Computer Graphics and Multimedia (CSE 358)** lab repository. This project contains a series of lab exercises and assignments focused on modern OpenGL (3.3 Core Profile) and real-time graphics rendering.

---

## � Repository Information
- **Course**: CSE 358: Computer Graphics and Multimedia
- **Semester**: Spring 2026
- **Student Name**: Md. Azhar Uddin Abeer
- **Student ID**: 0432320005101120
- **Section**: 5B2

---

## 🛠️ Tech Stack & Prerequisites
This project is built using:
- **Language**: C++17
- **Graphics API**: Modern OpenGL 3.3 (Core Profile)
- **Window Management**: [GLFW](https://www.glfw.org/)
- **OpenGL Loader**: [GLAD](https://glad.dav1d.de/)
- **Compiler**: GCC / G++ (Linux) or MinGW (Windows)

### Linux Dependencies
To run these labs on Ubuntu/Debian, install the following:
```bash
sudo apt-get update
sudo apt-get install build-essential libglfw3-dev libgles2-mesa-dev libx11-dev libxcursor-dev libxinerama-dev libxrandr-dev libxi-dev libgl1-mesa-dev libglu1-mesa-dev libxext-dev
```

---

## 📂 Project Structure
```text
CGM_LAB/
├── all-assignmets/        # Comprehensive list of course assignments
│   ├── assignment-01/     # Window creation & background colors
│   ├── assignment-02/     # Basic shapes (Triangles) & Shaders
│   └── assignment-03/     # Complex shapes (Star) & Input handling
├── lab0/                  # Initial setup and hello-world examples
├── lab3/                  # Detailed lab on Drawing a Cyan Star
└── readme.md              # Project overview (this file)
```

---

## 🚀 Lab & Assignment Index

### [Assignment 01: Hello Window](all-assignmets/assignment-01/)
- **Objective**: Initialize GLFW, load GLAD, and create a basic OpenGL window.
- **Key Features**: Sky blue background, Student name as window title.

### [Assignment 02: Triangle Geometry](all-assignmets/assignment-02/)
- **Objective**: Introduction to VAO, VBO, and GLSL Shaders.
- **Key Features**: Renders two cyan obtuse triangles on an orange background.

### [Assignment 03: The Cyan Star](all-assignmets/assignment-03/)
- **Objective**: Construct complex 2D geometry using only triangles.
- **Key Features**: Renders a yellow window with a cyan star. Closes on 'A' key press.

---

## 🔨 How to Build and Run
Each assignment directory contains its own `Makefile` or build instructions. Generally, you can compile using:

```bash
g++ -Wall -std=c++17 -I./include main.cpp glad.c -o build/app -lglfw -lGL -lX11 -lpthread -lXrandr -lXi -ldl
./build/app
```

---

## ⚖️ Academic Integrity Statement
This work is original and created solely for educational purposes as part of the **CSE 358** coursework. All code has been developed and tested by the student whose information is provided above.

---
*Created with ❤️ by Azhar*
