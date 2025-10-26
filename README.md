# Flipkart-E-commerce-Data-Analysis

# Flipkart E-commerce Product Analysis

## Project Overview
 
This project analyzes a sample dataset of Flipkart e-commerce products. The goal is to explore product details, pricing strategies, discounts, ratings, and identify patterns across different product categories and brands using Python libraries like Pandas, Matplotlib, and Seaborn.

## Dataset

* **Source:** # [Download the Flipkart Dataset](https://drive.google.com/file/d/1tVMd6DKzFwgLmUdwoGsstT_qZj480Koc/view?usp=sharing)
* **Description:** Contains information on approximately 20,000 products listed on Flipkart.
* **Key Features:** `uniq_id`, `product_name`, `product_category_tree`, `brand`, `retail_price`, `discounted_price`, `product_rating`, `overall_rating`, `description`, etc.

## Objectives

* Load and explore the Flipkart product dataset.
* Clean and preprocess the data (handle missing values, convert data types).
* Engineer new features, such as discount percentage.
* Perform aggregate analysis to understand trends by product category and brand.
* Visualize the relationship between product discounts and ratings.
* Identify top categories, brands, and highly discounted products.
* Provide a simple way to look up details for a specific product ID.

## Tools Used

* Python 3
* Pandas (Data manipulation and analysis)
* Matplotlib (Data visualization)
* Seaborn (Data visualization)
* Jupyter Notebook (Development environment)
* (Optional: ipywidgets for interactive lookup)

## Analysis Steps

1.  **Data Loading:** Imported the CSV data into a Pandas DataFrame.
2.  **Exploratory Data Analysis (EDA):**
    * Examined DataFrame structure (`head`, `info`, `shape`).
    * Checked for missing values (`isnull().sum()`, percentage calculation).
    * Analyzed unique value counts (`nunique`).
    * Generated descriptive statistics for numerical columns (`describe`).
3.  **Data Cleaning:**
    * Converted price columns (`retail_price`, `discounted_price`) to numeric.
    * Converted rating columns (`product_rating`, `overall_rating`) to numeric, handling non-numeric entries like "No rating available".
4.  **Feature Engineering:**
    * Calculated `discounted_%` using the formula: `((retail_price - discounted_price) / retail_price) * 100`.
5.  **Analysis & Insights:**
    * Developed functions (simple and interactive) to retrieve product details by `uniq_id`.
    * Grouped data by category (`product_category_tree`) to compute average prices, discounts, and counts.
    * Grouped data by brand (`brand`) to compute average discounts, ratings, and counts.
    * Identified the top 10 most discounted products.
6.  **Visualization:**
    * Created a scatter plot comparing discount percentage vs. overall rating.
    * Created discount percentage bins.
    * Generated a box plot showing overall rating distribution across discount ranges.
    * Generated bar plots for top categories (by avg discount) and top brands (by product count).

## Key Findings (Example - Fill these based on your actual results)

* The dataset contains significant missing values in the `brand` column (~29%).
* The top 10 product categories by count include [List top categories found, e.g., Jewellery, Automotive Accessories, etc.].
* The top 10 brands by product count include [List top brands found, e.g., Allure Auto, Regular, Voylla, etc.].
* Average discounts vary significantly across categories like [Mention categories with high/low avg discounts].
* The relationship between discount percentage and overall product rating appears to be [Describe the relationship observed from the plots - e.g., weak, non-linear, some ranges have higher median ratings, etc.].
* The products with the highest discounts (over 90%) belong primarily to categories like [Mention categories like FashBlush Jewellery, Rajcrafts Home Furnishing, etc.].

*(Optional: Include Images of your plots here)*

```markdown
### Discount vs. Rating Scatter Plot
![Discount vs Rating](path/to/scatter_plot.png)

### Rating Distribution by Discount Range
![Rating by Discount Box Plot](path/to/box_plot.png)

### Top Categories by Avg Discount
![Top Categories Bar Plot](path/to/category_bar_plot.png)

### Top Brands by Product Count
![Top Brands Bar Plot](path/to/brand_bar_plot.png)
