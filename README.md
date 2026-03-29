# Rental Market & Income Inequality in Spain

Exploratory analysis of living conditions using microdata from Spain's **Survey on Income and Living Conditions (ECV 2024)**, published by the Instituto Nacional de Estadística (INE).

---

## Business question

> Are people who rent their homes economically more vulnerable than those who own?  
> And who benefits on the other side — who are the landlords?

---

## What this project covers

**Part I — Tenants (arrendatarios)**
- Share of the population living in rented housing
- Proportion belonging to the low-income class (< 75% of median income)
- Comparison of low-income rates between tenants and non-tenants
- Mean equivalent income by housing tenure

**Part II — Landlords (arrendadores)**
- Share of the population with rental income
- Proportion belonging to the high-income class (> 200% of median income)
- Income distribution by percentile (P10, P50, P90)
- Internal inequality measured by the P90/P10 ratio

---

## Key findings

- Around **1 in 4 people** in Spain lives in rented housing
- The share of low-income individuals is substantially **higher among tenants**
- Landlords show a significantly **higher proportion of high-income** individuals
- The P90/P10 ratio reveals differences in internal inequality between both groups

---

## Dataset

| Source | INE — Encuesta de Condiciones de Vida (ECV) 2024 |
|---|---|
| Unit | Individual microdata with population weights (`RB050`) |
| Key variables | `HY020` (household income), `HX240` (equivalence scale), `ARRENDATARIO`, `HY040N` |
| Access | [INE microdata portal](https://www.ine.es/dyngs/INEbase/es/operacion.htm?c=Estadistica_C&cid=1254736176807&menu=resultados&idp=1254735976608) |

> Note: `ECVpersona.RData` is not included in this repository. Download the microdata directly from INE and load it following the instructions in the `.qmd` file.

---

## Stack

- **R** — dplyr, ggplot2, tidyr, Hmisc
- **Quarto** — reproducible HTML report with `code-fold` and `toc`

---

## How to run

```r
# 1. Download ECVpersona microdata from INE (link above)
# 2. Place ECVpersona.RData in the project root
# 3. Open and render ECV_mercado_alquiler.qmd in RStudio
```

---

*Lorena Marcos · UCM · 2025*
