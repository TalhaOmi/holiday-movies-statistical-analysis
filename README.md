# Holiday Movies: A Statistical Analysis (1929–2023)

Statistical analysis of how holiday-themed films have changed over nearly a century, using R and Quarto. Completed for **AMOD 5240: Statistical Aspects of Modeling** (M.Sc. Applied Modelling & Quantitative Methods, Trent University).

## Research questions

1. **Format:** How has the production format of holiday movies (theatrical, TV movie, direct-to-video) changed over time?
2. **Genre:** Has the mix of genres produced shifted across decades (e.g. away from Comedy/Family)?
3. **Runtime:** Do genres differ significantly in average runtime?

## Data

2,265 holiday-related titles from IMDb, released through the [TidyTuesday](https://github.com/rfordatascience/tidytuesday) project (2023-12-12). Files are in [`data/`](data/) (a copy also sits in `report/` so the report renders as-is). Titles were selected by keyword ("holiday", "Christmas", "Hanukkah", "Kwanzaa"), so the data is observational and not a random sample.

## Methods

- Exploratory data analysis: format counts by decade, genre trends, runtime distributions
- RQ1: polynomial / linear regression on yearly counts by title type
- RQ2: logistic regression (Comedy vs. not, over years) and chi-square test on primary genre by decade
- RQ3: one-way ANOVA, Kruskal-Wallis, and Tukey HSD post-hoc comparisons
- Tools: R, tidyverse, kableExtra, Quarto

## Repository layout

| Path | Contents |
|---|---|
| `report/` | Final report: `report.qmd` (source), `report.pdf` (rendered), plus the bibliography and citation style |
| `data/` | Source CSVs (`holiday_movies.csv`, `holiday_movie_genres.csv`) |


## Credits

Data: TidyTuesday / IMDb.

## Reproducing

Open `report/report.qmd` in RStudio (needs `tidyverse`, `kableExtra`, `readr`) and render to PDF with Quarto. The CSVs sit next to the `.qmd` so it runs as-is.
