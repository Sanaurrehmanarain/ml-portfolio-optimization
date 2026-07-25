<div align="center">
  <a href="ProjectReport.pdf">
    <img src="pm2.png" alt="banner" width="100%">
  </a>
  <p><em>Click the banner to view the full analysis report</em></p>
</div>

# 📈 Portfolio Optimization via Machine Learning

## 📝 Overview
This repository contains a comprehensive, mathematical approach to modern portfolio management, transitioning from traditional asset allocation (Kelly Criterion) to advanced machine learning methodologies. The project proves how ML algorithms can fundamentally solve standard portfolio flaws—such as estimation error and extreme concentration—yielding superior out-of-sample risk-adjusted returns.

## 🚀 Key Features & Methodologies
* **Constrained Kelly Optimization:** Implemented SLSQP optimization to maximize expected geometric growth ($\max E[\ln(1 + w^T R)]$) while enforcing strict risk-mandate constraints (max 20% weight per asset).
* **K-Fold Cross-Validation:** Built a non-stationary financial backtesting framework (5-Fold CV) to rigorously evaluate regime-dependent systemic risks.
* **Marčenko-Pastur Denoising:** Utilized Random Matrix Theory and eigenvalue decomposition to filter out estimation error/noise from empirical correlation matrices.
* **Matrix Detoning:** Extracted the dominant market eigenvector to isolate idiosyncratic relative-value asset relationships.
* **Hierarchical Risk Parity (HRP):** Replaced traditional Markowitz quadratic programming with graph theory/clustering algorithms (Recursive Bisection & Quasi-Diagonalization) to allocate capital without requiring matrix inversion.

## 📊 Results Summary
The methodologies were tested on a diverse portfolio of 10 mega-cap equities using real market data. The dataset was split into an In-Sample training period (Jan 2024 - Sep 2025) and an Out-of-Sample testing period (Q4 2025). 

The empirical results proved that sequencing ML methodologies (**Denoising $\rightarrow$ Detoning $\rightarrow$ Clustering**) strictly outperformed traditional baselines:
* **Higher Returns:** ML HRP generated higher Out-of-Sample returns (3.84%) compared to Standard HRP (3.39%).
* **Superior Risk-Adjusted Profile:** ML HRP improved the Sharpe Ratio to **1.34** (an ~18% increase over standard methods).
* **Downside Protection:** Achieved the shallowest Maximum Drawdown (-4.50%) and lowest Expected Shortfall, mathematically proving that ML filtering provides highly stable capital preservation during regime shifts.

## 🛠️ Project Structure
* `project_notebook.ipynb` - The central Jupyter Notebook containing all data extraction, optimizations, ML mathematical functions, and plotting algorithms.
* `oos_performance_comparison.png` - Out-of-Sample metric visualizations.
* `Report.docx/pdf` - A formal, 30+ page deep-dive analysis containing mathematical proofs, methodology justifications, and APA 7 citations.
* `TASKS.md` - A breakdown of the project requirements and assignment parameters.

## Citation

If you use this project in academic research, publications, educational
materials, or derivative works, please cite the project.

This repository includes a `CITATION.cff` file, so GitHub provides a
**"Cite this repository"** button in the repository sidebar. You can use it
to obtain citations in BibTeX, APA, and other supported formats.

**Suggested citation:**

Arain, S. U. R. (2026). ml-portfolio-optimization (Version 1.0) [Software].
<https://github.com/sanaurrehmanarain/ml-portfolio-optimization>

**Author:** Sana Ur Rehman Arain

**Profession:** Data Scientist

**GitHub:** <https://github.com/sanaurrehmanarain>

**Contact:** <sana.arain.work@gmail.com>

If you build upon this work, attribution is appreciated and helps others
discover the original project.

> **Note:** The MIT License requires that the original copyright
> notice be retained in copies of the Software.

---

## License

This project is licensed under the MIT License. See the
[LICENSE](LICENSE) file for details.