# Steel Plate Fault Analysis (Six Sigma DMAIC)

A personal project by Ukkusuri Bharath (NIT Kurukshetra) that applies the DMAIC method to a public dataset of faulty steel plates.

## The problem
Steel plates are inspected for surface and shape faults, and seven fault types are recorded. Which faults happen most, and do they follow a pattern in plate thickness, steel type or conveyor position that shows where to investigate?

## Dataset and source
- Steel Plates Faults, UCI Machine Learning Repository: 1,941 faulty plates, 27 measurements, 7 fault types.
- Buscema, M., Terzi, S., & Tastle, W. (2010). *Steel Plates Faults* [Dataset]. https://doi.org/10.24432/C5J88N

## Methods
Pareto chart (Google Sheets); box plot, Welch's ANOVA, Games-Howell post-hoc test, contingency table, chi-square test and descriptives (jamovi); fishbone diagram (draw.io); p-chart as a method demonstration.

## Key findings
1. Other_Faults, Bumps and K_Scatch make up about 75.5% of all faults (1,466 of 1,941 plates).
2. K_Scatch occurs almost only on A400 steel (390 of 391 plates, 99.7%), and 99.0% of K_Scatch plates are 40 mm thick. K_Scatch thickness differs from every other fault type (Games-Howell, all p < .001).
3. Z_Scratch (90.5%) and Bumps (69.4%) are mostly on A300 plates with a median thickness of 70 mm. Fault type and steel type are strongly linked (chi-square = 667, df = 6, p < .001).

## Limitations
Public data, not from a real plant; only faulty plates (no fault rate can be calculated); no time column (the control chart is a method demonstration only); no specification limits; all 40 mm plates are A400, so thickness and steel type cannot be separated. The results show patterns, not proven causes.

## Files
- `steel_plates_faults_original-1.csv`: original dataset (7 yes/no fault columns)
- `steel_plates_faults_clean-1.csv`: cleaned dataset (one Fault_Type column)
- `PARETO_STEEL_PROJECT.csv`: fault counts used for the Pareto chart
- `bharath project 1.pdf`: jamovi results (descriptives, ANOVA, Games-Howell, contingency table, chi-square)
- Figures: `IMG-20261018-WA0014(1).jpg` (Pareto chart), `Fig2_Boxplot.png` (box plot), `Fig2_Fishbone.png` (fishbone diagram), `Fig4_Control_Chart.png` (control chart, method demonstration)
- `Steel_Plate_Fault_Analysis_DMAIC_Report.pdf`: full project report

## Data note
The data is public (UCI, CC BY 4.0). This is a personal learning project and does not describe any real company.
