# Linear Regression — Cost Function

Implementation and visualization of the **Mean Squared Error (MSE) cost function** for
Linear Regression, built from scratch in Python using **NumPy** and **Matplotlib** —
no machine-learning frameworks involved.

The goal is to build intuition for how the cost function `J(w, b)` measures the fit
of a straight-line model, and why its shape is what makes gradient descent work
reliably for linear regression.

---

## What's inside

| File | Description |
|---|---|
| [`C1_W1_Lab03_Cost_function.ipynb`](./C1_W1_Lab03_Cost_function.ipynb) | Self-contained, runnable notebook: data, cost function implementation, and both static and interactive visualizations. |
| [`Cost_Function_Report.pdf`](./Cost_Function_Report.pdf) | A written report explaining the underlying concepts (linear model, cost equation, convexity) alongside the generated plots. |
| `LICENSE` | MIT License. |

---

## Key concepts covered

- **Linear model:** `f(w, b)(x) = w·x + b`
- **Cost function (MSE):**

  ```
  J(w, b) = (1 / 2m) · Σ [ f(w, b)(x⁽ⁱ⁾) − y⁽ⁱ⁾ ]²      for i = 0 … m−1
  ```

- **Cost intuition:** how `J(w, b)` changes as `w` sweeps across a range of values,
  with `b` held fixed.
- **Cost surface:** how `J(w, b)` varies across *both* parameters at once, shown as
  a contour plot.
- **Convexity:** why the squared-error cost surface for linear regression is a smooth
  "bowl" with a single global minimum — the reason gradient descent converges reliably
  for this problem.

---

## Notebook features

- Pure NumPy implementation of `compute_cost(x, y, w, b)`.
- Static plots (always render, no extra setup needed):
  - Candidate model lines vs. cost curve.
  - Contour plot of `J(w, b)`.
  - 3D convex cost surface.
- **Optional interactive widgets** (via `ipywidgets`) that let you drag `w` and `b`
  sliders and watch the model fit and the cost update live. These degrade gracefully
  with a plain message if `ipywidgets` isn't installed, so the notebook still runs
  top to bottom either way.

---

## Getting started

### 1. Clone the repository

```bash
git clone https://github.com/EngHasanSrour/linear-regression-cost-function.git
cd linear-regression-cost-function
```

### 2. Install dependencies

```bash
pip install numpy matplotlib jupyter ipywidgets
```

### 3. Run the notebook

```bash
jupyter notebook C1_W1_Lab03_Cost_function.ipynb
```

Run all cells top to bottom — every plot is self-contained and requires no external
data or helper files.

---

## Example output

The notebook produces plots similar to the ones below (see the report for the full,
annotated versions):

- **Cost vs. `w`** — a parabola with a single minimum.
- **Contour plot of `J(w, b)`** — concentric level curves converging on the
  lowest-cost point.
- **3D cost surface** — a convex "soup bowl" shape.

---

## Tech stack

- Python 3
- NumPy
- Matplotlib
- ipywidgets *(optional, for the interactive cells)*
- Jupyter Notebook

---

## License

This project is licensed under the [MIT License](./LICENSE).

## Author

**Hasan Srour**
Freelance data & document specialist · Electrical & Electronic Circuits student, Al-Aqsa University

- GitHub: [@EngHasanSrour](https://github.com/EngHasanSrour)
