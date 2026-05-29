# Additive Manufacturing & Topology Optimization Project

This repository contains the final report and design stages for the **ME463 Additive Manufacturing** course project. The objective of this project is to investigate and practically implement topology optimization (TO) and lattice structures on three different load-bearing mechanical components to minimize weight while preserving structural integrity.

<div align="center">
  <img src="https://github.com/user-attachments/assets/b546a6e9-2fc6-4efe-a78f-a6d25fa572b9" width="500">
</div>

---

## 🛠️ Software & Methodology
* **nTop:** Used to define design domains, material properties, implicit field modeling, and advanced configurations (lattice infills).
* **Finite Element Analysis (FEA):** Utilized to evaluate initial structural response and validate final optimized geometries.
* **Post-Processing:** Applied surface smoothing (Laplacian/implicit) and critical feature thickening to ensure dimensional accuracy and manufacturability.

---

## ⚙️ Case Studies

### 1. Marine Anchor Fairlead
* **Objective:** Maximize the stiffness-to-mass ratio and eliminate underutilized low-stress zones.
* **Material:** 316L Stainless Steel ($E = 200 \text{ GPa}$).
* **Loading Scenario:** Subjected to heavy line tension ($1 \times 10^6 \text{ N}$ operational load) and lateral rope forces calculated at a conservative $30^\circ$ vessel heel angle.
* **Optimization Strategy:** * Volume fraction target set to `0.35`.
  * Integrated an internal **Gyroid lattice core** inside a topologically optimized uniform shell ($15\text{ mm}$ thickness).
  * Critical interfaces (base plate and assembly holes) were protected using Boolean keep-out zones to ensure safe load transfer to the deck.

### 2. Automotive Steering Knuckle
* **Objective:** Reduce unsprung mass to improve steering precision and vehicle dynamics while handling multi-axial operational loads.
* **Material:** Changed from conventional mild steel to 316L Stainless Steel for additive manufacturing compliance ($E = 200 \text{ GPa}$).
* **Boundary Conditions:** Modeled based on a $1400\text{ kg}$ vehicle chassis (distributed symmetrically as $350\text{ kg}$ per wheel):
  * **Braking Force:** $1.5\text{mg}$
  * **Lateral Force:** $1.5\text{mg}$
  * **Hub Forces:** $3\text{mg}$ (X and Y axes), $1\text{mg}$ (Z axis)
* **Optimization Strategy:** Handled complex overlapping load cases and localized stress concentrations with a volume fraction constraint of `0.35` and a precise `0.5 mm` smoothing grid.

### 3. Aerospace Drone Body (Airframe)
* **Objective:** Minimize structural vibration and avoid catastrophic resonance caused by high-speed motor excitation.
* **Material:** Carbon Fiber Reinforced Polymer (CFRP) via FFF ($E = 10 \text{ GPa}$, $\text{Density} = 3000 \text{ kg/m}^3$).
* **Vibrational Targets:** Shifting the natural frequency away from the **20,000 RPM ($333.3 \text{ Hz}$)** motor excitation frequency. Target threshold set to $>330 \text{ Hz}$.
* **Results:** * Initial geometry baseline frequency: $885.5 \text{ Hz}$ (with motor arms acting as weak cantilevers).
  * Topologically optimized design achieved a safe final natural frequency of **$778.04 \text{ Hz}$**, fully exceeding the target and ensuring sensor stability.

---

## 📌 Conclusion
The project successfully demonstrates that topology optimization is not a replacement for traditional engineering judgment, but a powerful extension of it. By leveraging computational design toolsets, the final parts achieved massive mass reductions while maintaining optimal stress and vibrational responses within standard safety thresholds.

---

## 👥 Authors
* Burak ŞAHİN
* Berrin Nur VURAL


Here is our final report:
[ME463_Project final.pdf](https://github.com/user-attachments/files/28390889/ME463_Project.final.pdf)
