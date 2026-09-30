# DEC-ACSA: Dynamic Elite Cooperative Artificial Circulatory System Algorithm

### Definition

DEC-ACSA is an improved metaheuristic optimization algorithm inspired by the **human circulatory system**. It extends the Artificial Circulatory System Algorithm (ACSA) through **diversity-aware dynamic population grouping**, **elite-guided cooperative interaction**, and **directional elite refinement** to improve convergence stability and the use of high-quality population information.

The algorithm was used to:

- Estimate the **five unknown parameters of the photovoltaic Single-Diode Model (SDM)**.
- Minimize the **residual Root Mean Square Error (RMSE)** of the implicit SDM equation.
- Compare performance against **five algorithms**: ACSA, PSO, GWO, GA, and HGSO.
- Evaluate estimation accuracy, convergence behavior, run-to-run variability, parameter sensitivity, and computational cost.
- Reconstruct **current–voltage (I–V) characteristics** using the identified parameters.

This repository provides the **Python implementation** of DEC-ACSA, introduced in the paper *“Metaheuristic-Based Photovoltaic Parameter Identification Using a Dynamic Elite Cooperative Artificial Circulatory System Algorithm.”*

### Key Features

- **Bio-Inspired Framework:** Builds on the neural–hormonal regulation mechanisms of ACSA.
- **Dynamic Population Grouping:** Adjusts neural, hormonal, and elite group proportions according to search progress and population diversity.
- **Elite-Guided Cooperation:** Guides hormonal individuals toward randomly selected members of the current elite set.
- **Directional Elite Refinement:** Combines the global best solution, elite difference vectors, and a rank-weighted elite centroid.
- **Bound-Constrained Search:** Repairs candidates to satisfy parameter bounds and applies greedy selection.
- **Evaluation-Based Termination:** Controls computational effort through a fixed function-evaluation budget.
- **Photovoltaic Parameter Identification:** Estimates photocurrent, reverse saturation current, series resistance, shunt resistance, and diode ideality factor.
- **Configuration Transfer:** Uses the configuration selected on RTC France unchanged on three additional PV module benchmarks.

### Benchmark Validation

DEC-ACSA was evaluated on **four established photovoltaic benchmarks** using **30 independent runs** and an equal budget of **50,100 function evaluations** per run.

| Benchmark | PV System | Mean Residual RMSE |
|---|---|---:|
| RTC France | Solar cell | 1.2514 × 10⁻³ |
| PWP201 | PV module | 2.656 × 10⁻³ |
| STM6-40/36 | PV module | 2.647 × 10⁻³ |
| STP6-120/36 | PV module | 1.8108 × 10⁻² |

DEC-ACSA achieved the lowest mean residual RMSE among the evaluated algorithms on all four benchmarks and reduced run-to-run variability relative to the original ACSA.

After Holm correction, differences from PSO were **not statistically significant** on RTC France and PWP201. On STM6-40/36 and STP6-120/36, differences from all five comparison algorithms were statistically significant.

The identified parameter sets produced reconstructed I–V curves closely matching the measured data. These results apply to the four investigated SDM benchmarks and their measurement conditions.

### Publication

Full details of the algorithm and experimental evaluation are available in:

- **Title:** Metaheuristic-Based Photovoltaic Parameter Identification Using a Dynamic Elite Cooperative Artificial Circulatory System Algorithm
- **Authors:** Nermin Özcan and Imam Barket Ghiloubi
- **Journal:** Engineering Proceedings
- **Publisher:** MDPI
- **Year:** 2026
- **Volume:** 152
- **Article Number:** 4
- **DOI/Link:** [10.3390/engproc2026152004](https://doi.org/10.3390/engproc2026152004)
- **Conference:** 1st International Online Conference on Inventions—Energy Security and Sustainable Development, 25–26 June 2026

### Citation Request

If you use DEC-ACSA in your research, please cite the following paper:

```bibtex
@article{Ozcan2026DECACSA,
  title     = {Metaheuristic-Based Photovoltaic Parameter Identification Using a Dynamic Elite Cooperative Artificial Circulatory System Algorithm},
  author    = {{\"O}zcan, Nermin and Ghiloubi, Imam Barket},
  journal   = {Engineering Proceedings},
  volume    = {152},
  number    = {1},
  pages     = {4},
  year      = {2026},
  publisher = {MDPI},
  doi       = {10.3390/engproc2026152004},
  url       = {https://doi.org/10.3390/engproc2026152004}
}
```
