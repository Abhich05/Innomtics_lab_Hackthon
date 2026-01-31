# Food Delivery Data Analysis - Hackathon Submission

## Project Overview

This project demonstrates end-to-end data analysis of a food delivery platform by combining multiple data sources, performing comprehensive analysis, and deriving actionable business insights.

**Hackathon Challenge:** Merge three different data formats (CSV, JSON, SQL) and answer analytical questions about user behavior, restaurant performance, and revenue patterns.

---

## Objectives

1. **Data Integration**: Combine transactional, user, and restaurant data from different sources
2. **Data Analysis**: Answer 10 MCQs, 6 numerical questions, and 9 fill-in-the-blank questions
3. **Business Insights**: Identify trends in orders, revenue, user behavior, and restaurant performance
4. **Visualization**: Create meaningful visualizations to support findings

---

## Dataset Description

### 1. orders.csv (Transactional Data)
- **Records**: 10,000 orders
- **Columns**: order_id, user_id, restaurant_id, order_date, total_amount, restaurant_name
- **Period**: January 2023 - December 2023

### 2. users.json (User Master Data)
- **Records**: 3,000 users
- **Columns**: user_id, name, city, membership
- **Cities**: Bangalore, Chennai, Hyderabad, Pune
- **Membership**: Gold, Regular

### 3. restaurants.sql (Restaurant Master Data)
- **Records**: 500 restaurants
- **Columns**: restaurant_id, restaurant_name, cuisine, rating
- **Cuisines**: Chinese, Indian, Italian, Mexican
- **Ratings**: 3.0 - 5.0

---

## Technical Implementation

### Technologies Used
- **Python 3.8+**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical operations
- **Matplotlib & Seaborn** - Data visualization
- **JSON & Regex** - Data parsing

### Data Processing Pipeline

```
orders.csv ──────┐
                 ├──> Merge on user_id ──> Merge on restaurant_id ──> Final Dataset (10,000 records)
users.json ──────┤                                                     
                 │
restaurants.sql ─┘
```

### Key Operations
1. **Data Loading**: Parse CSV, JSON, and SQL formats
2. **Data Cleaning**: Handle missing values and data types
3. **Data Merging**: LEFT JOIN operations on key columns
4. **Feature Engineering**: Extract date components, create rating ranges
5. **Analysis**: Aggregations, grouping, filtering
6. **Visualization**: Revenue trends, distribution analysis

---

## Key Findings

### Revenue Insights
- **Total Revenue**: ₹8,011,624.12
- **Top Revenue City (Gold)**: Chennai (₹1,080,909.79)
- **Best Quarter**: Q3 Jul-Sep (₹2,037,385.10)
- **Top Cuisine**: Mexican (Highest avg order value: ₹808.02)

### User Behavior
- **Gold Members**: 49.87% of total orders (4,987 orders)
- **Gold Avg Order**: ₹797.15
- **Regular Avg Order**: ₹801.23
- **High-Value Users**: 2,544 users spent >₹1,000 total

### Restaurant Performance
- **Top Rating Range**: 4.6-5.0 (₹2,197,030.75 revenue)
- **High-Rated Orders**: 3,374 orders from restaurants rated ≥4.5
- **Cuisine Distribution**: Relatively balanced across all cuisines

### City Analysis
- **Chennai**: Leads in Gold member revenue and average order value
- **Hyderabad**: Total revenue ₹1,889,366.58
- **Active Users**: 2,883 distinct users across all cities

---

## Repository Structure

```
food-delivery-hackathon/
│
├── README.md                                    # This file
├── Food_Delivery_Analysis_Hackathon.ipynb      # Main analysis notebook
├── final_food_delivery_dataset.csv             # Merged dataset (output)
│
├── data/                                        # Input datasets
    ├── orders.csv
    ├── users.json
    └── restaurants.sql
                 
```

---

