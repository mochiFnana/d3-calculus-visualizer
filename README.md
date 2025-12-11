# 🚀 D3.js Symbolic Function and Derivative Visualizer (Math.js Integrated)

**The ultimate interactive, screen-responsive tool for visualizing any user-defined function, its mathematically supplied derivative, and the concept of the tangent line slope in real-time.**

## 🎯 Project Goal: The Mathematical Laboratory

This project has been transformed into a fully customizable educational environment using the **`math.js`** library for symbolic evaluation. Instead of editing JavaScript source code, users can now input and plot *any* differentiable function and its derivative directly on the web page.

The goal is to provide a complete, interactive tool for:

1.  **Symbolic Definition:** Defining and instantly visualizing custom mathematical equations.
2.  **Calculus Verification:** Proving the derivative relationship by observing if the slope of the main function ($f(x)$) matches the $y$-value of the derivative ($f'(x)$).

## ✍️ The Customization Engine (Symbolic Input)

The visualization is controlled directly by the two text areas on the screen. The entire chart will redraw based on the functions you define in these inputs.

### 1. Function Input Fields

| Input Field | Defines | Purpose | Action Required |
| :--- | :--- | :--- | :--- |
| **Y-Input** (`f(a, k, g)`) | The **Main Function** ($f(a)$) | Plots the **Red Curve**. | Enter your function expression here. |
| **Derivative Input** (`f'(a)`) | The **Derivative** ($f'(a)$) | Plots the **Blue Curve**. | Enter the mathematically correct derivative of your Y-Input here. |
| **APPLY NEW FUNCTIONS** | N/A | Parses the new input strings, recompiles the math using `math.js`, and regenerates the graph data. | **Must be clicked** after making changes to the text areas. |

### 2. Available Variables

Your input expressions can use the following variables, which are dynamically controlled by the sliders:

| Variable | Description | Controlled by | Example Use |
| :--- | :--- | :--- | :--- |
| **`a`** | The **Independent Variable** ($x$). | Angle Slider | `a^2`, `sin(a)` |
| **`k`** | The **K-Setting** constant. | K-Setting Slider | `a^2 + k` |
| **`g`** | The **G-Setting** constant. | G-Setting Slider | `g * a` |

### 3. Custom Functions & Syntax

* **Trigonometry:** All built-in trig functions (`cos`, `sin`, `tan`) are automatically set to accept **degrees** (matching the slider input) instead of the default radians.
* **Conditionals:** You can use the custom `if(condition, true_value, false_value)` function for piecewise or absolute value definitions.
    * *Example:* To get the sign of `a`: `if(a, a/abs(a), 0)`

---

## ⚙️ Core Visualization Features

| Feature | Description | Mathematical Concept |
| :--- | :--- | :--- |
| **Tangent Line (Purple)** | Visually represents the slope of the $f(a)$ curve at the current point. | Instantaneous Rate of Change |
| **Vertical Guide Line** | Connects the highlight point on $f(a)$ to the corresponding $y$-value on $f'(a)$. | **Verification:** The slope of the tangent line is equal to the height of the derivative curve. |
| **Dynamic Scaling** | The Y-axis (domain) automatically adjusts to fit the minimum and maximum values of the two custom functions you input. | Data Visualization & Fitting |

---

## 🛠️ Technology and Structure

* **Core Engine:** **`math.js`** for symbolic parsing and evaluation.
* **Visualization:** **`D3.js v7`** for efficient SVG drawing, data binding, and dynamic axis scaling.
* **Design:** Fully responsive chart width, utilizing screen space efficiently.
