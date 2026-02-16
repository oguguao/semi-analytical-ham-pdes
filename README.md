# Semi-Analytical HAM PDE Codes

**Author:** Ogugua N. Onyejekwe, PhD  
**Repository:** semi-analytical-ham-pdes  

---

## 📘 Overview

This repository contains MAPLE and MATLAB implementations supporting the monograph:

> **Semi-Analytical Solutions of Classical Free Boundary PDEs Using HAM with MAPLE and MATLAB**  
> Ogugua N. Onyejekwe, 2026.

The codes implement the Homotopy Analysis Method (HAM) for classical Stefan-type free-boundary partial differential equations (PDEs), including both one-dimensional and two-dimensional benchmark problems.

The primary objective of this repository is **full reproducibility** of the semi-analytical workflow developed in the book.

---

## ✨ Key Features

- Timewise determination of the convergence-control parameter \( h(t) \)  
- Interface reconstruction from the HAM solution field  
- Relative error validation for both the field variable and moving boundary  
- MAPLE symbolic pipeline → MATLAB numerical verification  
- Support for source and convection extensions  
- Extension from 1D to 2D Stefan-type problems  

---

## 📂 Repository Structure


Each example in the book has corresponding scripts for reproducibility.

---

## 🧮 Software Requirements

### MAPLE

- MAPLE 2020 or later recommended  
- Symbolic capabilities required  
- `Student[Calculus1]` package used in several scripts  

### MATLAB

- MATLAB R2020a or later recommended  
- Standard numerical environment sufficient  
- No specialized toolboxes required  

---

## 🚀 How to Reproduce Results

### Step 1 — MAPLE (Symbolic Stage)

1. Open the corresponding MAPLE worksheet/script.  
2. Run the HAM recursion to generate:
   - \( u_m(x,t) \)  
   - truncated solution \( u_{\mathrm{HAM}}^{(N)} \)  
3. Solve for the convergence-control parameter \( h(t_j) \).  
4. Solve for the reconstructed interface \( s_{\mathrm{HAM}}(t_j) \).  

---

### Step 2 — MATLAB (Numerical Stage)

1. Run the matching MATLAB script.  
2. The code will:
   - evaluate over the prescribed time grid  
   - compute relative errors  
   - generate verification plots  
3. Tables in the book should be reproducible to machine precision.  

---

## 📊 Error Metrics

Consistent with the book methodology, only relative errors are reported:

\[
\mathrm{RelErr}_u, \quad \mathrm{RelErr}_s.
\]

Maximum relative error metrics are intentionally not used.

---

## 🔬 Methodological Notes

Throughout the repository:

- The auxiliary function is fixed as  
  \[
  \mathcal{H}(x,t) = 1.
  \]

- The moving boundary is **not directly deformed**.

- The convergence-control parameter is determined **timewise** via pointwise matching.

- Complex-valued branches of \( h(t) \) are retained when required for consistency.

These choices follow the unified framework developed in the associated monograph.

---

## 📖 Citation Request

If you use these codes in your research, please cite:

> Onyejekwe, O. N.,  
> *Semi-Analytical Solutions of Classical Free Boundary PDEs Using HAM with MAPLE and MATLAB*,  
> 2026.

---

## ⚖️ License

This project is licensed under the **MIT License**.

You are free to use, modify, and distribute the code with proper attribution.

---

## 🤝 Contact

**Dr. Ogugua N. Onyejekwe**  
oguguao@yahoo.com

For questions or collaboration inquiries, please open a GitHub issue.

---

## ⭐ Acknowledgment

This repository accompanies ongoing research on semi-analytical methods for moving-boundary problems and is intended to support transparent and reproducible computational mathematics.
