# Physical Activity and Lung Cancer Risk: A Meta-Analysis Replication & Extension

## Overview

This project replicates and extends the systematic review and meta-analysis by [Qie et al. (2023)](https://doi.org/10.1016/j.jncc.2022.12.003), published in the *Journal of the National Cancer Center*, which examined the association between physical activity and lung cancer risk across 42 cohort studies (~10 million participants, ~86,000 lung cancer cases).

Study-level data were extracted visually from the published forest plots (Figures 2 and 4) to reconstruct the input dataset. The same statistical methods (fixed-effects and random-effects meta-analytic models) were then applied to verify that our pooled estimates closely match the published values. Once replication was confirmed, additional diagnostic and sensitivity analyses were performed to extend the original work.

Reports are available in both **English** and **French**.

## 📊 View the rendered reports

- **English**: [meta_analysis_report_en.html](https://killianfoubert.github.io/meta-analysis-lung-cancer/meta_analysis_report_en.html)
- **Français**: [meta_analysis_report_fr.html](https://killianfoubert.github.io/meta-analysis-lung-cancer/meta_analysis_report_fr.html)

## What this project demonstrates

* **Data extraction** from published forest plots to reconstruct study-level datasets
* **Meta-analysis** using inverse-variance weighted fixed-effects and random-effects (REML) models
* **Heterogeneity assessment** (Cochran's Q, I² statistic)
* **Publication bias diagnostics** (funnel plots with significance contours, Begg's rank test, Egger's regression, trim-and-fill correction)
* **Sensitivity analyses** (leave-one-out influence analysis, cumulative meta-analysis by publication year, multi-panel influence diagnostics)

## Key findings (replicated)

| PA Type | Pooled RR | 95% CI | Interpretation |
| --- | --- | --- | --- |
| Total PA (high vs. low) | 0.78 | 0.70–0.86 | 22% risk reduction |
| Leisure-time PA (high vs. low) | 0.88 | 0.83–0.93 | 12% risk reduction |
| Occupational PA (high vs. sitting) | 1.12 | 0.98–1.29 | No significant association |

## Project structure

```
meta-analysis-lung-cancer/
├── README.md
├── lung-cancer-meta-analysis.Rproj
├── meta_analysis_report_en.Rmd       # Full analysis report (English)
├── meta_analysis_report_en.html      # Rendered report (English)
├── meta_analysis_report_fr.Rmd       # Full analysis report (French)
├── meta_analysis_report_fr.html      # Rendered report (French)
├── assets/
│   ├── styles.css                    # Editorial design styling
│   ├── hero_en.html                  # English hero section
│   └── hero_fr.html                  # French hero section
└── data/
    ├── study_data_tpa.csv            # Total PA: extracted study data
    ├── study_data_ltpa.csv           # Leisure-time PA: extracted study data
    └── study_data_opa.csv            # Occupational PA: extracted study data
```

## How to reproduce

1. Clone the repository: `git clone https://github.com/KillianFoubert/meta-analysis-lung-cancer.git`
2. Open `lung-cancer-meta-analysis.Rproj` in RStudio (this sets the working directory automatically)
3. Install required packages:

```r
install.packages(c("meta", "metafor", "tidyverse", "knitr", "kableExtra",
                   "gridExtra", "here", "base64enc", "htmltools"))
```

4. Open `meta_analysis_report_en.Rmd` (or `_fr.Rmd`) and click **Knit**

## Reference

Qie, R., Han, M., Huang, H., Sun, P., Xie, Y., He, J., & Zhang, Y. (2023). Physical activity and risk of lung cancer: A systematic review and dose-response meta-analysis of cohort studies. *Journal of the National Cancer Center*, 3, 48–55. [doi:10.1016/j.jncc.2022.12.003](https://doi.org/10.1016/j.jncc.2022.12.003)

## Author

**Killian Foubert, Ph.D.**

* Portfolio: [killianfoubert.github.io](https://killianfoubert.github.io)
* GitHub: [github.com/KillianFoubert](https://github.com/KillianFoubert)
* LinkedIn: [linkedin.com/in/kfoubert](https://linkedin.com/in/kfoubert/)

## License

MIT
