# Quantium Virtual Internship - Retail Strategy and Analytics

## 📝 Project Overview
This repository contains the R code and analysis for the **Quantium Virtual Internship** in Retail Strategy and Analytics. The project focuses on leveraging transaction and customer data to identify valuable customer segments and measure the impact of a targeted chip category trial.

The analysis is divided into two main tasks:
1.  **Data Preparation and Customer Analytics (Task 1):** Cleaning transaction data, feature engineering, and profiling key customer segments.
2.  **Measure the Impact of the Trial (Task 2):** Designing a control group and analyzing sales uplift to assess the effectiveness of the trial.

---

## 💻 Technologies and Libraries
This project is built entirely using the **R** programming language. The following packages are required:

* **`data.table`**: For fast, efficient data manipulation.
* **`readxl`**: For reading the `.xlsx` transaction data file.
* **`readr`**: For reading the `.csv` customer data file.
* **`ggplot2`**: For creating standard visualizations.
* **`ggmosaic`**: For visualizing customer segment proportions (mosaic plots).
* **`lubridate`**: For date manipulation (e.g., converting integer dates).

---

## 📂 Repository Structure
The project structure should ideally look like this:
Quantium_Retail_Analytics/ ├── code.R # Main analysis script (contains both Task 1 & 2 code) ├── README.md # This file └── Data/ ├── QVI_transaction_data.xlsx # Transaction data (Excel format) └── QVI_purchase_behaviour.csv # Customer data (CSV format)

**Note:** Ensure your data files are placed within a folder named `Data/` in the same directory as your main script.

---

## 🚀 Getting Started

### Prerequisites

1.  Install **R** and **RStudio**.
2.  Install the required R packages (run this in your R console):

```R
install.packages(c("data.table", "readxl", "readr", "ggplot2", "ggmosaic", "lubridate"))
```

📈 Task 1: Data Preparation and Customer Analytics
Key Steps
Data Loading: Loading QVI_transaction_data.xlsx (using read_excel) and QVI_purchase_behaviour.csv (using fread).

Cleaning: Converting integer dates, removing non-chip products (Salsa), and removing the outlier commercial customer (LYLTY_CARD_NBR == 226000).

Feature Engineering: Extracting PACK_SIZE (using parse_number) and cleaning/standardizing BRAND names.

Merging: Combining transaction and customer data into a single data table.

Customer Segmentation: Analyzing Total Sales, Customer Count, Average Units, and Average Price per unit segmented by LIFESTAGE and PREMIUM_CUSTOMER flag.

Deep Dive: Identifying brand and pack size affinity for the high-value segment: Mainstream Young Singles/Couples.

📊 Task 2: Measure the Impact of the Trial
(Based on typical Quantium VI scenarios, this involves selecting a control store and measuring sales uplift.)

Key Steps
Trial Definition: The trial involves stores 77, 86, and 88 for a defined period.

Control Store Selection:

Filtering: Identifying potential control stores based on pre-trial sales data.

Calculation: Measuring correlation and magnitude difference between the trial store and potential control stores.

Selection: Choosing the store with the highest correlation and lowest magnitude difference as the optimal control.

Sales Analysis:

Calculating and visualizing post-trial sales and percentage difference for the trial and control stores.

Calculating the scaling factor and percentage uplift to determine the trial's effectiveness.

Statistical Testing: Performing a t-test to confirm if the observed sales uplift is statistically significant.

Conclusion: Providing a final recommendation on whether to roll out the strategy.

👤 Author
Sairaj 
