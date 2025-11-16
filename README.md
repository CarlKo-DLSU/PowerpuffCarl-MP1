# QCOMP01 — MP1 (PowerpuffCarl)

Collection of four example Python programs (notebooks) demonstrating basic quantum circuits,
classical-logic reversible circuits, and small optimization tasks using Qiskit.

Files
- mp_problem1_powerpuffcarl.py — visualize state evolution for |ψ⟩ = HZH|0⟩ and produce an inline GIF.
- mp_problem2_powerpuffcarl.py — reversible implementations and validation of 3‑input XNOR, NAND, OR, NOR.
- mp_problem3_powerpuffcarl.py — find θ such that RX(θ) = X (global-phase invariant); numeric search + analytic snap.
- mp_problem4_powerpuffcarl.py — find U(θ,φ,λ) ≈ H via grid search + local optimization (Nelder–Mead).

Notes about execution environment
- mp_problem1 displays a GIF inline when executed in Jupyter/Colab. When run in a terminal it will still create the GIF in memory but may not display; you can save to disk by uncommenting the write-to-disk lines in the script.
- mp_problem2 and mp_problem3 use Statevector simulation and are deterministic; mp_problem4 runs a numeric optimizer (may take longer depending on grid settings).

Expected outputs (summary)
- mp_problem1: printed statevectors and a GIF showing the Bloch-sphere evolution.
  Example printed statevectors:
  
    |0⟩: [1.+0.j 0.+0.j]
  
    H|0⟩: [0.707107+0.j 0.707107+0.j]
  
    ZH|0⟩: [ 0.707107+0.j -0.707107+0.j]
  
    HZH|0⟩: [0.+0.j 1.+0.j]

- mp_problem2: truth tables for XNOR3, NAND3, OR3, NOR3 — all entries valid = True.

- mp_problem3: numeric theta near π then snapped to analytic θ = π + 2πk. Validation yields distance ≈ 0, action error ≈ 0, Conclusion: valid = True.

- mp_problem4: optimizer finds (θ, φ, λ) ≈ (π/2, 0, π) with distance ≈ 0 and valid = True.
