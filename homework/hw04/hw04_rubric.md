# MMAE 450 — Homework 04 Rubric (10 Points Total)

## 1️⃣ Grid and Stability Verification (3 points)

- **1 point** — Correct computation of Δx and Δy  
- **1 point** — Correct computation of Δt satisfying  
  α Δt (1/Δx² + 1/Δy²) ≤ 1/2  
- **1 point** — Explicit stability check printed (η value shown and ≤ 1/2)

**Grading guidance**
- If stability condition is violated → maximum score 6/10  
- If no stability check shown → 0 for that item  

---

## 2️⃣ Correct FTCS Implementation (3 points)

- **2 points** — Correct interior FTCS stencil (2D form including both x and y second derivatives)  
- **1 point** — Dirichlet boundary conditions enforced at every time step  

**Grading guidance**
- If stencil incorrect → maximum score 5/10  
- If boundaries not enforced each step → 0 for boundary item  

---

## 3️⃣ Contour Plots at Required Times (2 points)

- **2 points** — Contour plots produced at  
  t = 0, 10, 50, 200 s  
  using consistent contour levels or consistent color scale  

**Grading guidance**
- Missing one required time → 1 point  
- Missing multiple required times → 0 points  

---

## 4️⃣ Center-Point Temperature History (1 point)

- **1 point** — Correct plot of T(0.5, 0.25, t) versus time  

---

## 5️⃣ Maximum Temperature and Cooling Metric (1 point)

- **1 point** — Plot of Tmax(t) and correct computation/reporting of  
  first time t₁₀% such that Tmax < 10°C  

---

## Important Notes

- No half points awarded.  
- If FTCS formula is incorrect → cap at 5/10.  
- If Dirichlet BCs are not enforced properly → cap at 7/10.  
- If stability condition is violated → cap at 6/10.