## How to Run

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Execution Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/Abhich05/Innomtics_lab_Hackthon
   cd food-delivery-hackathon
   ```

2. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook Food_Delivery_Analysis_Hackathon.ipynb
   ```

3. **Run all cells**
   - Click "Cell" → "Run All" or use Shift+Enter for each cell
   - The notebook will generate all outputs and visualizations

### Expected Outputs
- Final merged dataset: `final_food_delivery_dataset.csv`
- All MCQ answers
- All numerical answers
- Data visualizations
- Business insights summary

---

##  Analysis Highlights

### Multiple Choice Questions (10)
1. Top Gold revenue city: **Chennai**
2. Highest avg order cuisine: **Mexican**
3. Users spending >₹1000: **>2000**
4. Top revenue rating range: **4.6-5.0**
5. Gold avg order city: **Chennai**
6. Fewest restaurants cuisine: **Chinese**
7. Gold member %: **50%**
8. Best restaurant (<20 orders): **Ruchi Foods Chinese**
9. Top revenue combo: **Gold + Italian**
10. Best quarter: **Q3 (Jul-Sep)**

### Numerical Questions (6)
1. Gold member orders: **4987**
2. Hyderabad revenue: **1889367**
3. Distinct users: **2883**
4. Gold avg order: **797.15**
5. High-rated orders: **3374**
6. Top Gold city orders: **1337**

### Fill-in-the-Blank (9)
1. Join column (orders-users): **user_id**
2. Restaurant data format: **SQL**
3. Final dataset rows: **10000**
4. Unmatched values: **NaN**
5. Merge function: **merge**
6. Membership source: **users.json**
7. Join column (orders-restaurants): **restaurant_id**
8. Food type column: **cuisine**
9. User detail repetition: **multiple times**

---

## Business Recommendations

Based on the analysis:

1. **Focus on Chennai**: Highest Gold member engagement and revenue
2. **Premium Quality**: 4.6-5.0 rated restaurants drive most revenue
3. **Mexican Cuisine**: Promote for higher order values
4. **Q3 Marketing**: Capitalize on peak season (Jul-Sep)
5. **Gold Program**: Nearly 50% adoption - strong value proposition
6. **User Retention**: 85%+ users are repeat customers (>₹1000 spent)

---

## Methodology

### Data Quality Checks
- Verified no missing values in key columns
- Confirmed data type consistency
- Validated join operations (10,000 records maintained)
- Cross-checked aggregations with manual calculations

### Analysis Approach
1. **Exploratory Data Analysis (EDA)**
2. **Descriptive Statistics**
3. **Comparative Analysis** (cities, cuisines, memberships)
4. **Temporal Analysis** (quarterly trends)
5. **Segmentation** (user behavior, restaurant performance)

---

## Skills Demonstrated

- Data Wrangling (CSV, JSON, SQL parsing)
- Data Integration (Multi-source merging)
- Data Analysis (Pandas operations)
- Statistical Analysis (Aggregations, distributions)
- Data Visualization (Matplotlib, Seaborn)
- Business Intelligence (Insight generation)
- Problem Solving (Hackathon questions)

---

## Validation

All answers have been:
- Verified against original datasets
- Cross-checked with multiple methods
- Documented with supporting evidence
- Tested for accuracy and completeness

---

## Contact

For questions or clarifications about this analysis:
- **GitHub**: https://github.com/Abhich05
- **LinkedIn**: https://www.linkedin.com/in/errorwithabhich/

---

##  License

This project is submitted as part of a hackathon evaluation. All rights reserved.

---

## Acknowledgments

- Dataset provided by Hackathon organizers
- Python data science community for excellent libraries
- Pandas, NumPy, Matplotlib developers

---

**Note**: This analysis was completed as part of a data analytics hackathon challenge. The findings are based on the provided sample datasets and represent analytical capabilities in data integration, analysis, and insight generation.

---

### If you find this analysis helpful, please star this repository!

**Last Updated**: January 31, 2026