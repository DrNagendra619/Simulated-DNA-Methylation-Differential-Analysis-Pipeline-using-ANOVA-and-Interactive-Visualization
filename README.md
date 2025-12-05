# Simulated-DNA-Methylation-Differential-Analysis-Pipeline-using-ANOVA-and-Interactive-Visualization
Simulated DNA Methylation Differential Analysis Pipeline using ANOVA and Interactive Visualization
# Simulated DNA Methylation Differential Analysis Pipeline using ANOVA and Interactive Visualization 🧬📊

A comprehensive Python-based pipeline for simulating and performing differential DNA methylation analysis. This project utilizes standard bioinformatics tools (`pandas`, `statsmodels`) and features advanced interactive visualization using `Plotly` to enhance data exploration and result interpretation.

## 🌟 Project Overview

This repository contains a Jupyter Notebook (`Simulated_DNA_Methylation_Differential_Analysis_Pipeline_using_ANOVA_and_Interactive_Visualization.ipynb`) that demonstrates a complete workflow for identifying differentially methylated CpG sites between two simulated groups (e.g., Control vs. Disease).

The pipeline covers:
1.  **Data Simulation:** Creating a controlled, synthetic dataset.
2.  **Exploratory Data Analysis (EDA):** Utilizing advanced plots (Heatmaps, PCA) to visualize overall sample clustering and data quality.
3.  **Statistical Analysis:** Implementing one-way **ANOVA** for site-specific differential methylation testing.
4.  **Interactive Visualization:** Generating a **Volcano Plot** and individual site plots for robust interpretation of results.

## 🚀 Key Features

* **Interactive Plots (Plotly):** All major visualizations (Heatmap, PCA, Volcano Plot, Box Plots) are interactive, allowing for zooming, hovering over data points for details (e.g., CpG ID, Beta Value), and dynamic exploration.
* **Dimensionality Reduction:** Includes **Principal Component Analysis (PCA)** to visually confirm that group differences are the primary source of variance in the dataset.
* **Differential Methylation (DM) Metrics:** Calculates both **P-values** (statistical significance) and **Delta Beta** (magnitude of change) for robust DM calling.
* **Quality Control (QC):** Provides global and site-specific quality checks to ensure data integrity and distribution assumptions.

## 🛠️ Prerequisites

To run this pipeline, you need Python and the following libraries. The notebook automatically installs them using `!pip install`.

| Package | Purpose |
| :--- | :--- |
| `pandas`, `numpy` | Data manipulation and numerical operations. |
| `matplotlib`, `seaborn` | Basic plotting utilities. |
| `statsmodels` | Statistical modeling (ANOVA). |
| `plotly`, `plotly.express` | **Interactive visualization.** |
| `scikit-learn` | Principal Component Analysis (PCA). |

## 📦 Installation and Setup

1.  **Clone the Repository:**
    ```bash
    git clone [Your-GitHub-Repository-URL]
    cd [Your-Repository-Name]
    ```
2.  **Run the Notebook:**
    Open the `Simulated_DNA_Methylation_Differential_Analysis_Pipeline_using_ANOVA_and_Interactive_Visualization.ipynb` file in a Jupyter environment (e.g., JupyterLab, VS Code, or Google Colab).
3.  **Execute Cells:** Run all code cells sequentially. The first cell will handle the package installation.

## 📋 Pipeline Workflow & Interpretation

The notebook is divided into logical cells, each performing a distinct step:

| Cell | Title | Action Performed | Key Insight (from Simulated Data) |
| :--- | :--- | :--- | :--- |
| **Cell 3** | **Interactive EDA** | Generates Heatmap and **PCA Plot**. | **PCA showed clear separation** between Control and Disease samples along PC1, validating the simulated effect.  |
| **Cell 4** | **Data Formatting & QC** | Converts data to long format. Generates a global interactive **Box Plot**. | Confirmed a global shift towards **higher mean beta values** (hypermethylation) in the Disease group. |
| **Cell 5** | **Statistical Analysis** | Runs **ANOVA** per CpG site and calculates **Delta Beta** and `-Log10 P-Value`. | Generated the statistical metrics needed for the Volcano Plot. |
| **Cell 6** | **Interactive Volcano Plot** | Plots significance vs. fold change. | Highlighted **`CpG_6`** as the most differentially methylated site, showing both high significance and large positive Delta Beta (hypermethylation).  |
| **Cell 7** | **Plot Significant CpGs** | Zooms into significant sites using Strip/Box plots. | Visually confirmed the **clear separation** of beta values for `CpG_6` between Control and Disease. |

## 🖼️ Example Visualization

The **Volcano Plot** is the definitive visualization for omics data, combining both the magnitude and statistical significance of the change.

**Interpreting the Volcano Plot (Cell 6):**
* **Y-axis ($\mathbf{-Log_{10}\ P-Value}$):** The higher the point, the more statistically significant the CpG site. The dashed line marks the significance threshold (e.g., Bonferroni-corrected $\alpha=0.05$).
* **X-axis ($\mathbf{\Delta Beta}$):**
    * **Points on the Right ($\Delta \beta > 0$):** Hypermethylated in Disease (Increased methylation).
    * **Points on the Left ($\Delta \beta < 0$):** Hypomethylated in Disease (Decreased methylation).

---

## ✍️ Author

[Dr Nagendra]
