## 🚀 Lab 03: Drawing a Cyan Star with Yellow Background

### 📋 Assignment Description

Develop an OpenGL application that renders **one cyan-colored star** (constructed only with triangles) on a **yellow background**.  
The program window must display your **full student ID as the title** and should **terminate when the user presses the initial letter of your name**.

---

### ✅ Requirements Fulfilled

1. ✅ Window background is **yellow** (`RGB: 1.0, 1.0, 0.0`)
2. ✅ One **cyan-colored star** drawn using triangles
3. ✅ Window title displays **0432320005101120** (your full ID)
4. ✅ Window closes when the **initial letter of your name** (`A`) is pressed
5. ✅ Uses **GLFW + GLAD** (Modern OpenGL Core Profile)
6. ✅ Proper code structure, formatting, and comments
7. ✅ README documentation and output screenshot attached

---

### 🔧 Program Features

* **Graphics Library**: OpenGL 3.3 Core Profile
* **Window Management**: GLFW
* **Function Loader**: GLAD

**Window Properties**

* Size: `800 × 600` pixels
* Background Color: **Yellow** `(1.0, 1.0, 0.0)`
* Title: **0432320005101120**

**Rendering**

* One **cyan star** (built from triangles)
* Rendered using `glDrawArrays(GL_TRIANGLES)`
* Vertex Array Object (VAO) and Vertex Buffer Object (VBO) used

**Keyboard Interaction**

* Press **A** (your name’s initial) to close the window

**Platform**

* Linux / Windows / macOS (cross-platform)

---

### 📁 Project Structure

```
assignment-03/
├── main.cpp          # OpenGL source code
├── readme.md         # Project documentation
├── output.png        # Screenshot of program output
```

---

### 🛠️ Compilation and Execution

#### Prerequisites

* OpenGL development libraries
* GLFW
* GLAD
* C++ compiler (g++ recommended)

#### Linux Compilation

```bash
g++ main.cpp glad.c -o star -lglfw -lGL -ldl
./star
```

#### Windows (MinGW)

```bash
g++ main.cpp glad.c -o star.exe -lglfw3 -lopengl32 -lgdi32
```

---

### 📸 Screenshot Information

The attached screenshot (`output.png`) shows:

1. Successful compilation in terminal
2. OpenGL window with **yellow background**
3. One **cyan star** in the center
4. Window title displaying your **student ID**

---

### 💻 Code Implementation Details

* `glfwInit()` for window initialization
* `glfwCreateWindow()` to create a named OpenGL window
* `glClearColor(1.0f, 1.0f, 0.0f, 1.0f)` for yellow background
* Custom **vertex and fragment shaders** for cyan color
* VAO & VBO for vertex management
* `glfwGetKey()` for keyboard input handling (window closes on `A`)
* Graceful cleanup using `glDelete*()` and `glfwTerminate()`

---

### 📚 Learning Outcomes

* Drawing custom shapes (star) using triangles in OpenGL
* Shader compilation and linking
* Keyboard input handling with GLFW
* Proper OpenGL resource management
* Structuring a graphics project for academic submission

---

### 📅 Submission Details

* **Course**: Computer Graphics & Multimedia Lab
* **Lab No**: 03
* **Assignment Title**: Drawing a Cyan Star with Yellow Background
* **Submission Method**: GitHub repository link
* **Attachments**: `main.cpp` + output screenshot
* **Deadline**: As announced (No exception)


