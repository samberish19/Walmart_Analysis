# 🛒 Walmart Sales Data Analysis

This project provides a comprehensive exploratory data analysis (EDA) of Walmart's retail sales data to uncover trends, patterns, and actionable insights for better decision-making.

---

## 📊 Objective

Analyze historical sales data across different Walmart stores and departments to:

- Identify sales trends over time
- Understand the impact of holidays and external factors like temperature and fuel prices
- Evaluate performance across store types and departments
- Provide recommendations to improve business operations

---

## 📁 Project Structure

```plaintext
|-- Walmart_Analysis/
|-- data/                     # Raw data and transformed data
|-- sql_queries/              # SQL scripts for analysis and queries
|-- notebooks/                # Jupyter notebooks for Python analysis
|-- README.md                 # Project documentation
|-- requirements.txt          # List of required Python libraries
|-- main.py                   # Main script for loading, cleaning, and processing data
```
---

---

## Project Steps

### 1. Set Up the Environment
   - **Tools Used**: Visual Studio Code (VS Code), Python, SQL (MySQL)
   - **Goal**: Create a structured workspace within VS Code and organize project folders for smooth development and data handling.

### 2. Set Up Kaggle API
   - **API Setup**: Obtain your Kaggle API token from [Kaggle](https://www.kaggle.com/) by navigating to your profile settings and downloading the JSON file.
   - **Configure Kaggle**: 
      - Place the downloaded `kaggle.json` file in your local `.kaggle` folder.
      - Use the command `kaggle datasets download -d <dataset-path>` to pull datasets directly into your project.

### 3. Download Walmart Sales Data
   - **Data Source**: Use the Kaggle API to download the Walmart sales datasets from Kaggle.
   - **Dataset Link**: [Walmart Sales Dataset](https://www.kaggle.com/najir0123/walmart-10k-sales-datasets)
   - **Storage**: Save the data in the `data/` folder for easy reference and access.

### 4. Install Required Libraries and Load Data
   - **Libraries**: Install necessary Python libraries using:
     ```bash
     pip install pandas numpy sqlalchemy mysql-connector-python 
     ```
   - **Loading Data**: Read the data into a Pandas DataFrame for initial analysis and transformations.

### 5. Explore the Data
   - **Goal**: Conduct an initial data exploration to understand data distribution, check column names, types, and identify potential issues.
   - **Analysis**: Use functions like `.info()`, `.describe()`, and `.head()` to get a quick overview of the data structure and statistics.

### 6. Data Cleaning
   - **Remove Duplicates**: Identify and remove duplicate entries to avoid skewed results.
   - **Handle Missing Values**: Drop rows or columns with missing values if they are insignificant; fill values where essential.
   - **Fix Data Types**: Ensure all columns have consistent data types (e.g., dates as `datetime`, prices as `float`).
   - **Currency Formatting**: Use `.replace()` to handle and format currency values for analysis.
   - **Validation**: Check for any remaining inconsistencies and verify the cleaned data.

### 7. Feature Engineering
   - **Create New Columns**: Calculate the `Total Amount` for each transaction by multiplying `unit_price` by `quantity` and adding this as a new column.
   - **Enhance Dataset**: Adding this calculated field will streamline further SQL analysis and aggregation tasks.

### 8. Load Data into MySQL 
   - **Set Up Connections**: Connect to MySQL  using `sqlalchemy` and load the cleaned data into each database.
   - **Table Creation**: Set up tables in MySQL using Python SQLAlchemy to automate table creation and data insertion.
   - **Verification**: Run initial SQL queries to confirm that the data has been loaded accurately.

### 9. SQL Analysis: Complex Queries and Business Problem Solving
   - **Business Problem-Solving**: Write and execute complex SQL queries to answer critical business questions, such as:
     - Revenue trends across branches and categories.
     - Identifying best-selling product categories.
     - Sales performance by time, city, and payment method.
     - Analyzing peak sales periods and customer buying patterns.
     - Profit margin analysis by branch and category.
   - **Documentation**: Create pdfs for clear notes of each query's objective, approach, and results.

### 10. Project Publishing and Documentation
   - **Documentation**: I have uploaded all the documents all the important things are mentioned in the files.
   - **Project Publishing**: Published this complete project here on GitHub, including:
     - The `README.md` file (this document).
     - Jupyter Notebooks (if applicable).
     - SQL query scripts.
     - Data files (if possible) or steps to access them.

---


---

## 🛠️ Technologies Used

- **Python** (Pandas, NumPy, Matplotlib, Seaborn)
- **Jupyter Notebook**
- **Git** and **GitHub** for version control

---

## 🚀 How to Run This Project

1. **Clone the repository:**
   ```bash
   git clone https://github.com/samberish19/Walmart_Analysis.git
   cd Walmart_Analysis

2. Install Python libraries:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up your Kaggle API, download the data, and follow the steps to load and analyze.

---


## Results and Insights

This section will include your analysis findings:
- **Sales Insights**: Key categories, branches with highest sales, and preferred payment methods.
- **Profitability**: Insights into the most profitable product categories and locations.
- **Customer Behavior**: Trends in ratings, payment preferences, and peak shopping hours.

## Future Enhancements

Possible extensions to this project:
- Integration with a dashboard tool (e.g., Power BI or Tableau) for interactive visualization.
- Additional data sources to enhance analysis depth.
- Automation of the data pipeline for real-time data ingestion and analysis.

---

## 📌 Results and Insights

This project involved solving several key business problems for Walmart using MySQL and Python-based data analysis. Here are the primary insights derived from the dataset:

### 💳 1. Payment Preferences
- **Cash** was the most used payment method, followed by **Credit Card** and **Ewallet**.
- The highest number of items sold was also via **Cash**, indicating a strong customer preference.

### 🏬 2. Top-Rated Categories by Branch
- Each branch had a distinct top-performing category based on average customer rating.
- This allows for **branch-specific marketing** and inventory decisions.

### 📅 3. Busiest Days
- Each Walmart branch had a unique **busiest day of the week**, which can help in **staff scheduling** and **stock planning**.
- For example, Branch A saw peak activity on **Saturday**, while Branch C peaked on **Friday**.

### 📦 4. Sales Volume by Payment Method
- **Total quantity sold** also aligned closely with the most frequently used payment method (Cash).
- This confirms **high volume and trust** in that payment channel.

### 🏙️ 5. Category Ratings by City
- **Average, minimum, and maximum ratings** were calculated per category per city.
- Useful for designing **city-level promotions** and **tailored shopping experiences**.

### 💰 6. Profitability by Category
- The analysis ranked categories by **total profit**, revealing where the **highest margins** lie.
- Focused expansion into these categories could **boost overall profitability**.

### 🧾 7. Preferred Payment Methods per Branch
- Payment methods varied by branch, indicating **local payment preferences**.
- For example, Branch B showed a higher usage of **Ewallets** compared to others.

### 🕰️ 8. Sales by Time of Day (Shifts)
- Transactions were broken down into **Morning**, **Afternoon**, and **Evening** shifts.
- **Afternoon** emerged as the most active time period overall, guiding **shift management** and **inventory restocking**.

### 📉 9. Revenue Decline by Branch (YoY)
- Identified top 5 branches with the **highest revenue decline** year-over-year (e.g., 2022 to 2023).
- Useful for **diagnosing local market issues** and taking corrective action.

---

## 💡 Business Recommendations

Based on the analytical insights drawn from the data, here are several actionable recommendations for Walmart:

### 1. **Optimize Payment Infrastructure**
- Ensure that **cash payments** are fast and well-supported in all branches.
- Consider promoting **Ewallet usage** in branches where it is underutilized, possibly through loyalty programs or discounts.

### 2. **Branch-Specific Product Focus**
- Highlight and promote the **top-rated categories** within each branch through in-store displays and digital ads.
- Tailor inventory and promotional strategies based on **local preferences**.

### 3. **Enhance Staffing on Peak Days**
- Use the identified **busiest day per branch** to optimize staffing levels.
- Reinforce customer service and checkout resources on these high-traffic days.

### 4. **Shift-Based Sales Optimization**
- Since **afternoons** are the busiest across branches, focus replenishment, cleaning, and promotions during low-traffic **morning** and **evening** periods.
- Align employee shift scheduling with these patterns for better efficiency.

### 5. **Targeted City-Level Promotions**
- Launch **city-specific marketing campaigns** based on category performance in each location.
- Focus on categories with high average ratings to maintain customer satisfaction and repeat visits.

### 6. **Maximize Profit-Generating Categories**
- Increase marketing and shelf space for **high-profit categories** identified through the analysis.
- Negotiate better supplier terms for top-margin products.

### 7. **Mitigate Revenue Decline**
- Conduct further analysis on the **branches showing year-over-year revenue decline** to identify root causes (e.g., local competition, poor ratings, fewer transactions).
- Consider management audits or localized surveys in these underperforming locations.

---

## 👨‍💻 Author

**Samberish19**  
📎 GitHub: [https://github.com/samberish19](https://github.com/samberish19)

---

## 📬 Contributions

Feel free to fork this repo and submit pull requests. Suggestions, improvements, or corrections are welcome!

## Acknowledgments

- **Data Source**: Kaggle’s Walmart Sales Dataset
- **Inspiration**: Walmart’s business case studies on sales and supply chain optimization.

---
