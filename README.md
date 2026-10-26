# Rental Market & Income Inequality in Spain

[![Report](https://img.shields.io/badge/report-live-2ea44f)](https://lorenadata.github.io/ECV-rental-market/)
![R](https://img.shields.io/badge/R-276DC3?logo=r&logoColor=white)
![Quarto](https://img.shields.io/badge/Quarto-75AADB?logo=quarto&logoColor=white)

Survey-weighted analysis of both sides of the Spanish rental market, using official microdata from the INE **Survey on Income and Living Conditions (ECV 2024)**.

**📄 Full report (Spanish):** https://lorenadata.github.io/ECV-rental-market/

---

## Questions

> Are people who rent their homes economically more vulnerable than those who own?
> And on the other side, who are the landlords?

## Key findings

- Around **1 in 4 people** in Spain lives in rented housing.
- The share of low-income individuals is substantially **higher among tenants** than among non-tenants.
- People with rental income show a much **higher share of high-income** individuals.
- The P90/P10 ratio shows how internal inequality differs between tenants and landlords.

## Methodology

**Income classes.** These follow the Eurostat convention on equivalised income (`HY020 / HX240`). The national median is €19,307 in ECV 2024.
- *Low income:* below 75% of the median
- *High income:* above 200% of the median

**Part I: Tenants.** Share of the population renting, low-income rate compared with non-tenants, and mean equivalised income by housing tenure.

**Part II: Landlords.** Share of the population with rental income (`HY040N`), high-income rate, income percentiles (P10, P50, P90) and the P90/P10 ratio.

All estimates are weighted with the population expansion factor `RB050`.

## Repository structure

```
.
├── ECV_mercado_alquiler.qmd   # Analysis source (Quarto)
├── index.html                 # Rendered report, served by GitHub Pages
└── ECVpersona.RData           # ECV 2024 person-level microdata (INE)
```

## Reproduce

```r
install.packages(c("dplyr", "tidyr", "ggplot2", "Hmisc"))
```

Open `ECV_mercado_alquiler.qmd` in RStudio and click **Render**. The microdata file is included; it can also be downloaded from the [INE microdata portal](https://www.ine.es/dyngs/INEbase/es/operacion.htm?c=Estadistica_C&cid=1254736176807&menu=resultados&idp=1254735976608).

## Data source

Instituto Nacional de Estadística (INE), *Encuesta de Condiciones de Vida 2024*, person-level microdata. Data © INE, reused under its open-data terms.

---

**Lorena Marcos** · Applied Data Science, Universidad Complutense de Madrid · [LinkedIn](https://www.linkedin.com/in/lorena-marcos-6516272b5/) · [GitHub](https://github.com/Lorenadata)
