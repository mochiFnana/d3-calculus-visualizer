# d3-calculus-visualizer
Interactive D3.js visualization exploring the function f(x) = (x/g)^2 e^{-kx}, its derivative, and the relationship between slope and tangent lines using real-time parameter controls.
# 🌊 D3.js Advanced Trigonometry Visualizer: The Symmetric Parameterized Cosine Wave

**An interactive, responsive web application that visualizes a complex, parameterized function, its mathematically correct derivative, and the visual concept of the tangent line.**

---

## 🎯 Project Goal

This visualization tool is designed to move beyond simple function plotting, serving as an advanced educational environment for calculus students and web developers. It allows for the real-time exploration of how external parameters affect the shape of a function and its derivative.

## ✍️ Customization: Defining Your Own Mathematical Model

The power of this project lies in its simplicity for customization. The entire mathematical model is defined by two JavaScript functions in the `<script>` block, allowing you to easily swap out the current trigonometric functions for any other differentiable function.

### How to Change the Function

To visualize a new function, $h(x)$, and its derivative, $h'(x)$:

1.  **Edit `cal(a)`:** Define the function $h(x)$. This calculates the $y$-value for the **red curve**.
2.  **Edit `dal(a)`:** Define the mathematically correct derivative, $h'(x)$. This calculates the $y$-value for the **blue curve**.

The D3.js framework will automatically handle the scaling, axis drawing, and dynamic updates based on your new definitions.

### Current Model

The project is currently configured to analyze the highly customizable **Symmetric Parameterized Cosine Wave**:

| Function | Mathematical Expression | Control |
| :--- | :--- | :--- |
| **Main Function** | $f(x) = \cos(|x|^g) + \frac{k}{2}$ | Red Curve |
| **Derivative** | $f'(x) = \frac{d}{dx} f(x)$ (Calculated via Chain Rule) | Blue Curve |

---

## ⚙️ Interactive Controls and Parameter Effects

The visualization is dynamically sized based on your screen width and controlled by four main interactive elements:

| Control | Parameter | Description |
| :--- | :--- | :--- |
| **Angle Slider** | **$x$** (Independent Variable) | **Moves the highlight point** on the curve across the defined domain (e.g., $-360^\circ$ to $360^\circ$). |
| **K-Setting** | **$k$** (Vertical Shift) | Controls the $\frac{k}{2}$ constant. Shifts both the function and its derivative **vertically**. |
| **G-Setting** | **$g$** (Exponent Power) | Controls the $|x|^g$ term (range 0 to $\pi$). Drastically changes the **wave frequency and sharpens the curve** near $x=0$. |
| **Tangent Line (Purple)** | N/A | Visually represents the instantaneous slope of $f(x)$ at the highlighted point. |

### Key Visualization Feature

A **Vertical Guide Line** connects the highlighted point on the $f(x)$ curve to the corresponding $y$-value on the $f'(x)$ curve. This visually proves that the **slope of the tangent line** on the red curve is exactly equal to the **height of the blue curve** at that $x$-position.

---

## 🛠️ Technology and Structure

* **HTML/CSS:** Minimal structure, using flexbox for control layout and responsive CSS.
* **D3.js v7:** Core library for all data binding, scaling, and SVG rendering.
* **JavaScript:** Pure vanilla JS handling all math calculations, event listeners, and performance optimization (such as dynamic screen width handling and minimizing DOM updates).
