# Restaurant Revenue Prediction — Exploratory Data Analysis

A structured exploratory data analysis project on a real-world restaurant dataset, focusing on understanding the drivers of revenue through statistical profiling, feature engineering, and visual analytics.

---

## Project Overview

This project investigates what factors influence restaurant revenue across different locations, cuisines, and operational profiles. The analysis covers 8,368 restaurant records with 17 features spanning pricing, marketing, staffing, customer engagement, and service quality. The goal is to surface actionable insights that can inform business strategy and lay the groundwork for predictive modeling.

---

## Dataset

| Property | Value |
|---|---|
| Source | Kaggle — Restaurant Revenue Prediction Dataset |
| Records | 8,368 |
| Features | 17 |
| Target Variable | Revenue (USD) |
| Missing Values | None |

**Feature Categories**

- **Identity:** Name, Location, Cuisine
- **Operational:** Seating Capacity, Average Meal Price, Parking Availability
- **Staffing:** Chef Experience Years
- **Marketing:** Marketing Budget, Social Media Followers
- **Customer Signals:** Rating, Number of Reviews, Avg Review Length
- **Quality Metrics:** Ambience Score, Service Quality Score
- **Demand:** Weekend Reservations, Weekday Reservations

---

## Key Statistics

| Metric | Value |
|---|---|
| Revenue Range | $184,709 — $1,531,868 |
| Mean Revenue | $656,071 |
| Median Revenue | $604,242 |
| Std Deviation | $267,414 |

**Top Cuisines by Mean Revenue**

| Cuisine | Mean Revenue (USD) |
|---|---|
| Japanese | $937,969 |
| French | $820,204 |
| Italian | $692,742 |
| American | $564,942 |
| Indian | $496,616 |

---

## Analysis Pipeline

**1. Data Inspection**

Shape validation, dtype profiling, null checks, cardinality review across all columns.

**2. Filtering and Subsetting**

Conditional queries on Rating, Revenue, Seating Capacity, Location, and Cuisine to isolate relevant segments.

**3. Feature Engineering**

Five derived features were created to enrich the analysis:

- **Revenue per Seat** — operational efficiency metric: Revenue / Seating Capacity
- **Marketing Efficiency** — return on spend: Revenue / Marketing Budget
- **Revenue Category** — binned revenue into Low, Medium, and High tiers
- **Total Reservations** — aggregate demand: Weekend + Weekday Reservations
- **Customer Engagement** — combined reach: Social Media Followers + Number of Reviews

**4. Aggregation and Group Analysis**

GroupBy operations on Cuisine and Location to compute mean Revenue, Rating, and Marketing Budget per segment.

**5. Correlation Analysis**

Pearson correlation matrix across all numeric features with a focus on Revenue drivers. Heatmap visualization using Seaborn.

**6. Visual Analytics**

| Chart Type | Variables |
|---|---|
| Histogram | Revenue, Rating |
| Box Plot | Revenue, Marketing Budget, Revenue by Cuisine, Revenue by Parking |
| Bar Chart | Cuisine distribution, Parking Availability, Mean Revenue by Cuisine, Top 10 by Revenue |
| Pie Chart | Cuisine share |
| Scatter Plot | Rating vs Revenue, Marketing Budget vs Revenue, Social Media Followers vs Revenue |
| Line Plot | Chef Experience Years vs Mean Revenue |
| Heatmap | Full numeric correlation matrix |

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core language |
| pandas | Data manipulation and aggregation |
| NumPy | Numerical operations |
| Matplotlib | Base visualizations |
| Seaborn | Statistical plotting |
| Jupyter Notebook | Interactive development environment |

---

## Project Structure

```
restaurant-revenue-eda/
|
|-- restaurant-revenue-predictions-ipynb.ipynb   # Main analysis notebook
|-- restaurant-data.csv                          # Dataset
|-- README.md                                    # Project documentation
```

---

## Key Findings

- Japanese and French restaurants consistently outperform other cuisine types by revenue, despite similar average ratings.
- Marketing Budget and Social Media Followers show a positive correlation with Revenue, indicating that digital visibility has a measurable impact.
- Chef Experience Years follows a non-linear trend relative to Revenue — moderate experience levels outperform both extremes in several segments.
- Restaurants with parking availability show a broader revenue distribution and a higher median, suggesting operational convenience matters to customers.
- Downtown locations yield higher average ratings than Suburban and Rural counterparts.

---

## Author

**NAIT ALI Mohamed Abderrahim**
Energy and Mechanical Engineer | Data Scientist

- GitHub: [github.com/Loki-01](https://github.com/Loki-01)
- LinkedIn: [linkedin.com/in/nait-ali-mohamed-abderrahim-663a202a5](https://linkedin.com/in/nait-ali-mohamed-abderrahim-663a202a5)

---

## License

This project is open for educational and portfolio purposes. Dataset credit: Anthony Therrien via Kaggle.
