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
## 📌 Results and Insights

The data analysis revealed several key findings that can help optimize Walmart's operations:

- **Cash** was the most used payment method, both in terms of transaction count and items sold.
- **Top-rated product categories** vary by branch, providing an opportunity for location-specific promotions.
- **Peak sales periods** differ across branches and are typically concentrated in the **afternoon shift**, suggesting optimal times for staffing and inventory restocking.
- **Profitability analysis** highlighted a few categories with significantly higher margins, ideal for strategic focus.
- **Some branches showed declining revenue year-over-year**, warranting deeper investigation and targeted interventions.

These insights form the basis for practical business recommendations.


## 💡 Business Recommendations

- **Promote high-performing categories** tailored to each branch.
- **Enhance staffing and inventory** during identified peak hours.
- **Encourage Ewallet usage** in branches with low digital payment adoption.
- **Focus marketing efforts** on city-specific category performance.
- **Investigate underperforming branches** and address causes of revenue decline.

## Future Enhancements

Possible extensions to this project:
- Integration with a dashboard tool (e.g., Power BI or Tableau) for interactive visualization.
- Additional data sources to enhance analysis depth.
- Automation of the data pipeline for real-time data ingestion and analysis.

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
