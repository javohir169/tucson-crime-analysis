Tucson Crime Analysis (Data Science + ML)

Overview
This project explores crime patterns in Tucson, Arizona and investigates how crime frequency relates to socioeconomic conditions (income) and environmental/infrastructure factors (streetlights). The goal is not only to visualize where crime is happening, but also to understand what factors may contribute to it, and whether crime counts can be predicted using machine learning.

Why I built this
Crime impacts community safety, quality of life, and how cities allocate resources. In this project, we focused on:
- Which Tucson wards experience the highest crime volume?
- What crime types are most common citywide?
- How do income levels relate to crime?
- How does streetlight distribution relate to crime frequency?
- Can we predict crime counts using socioeconomic indicators?

Data Used
The analysis integrates multiple public datasets:
- Neighborhood income data
- Tucson police reported crimes (type, time, location)
- Streetlight distribution data
- Tucson ward boundaries (CSV + GeoJSON)

Key Findings
1) Crime is unevenly distributed across the city
Crime totals vary significantly by ward:
- Ward 3 and Ward 6 have the highest crime totals (major hotspots)
- Ward 4 has the lowest crime totals (comparatively safer)

2) Property crime dominates in Tucson
Larceny is the most common crime type, accounting for about 68.7% of all crimes across wards. This suggests Tucson’s crime profile is largely driven by property-related offenses.

3) Streetlights vs crime is a complex relationship
- Crime count and streetlight count have a moderately strong positive correlation (~0.67), likely due to urban density (more lights and more crime in busy areas).
- Streetlight count and crimes per streetlight show a slightly negative correlation (-0.19), suggesting that lighting may reduce the crime burden per light.

4) Income vs crime pattern
High-crime wards (especially Wards 3 and 6) generally show lower median and average income, while Ward 4 shows higher income with lower crime totals. This supports the idea that economic disadvantage can contribute to elevated crime, but it is not the only factor.

Machine Learning: Prediction
To test predictive power of socioeconomic indicators, two regression models were built:
- Linear Regression (baseline)
- Random Forest Regressor (non-linear model)

Model Results (from report output)
Linear Regression:
- Cross-validated R²: 0.82 ± 0.09
- Cross-validated MSE: 92362722.35
- Final MSE: 13841243.97
- Final R²: 0.98

Random Forest:
- Cross-validated R²: 0.87 ± 0.10
- Cross-validated MSE: 66834073.16
- Final MSE: 6851218.75
- Final R²: 0.99
- Best parameters: max_depth=None, min_samples_split=2, n_estimators=100

Random Forest performed slightly better overall and captured non-linear relationships more effectively.

Files in this Repo
- project1_380.ipynb: Full pipeline (data processing, EDA, visualizations, modeling)
- report.pdf: Final report writeup

Tools and Libraries
Python, pandas, numpy, matplotlib, scikit-learn

Authors
Imronbek Abduvaliev
Javokhir Kakhkhorov
Tokhirjon Vokhidov

