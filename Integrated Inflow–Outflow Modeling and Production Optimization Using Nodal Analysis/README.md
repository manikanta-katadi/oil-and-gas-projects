# Physics-Guided Nodal Analysis and Production Optimization of Oil Wells

## Overview

This project implements a physics-based nodal analysis framework to evaluate and optimize oil well production by coupling reservoir inflow performance (IPR) with wellbore outflow performance (TPR).

Unlike conventional academic implementations, this project extends nodal analysis with **decision-making and optimization logic** to identify optimal operating conditions such as tubing size, wellhead pressure, and artificial lift requirements.

---

## Problem Statement

In oil and gas production, determining the optimal operating condition of a well is critical for maximizing production while minimizing operational inefficiencies.

Engineers must balance:

* Reservoir deliverability (IPR)
* Wellbore lifting constraints (TPR)
* Surface operating conditions (WHP)
* Artificial lift requirements

This project simulates these interactions and provides **data-driven engineering decisions** for production optimization.

---

## Technical Approach

### 1. Inflow Performance Relationship (IPR)

* Modeled using **Vogel’s equation**
* Calculates reservoir deliverability and Absolute Open Flow (AOF)

### 2. Tubing Performance Relationship (TPR)

* Modeled using:
  [
  P_{wf} = P_{wh} + aq + bq^2
  ]
* Captures:

  * Hydrostatic pressure losses
  * Frictional losses

### 3. Nodal Analysis

* Numerical intersection of IPR and TPR curves
* Determines:

  * Operating flow rate
  * Bottomhole flowing pressure

---

Key Features
✅ Physics-based IPR modeling using Vogel correlation
✅ TPR modeling including hydrostatic and frictional effects
✅ Integrated nodal analysis (IPR–TPR coupling)
✅ Sensitivity analysis:
Tubing size optimization
Wellhead pressure optimization
✅ Reservoir depletion modeling
✅ Artificial lift (gas lift) simulation
✅ Decision-making layer for engineering recommendations

---

## Decision & Optimization Logic

This project goes beyond visualization by implementing **engineering decision logic**:

*  Automatically identifies **optimal tubing size** for maximum production
*  Determines **optimal wellhead pressure (WHP)**
*  Evaluates whether **gas lift is required**
*  Quantifies **percentage improvement in production**

---

## 📈 Key Results & Insights

* Larger tubing significantly reduces friction losses and increases production rate
* Increasing wellhead pressure reduces production due to higher backpressure
* Reservoir depletion reduces both pressure and deliverability (AOF)
* Gas lift improves production by reducing hydrostatic pressure
* Optimization logic shows production improvements of ~5–15% depending on conditions

---

## Tech Stack

* Python
* NumPy
* Matplotlib

---

## How to Run

```bash
pip install numpy matplotlib
python main.py
```

---

## Project Structure

```
├── step1_ipr.py
├── step2_tpr.py
├── step3_nodal.py
├── step4_sensitivity.py
├── step5_optimization.py
└── README.md
```

---

## Future Improvements (Industry-Level)

* 🔹 Integration with real field production data
* 🔹 Multi-well optimization and field-level modeling
* 🔹 Economic analysis (NPV, cost vs production optimization)
* 🔹 Machine learning models for production prediction
* 🔹 Interactive dashboards using Plotly / Streamlit

---

## Conclusion

This project demonstrates how physics-based modeling combined with numerical methods can be used to optimize oil well performance. By incorporating decision-making logic, it bridges the gap between academic concepts and real-world petroleum engineering applications.

---

### Author

**Mani Kanta**  
Petroleum Engineering  
IIT (ISM) Dhanbad

---

