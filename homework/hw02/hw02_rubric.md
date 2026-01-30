# MMAE 450 — Homework 2 Grading Rubric  
**Newton’s Method for Nonlinear Systems (10 points total)**

This homework assesses understanding of residual-based formulations, Jacobian construction, and Newton’s method for solving nonlinear systems, with emphasis on algorithmic clarity and numerical implementation.

---

## Problem (a): Residual Formulation (2 points)

**2 / 2**
- Correctly defines the unknown vector  
  \[
  \mathbf{T} = \begin{bmatrix} T_1 \\ T_2 \end{bmatrix}
  \]
- Correctly expresses the residual vector  
  \[
  \mathbf{R}(\mathbf{T}) = \begin{bmatrix} R_1(T_1,T_2) \\ R_2(T_1,T_2) \end{bmatrix}
  \]
- Residual components are consistent with the governing equations.

**1 / 2**
- Minor issues in notation or clarity, but residual equations are essentially correct.

**0 / 2**
- Residual formulation is incorrect or missing.

---

## Problem (b): Jacobian Matrix (2 points)

**2 / 2**
- Jacobian matrix is computed correctly.
- Partial derivatives are correct and clearly associated with the residual components.
- Analytical or symbolic approach is clearly documented.

**1 / 2**
- Jacobian structure is correct but contains a minor algebraic error, or explanation is unclear.

**0 / 2**
- Jacobian is incorrect, missing, or not related to the residual formulation.

---

## Problem (c): Newton Iteration Statement (2 points)

**2 / 2**
- Correctly writes the Newton linear system  
  \[
  \mathbf{J}(\mathbf{T}^{(k)}) \, \Delta \mathbf{T}^{(k)} = -\mathbf{R}(\mathbf{T}^{(k)})
  \]
- Correctly states the update rule  
  \[
  \mathbf{T}^{(k+1)} = \mathbf{T}^{(k)} + \Delta \mathbf{T}^{(k)}
  \]
- Clearly connects the algebraic system to the algorithmic iteration.

**1 / 2**
- Newton system or update is mostly correct but missing clarity or precision.

**0 / 2**
- Newton iteration is incorrect or omitted.

---

## Problem (d): Numerical Implementation (3 points)

**3 / 3**
- Newton solver implemented correctly using NumPy.
- Uses a relative residual convergence criterion as specified.
- Reports:
  - Converged solution \((T_1, T_2)\)
  - Number of Newton iterations
- Code is logically organized and readable.

**2 / 3**
- Solver works but has minor issues (e.g., convergence check slightly incorrect, weak reporting, or unclear structure).

**1 / 3**
- Partial implementation with significant issues.

**0 / 3**
- No meaningful Newton solver implementation.

---

## Problem (e): Convergence Behavior (1 point)

**1 / 1**
- Correct plot of relative residual norm versus iteration number.
- Brief and reasonable commentary on convergence behavior (e.g., quadratic convergence).

**0 / 1**
- Plot missing, incorrect, or no discussion provided.

---

## Presentation and Organization (Expectation)

Students are expected to submit a single, well-organized Jupyter notebook with:
- Clear problem setup
- Clearly labeled sections
- Clean plots and readable output

Poor organization may result in point deductions within individual categories.
