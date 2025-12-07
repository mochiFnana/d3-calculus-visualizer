# d3-calculus-visualizer
Interactive D3.js visualization exploring the function f(x) = (x/g)^2 e^{-kx}, its derivative, and the relationship between slope and tangent lines using real-time parameter controls.
# 📈 Interactive D3.js Calculus Visualizer

**A web-based tool for exploring the behavior of a parameterized exponential function and its derivative in real-time.**



---

## 💡 Project Goal

The primary goal of this project is to provide an intuitive, interactive environment for learning core calculus concepts, specifically:

1.  The **relationship between a function $f(x)$ and its derivative $f'(x)$**.
2.  The visual meaning of the **tangent line slope** as the value of the derivative.
3.  How changing **mathematical parameters ($k$ and $g$)** alters the shape of both the function and its derivative.

---

## 📐 Mathematical Context

The visualization plots two related curves:

### 1. Main Function (Red Curve)

The function being visualized combines polynomial growth and exponential decay:

$$f(x) = \left(\frac{x}{g}\right)^2 e^{-kx}$$

### 2. Derivative (Blue Curve)

The derivative represents the instantaneous slope of $f(x)$:

$$f'(x) = \frac{2x}{g^2} e^{-kx} - \frac{kx^2}{g^2} e^{-kx}$$

---

## 🚀 Usage

To run this visualization, simply open the `index.html` file in any modern web browser. No server or complex setup is required, as all dependencies (D3.js) are loaded via CDN.

### Interactive Controls

The visualization is controlled by three range sliders at the bottom of the page:

| Slider | Parameter | Effect |
| :--- | :--- | :--- |
| **Angle Slider** | **$x$** (Independent Variable) | **Highlights a point** on the red curve and draws the **tangent line**. The current $x$ and $f(x)$ values are displayed. |
| **K-Setting** | **$k$** (Decay Constant) | Adjusts the strength of the **exponential decay** ($e^{-kx}$). Higher $k$ values cause the function to return to zero faster. |
| **G-Setting** | **$g$** (Scaling Constant) | Adjusts the $\left(\frac{x}{g}\right)^2$ term. Controls the **initial rise** and the overall scaling and peak location of the function. |

---

## 🛠️ Technology Stack

* **HTML:** Structure and control placement.
* **D3.js v7:** Core library used for data binding, scaling, drawing the SVG graph, and handling all dynamic updates.
* **Vanilla JavaScript:** Logic for parameter calculation, event handling, and managing the update cycle.

---

## 🤝 Contributing

This is a personal project, but feedback and suggestions for educational improvements or refactoring are welcome!

---

**[Code for this project is entirely contained within the single `index.html` file.]**
