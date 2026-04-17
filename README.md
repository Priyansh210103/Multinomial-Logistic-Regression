# Multinomial-Logistic-Regression
A Multinomial Logistic Regression analysis of Florida alligator dietary habits. This project utilizes R to model the 'ontogenetic shift' in predatory behavior based on geographical habitat and biological maturity, achieving 48.4% classification accuracy across five nominal prey categories.
# Modeling the Dietary Habits of Florida Alligators
### A Multinomial Logistic Regression Analysis

## 📌 Project Overview
This project investigates the factors influencing the prey selection of 219 American Alligators (*Alligator mississippiensis*) across four Florida lakes. Using a **Multinomial Logistic Regression** (Baseline-Category Logit) framework, the study quantifies how geographical location and physical maturity (the "ontogenetic shift") drive predatory transitions from invertebrates to vertebrate prey.

## 📊 Key Findings
* [cite_start]**The Ontogenetic Shift:** As alligators mature (Size > 2.3m), they are **4.35x more likely** to prefer fish over invertebrates compared to juveniles[cite: 486].
* [cite_start]**Predictive Accuracy:** The final additive model achieved a classification accuracy of **48.4%**, performing **2.4x better** than random chance for a 5-category response [cite: 471-472].
* [cite_start]**Gender Neutrality:** Rigorous model selection using AIC confirmed that dietary drivers are gender-neutral; adding "Sex" as a predictor increased AIC from 580.08 to 585.87, indicating it added complexity without predictive value [cite: 322-324].
* [cite_start]**Significant Predictors:** Type II Likelihood Ratio Tests confirmed both **Lake** ($p < 0.001$) and **Size** ($p < 0.001$) as primary drivers of food choice [cite: 331-334].

## 🛠 Tech Stack
* **Language:** R
* **Libraries:** `nnet` (multinomial modeling), `vcdExtra` (dataset), `ggplot2` (visualization), `car` (Anova tests), `tidyr/dplyr` (data wrangling).

## 🗂 Dataset
[cite_start]The analysis is based on the classic alligator dataset from Dr. Alan Agresti’s *Categorical Data Analysis* (Table 8.1), featuring stomach contents from Lakes George, Hancock, Oklawaha, and Trafford[cite: 173, 176].

## 📈 Methodology
1. [cite_start]**Exploratory Data Analysis (EDA):** Identified data sparsity in rare categories (Birds/Reptiles) [cite: 274-275].
2. [cite_start]**Model Selection:** Compared Null, Additive, and Interaction models using **Akaike Information Criterion (AIC)** [cite: 298-300].
3. [cite_start]**Validation:** Verified fit using McFadden’s Pseudo-R² (0.1064) and residual analysis[cite: 425, 462].
4. [cite_start]**Interpretation:** Calculated **Odds Ratios** to quantify the likelihood of prey selection shifts [cite: 483-484].

## 🚀 How to Run
1. Clone this repository.
2. Open `4561-Final-Project.Rmd` in RStudio.
3. Ensure the `vcdExtra` and `nnet` packages are installed.
4. Knit to PDF/HTML to view the full report.

---
**Author:** Priyansh Tyagi  
**Institution:** Memorial University of Newfoundland  
**Course:** Advanced Statistics (Stats 4561)
