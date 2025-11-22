-----

# 📊 Quantium Retail Data Science & AI Project

## About Quantium

Quantium is a **leading data science and AI firm**, founded in Australia in 2002. With over **17 years of innovation** in data science, Quantium combines the best of human and artificial intelligence to create possibilities for individuals, organizations, and society.

-----

## 🚀 Project Overview

This project is a retail analytics engagement focused on analyzing customer transaction data to drive commercial recommendations for a client's chip category. It consists of three primary phases:

1.  **Data Preparation and Customer Analytics:** Identify customer purchasing behaviors to generate key insights.
2.  **Experimentation and Uplift Testing:** Design and execute a benchmark/control store experiment to test the commercial impact of store layout changes (trials).
3.  **Analytics and Commercial Application:** Synthesize findings into a final report for the Category Manager.

-----

## 💻 Installation

This project is developed using the **R programming language**.

### Required Software

  * **R Software:** Download and install R from the official **CRAN** website: [https://cran.r-project.org/](https://cran.r-project.org/)

### Required Libraries

Run the following commands in your R console to install the necessary packages:

```r
install.packages("ggplot2")
install.packages("ggmosaic")
install.packages("readr")
```

-----

## 🔬 Task 1: Data Preparation & Customer Analytics

### Objective

Analyze the transaction dataset to understand current purchasing trends and behaviors, with a specific focus on **customer segments** and their chip purchasing habits.

The client is particularly interested in two key segmentation attributes:

  * **LIFESTAGE:** Defines customer life stage, e.g., young singles/couples, older families, etc.
  * **PREMIUM\_CUSTOMER:** Differentiates shoppers based on their price sensitivity (e.g., budget, mainstream, premium).

### Key Insights & Recommendations

  * **Top Contributing Segments:** Sales are primarily driven by **Budget - Older Families**, **Mainstream - Young Singles/Couples**, and **Mainstream - Retirees** segments.
  * **High Spend:** The high chip expenditure by **Mainstream - Young Singles/Couples** and **Mainstream - Retirees** is largely attributable to the sheer volume of these buyers.
  * **Impulse Behavior:** **Mainstream - Mid-age and Young Singles/Couples** are more likely to spend more per packet of chips, indicating **impulse buying behavior**.
  * **Brand Affinity:** **Mainstream - Young Singles/Couples** are **23% more likely** to purchase **Tyrrells** chips compared to the general population.

### Commercial Recommendation

To boost category performance, the Category Manager should consider **off-locating** specific products (Tyrrells and smaller chip packs) in **discretionary space** near areas frequently visited by **young singles/couples**. This strategy aims to increase visibility and capitalize on their impulse buying tendency.

-----

## 📈 Task 2: Experimentation & Uplift Testing

### Objective

Identify suitable **benchmark (control) stores** for each of the trial stores to accurately measure the sales **uplift** resulting from the new store layouts.

### Methodology

A **comparison measure** must be created to compare potential control stores against trial stores. A **reusable function** should be implemented to streamline the selection process for multiple trial stores.

Possible comparison metrics include:

  * **Pearson Correlation**
  * **Magnitude Distance Metric:** $1 - \frac{\text{Observed Distance} - \text{Minimum Distance}}{\text{Maximum Distance} - \text{Minimum Distance}}$

The analysis involves comparing sales trends for each trial and control pair **during the trial period**.

### Key Findings

  * **Selected Control Stores:** Control stores 233, 155, and 237 were identified for trial stores 77, 86, and 88, respectively.
  * **Trial Impact:**
      * Trial stores **77 and 88** showed a **significant difference** in sales uplift in at least two of the three trial months.
      * Trial store **86** did **not** show a similar significant difference. Further investigation with the client regarding the trial's implementation in store 86 is recommended.
  * **Overall Conclusion:** Despite the anomaly in store 86, the overall trial demonstrates a **significant increase in sales** due to the new store layouts.

-----

## 📝 Task 3: Analytics and Commercial Application

### Objective

Prepare a comprehensive **final report** for the client (the Category Manager) summarizing the analytical insights and commercial recommendations derived from **Task 1 and Task 2**.

-----
