# affilate_retention_abtest

A/B Testing Analysis: 
E-Commerce Conversion Optimization

This project evaluates user conversion funnels across four distinct marketing/product experiments using a multi-metric framework. By performing two-sided Z-tests for proportions, the analysis isolates actual feature impacts from random statistical noise, driving data-validated product decisions.

📂 Repository StructurePlaintextaffilate_retention_abtest/
│
├── code/
│   └── affilate_retention.ipynb      # Data aggregation, EDA, and statistical testing
│
├── datasets/
│   └── ab_test_significance_results.csv # Exported statistical outputs
│
└── viz/
    └── README.md                     # Links and context for the Tableau dashboard
    
🛠️ Tech Stack & MethodologyData Manipulation: 

pandas (Nested aggregations, custom pivot tables).

Statistical Analysis: statsmodels (proportions_ztest for two-sample Z-tests).

Data Visualization: Tableau Public for cross-functional reporting.

Core Metrics Tracked (per Session):Add Payment Info Conversion Rate ($CR_{payment}$)

Add Shipping Info Conversion Rate ($CR_{shipping}$)

Begin Checkout Conversion Rate ($CR_{checkout}$)

New Account Creation Rate ($CR_{account}$)

📊 Experiment Results SummaryThe statistical significance of each experiment was calculated using a two-sided Z-test with an alpha level ($\alpha$) of 0.05.Test ID MetricControl CRTest CRUplift (%)P-ValueSignificanceAction1add_payment_info / session4.38%4.93%+12.54%0.000087✨ SignificantDeploy1add_shipping_info / session6.69%7.13%+6.56%0.009226

✨ SignificantDeploy1begin_checkout / session8.34%8.90%+6.66%0.002894

✨ SignificantDeploy1new_accounts / session8.43%8.15%-3.35%0.122859Not SignificantNeutral2All Metrics Evaluated———> 0.05Not SignificantIterate / Rollback3begin_checkout / session13.61%13.15%-3.35%0.012026

⚠️ Significant DropRollback4begin_checkout / session11.95%11.67%-2.35%0.045934

⚠️ Significant DropRollback4new_accounts / session8.55%8.26%-3.36%0.017527

⚠️ Significant DropRollback💡 Key Business Insights & Conclusions🚀 Test 1 is a Definitive Success: It delivered robust, statistically significant positive uplifts across the upper and middle funnel stages (Payment info, Shipping info, and Checkout starts), with an impressive 12.54% uplift in payment info submissions.⚖️ Test 2 is Neutral: No statistically valid deviations were observed, indicating the variant changes had no tangible impact on user behavior.🚨 Tests 3 & 4 Caused Regression: Both variants introduced friction that significantly depressed down-funnel performance (e.g., a -3.36% drop in account creation for Test 4). These modifications should be permanently discarded.

🔗 Project Links📊 Interactive Tableau Dashboard: https://public.tableau.com/app/profile/dmytro.ruzhytskyi/viz/affilate_retention_AB_test/Dashboard2

Raw & Processed Datasets: https://drive.google.com/drive/folders/1mm0oF_KTewXzk7Qm57zJKaqEyKwl4PaZ?usp=sharing
