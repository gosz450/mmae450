MMAE 450 — Homework 3 Rubric (10 Points Total)

Problem 1 — 1D FTCS Rod (4 points)
	•	1 point — Correct interior FTCS update equation
	•	1 point — Zero-flux boundary at x = 0 implemented correctly
	•	1 point — Code runs and produces midpoint temperature plot
	•	1 point — Clear demonstration of transient decay behavior

Notes for grading
	•	If zero-flux condition is treated as Dirichlet → 0 for that item
	•	If FTCS stencil is incorrect → 0 for that item

⸻

Problem 2 — Cooling of a Sphere (6 points)
	•	2 points — Correct spherical FTCS interior stencil
	•	2 points — Regularity condition at r = 0 correctly enforced
	•	1 point — Robin (convection) condition at r = R correctly implemented
	•	1 point — Stability study demonstrated (stable / near limit / unstable)

⸻

Important Grading Guidance
	•	If the regularity condition at r = 0 is incorrect, the score should not exceed 4/6.
	•	If the spherical operator is incorrect (e.g., Cartesian stencil used), the score should not exceed 4/6.