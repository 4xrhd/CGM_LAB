# Class Notes: DDA Line Drawing & OpenGL Setup

## Key Concepts

### 1. DDA (Digital Differential Analyzer) for Line Scan Conversion
- **Purpose:** Used to generate points of a line between two endpoints in computer graphics.
- **Algorithm Steps:**
	- Calculate $dx = x_1 - x_0$ and $dy = y_1 - y_0$.
	- Compute slope $m = dy/dx$.
	- If $|m| \leq 1$, increment $x$ by 1 and $y$ by $m$ each step (x is independent variable).
	- If $|m| > 1$, increment $y$ by 1 and $x$ by $1/m$ each step (y is independent variable).
	- Always draw from left to right (or bottom to top for steep lines).
	- Store each calculated $(x, y)$ as a point on the line.
- **Implementation:**
	- See the `DDA` function in `main.cpp`.
	- Returns a vector of points (x, y, z=0) for OpenGL rendering.

### 2. OpenGL Program Structure (main.cpp)
- **Window Setup:**
	- Uses GLFW for window/context creation and input handling.
	- Sets up an 800x600 window.
- **GLAD:**
	- Loads OpenGL function pointers.
- **Shaders:**
	- Simple vertex and fragment shaders for drawing white lines.
- **Vertex Data:**
	- Calls `DDA` to generate line points between $(x_0, y_0)$ and $(x_1, y_1)$ (here: $(-0.5, -0.5)$ to $(0.5, 0.5)$).
	- Stores points in a Vertex Buffer Object (VBO) and configures a Vertex Array Object (VAO).
- **Rendering Loop:**
	- Clears the screen.
	- Draws the line using `glDrawArrays(GL_LINE_STRIP, ...)`.
	- Handles window events and input.
- **Cleanup:**
	- Deletes OpenGL resources and terminates GLFW.

## Important Points to Understand
- **DDA is a simple, incremental algorithm for rasterizing lines.**
- **OpenGL requires vertex data to be sent to the GPU using VBOs/VAOs.**
- **Shaders are required for rendering in modern OpenGL.**
- **GLFW handles windowing and input; GLAD loads OpenGL functions.**

## References
- See `main.cpp` for full implementation details.
- [DDA Algorithm - Wikipedia](https://en.wikipedia.org/wiki/Digital_differential_analyzer_(graphics_algorithm))
