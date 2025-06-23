# Customer Behavior Analysis in E-Commerce

This project explores and analyzes real-world e-commerce customer behavior data. The goal is to uncover purchasing patterns, calculate conversion rates, and extract behavioral insights using Python and various data analysis tools.

---

## 📁 Project Structure

```
customer-behavior-analysis/
|
├── data/
│   └── 2019-Oct.csv           # Raw dataset (~42 million rows)
├── notebooks/
│   └── 01_data_overview.ipynb # Data overview and cleaning
├── outputs/
│   └── plots/                 # Saved plots and visuals
├── requirements.txt          # Python dependencies
└── README.md                 # This file
```

---

## 📊 Dataset Description

- **Source**: Kaggle - [E-Commerce Behavior Data](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store)
- **Period**: October 2019
- **Size**: ~42 million events
- **Fields**: `event_time`, `event_type`, `product_id`, `category_id`, `user_id`, `user_session`
<br><br>
---

## 🔧 Technologies Used

- Python 3.10
- pandas
- numpy
- matplotlib
- seaborn
- Jupyter Notebook
- VS Code
<br><br>
---

## 📈 Project Workflow

### 1. Project Setup

- Created folder structure (`data/`, `notebooks/`, `outputs/plots/`)
- Created virtual environment `venv`
- Installed necessary packages and created `requirements.txt`

### 2. Initial Data Exploration (`01_data_overview.ipynb`)

- Loaded dataset from `2019-Oct.csv`
- Reviewed data dimensions, column types, and sample rows

### 3. Data Cleaning: Handling Missing Values, Duplicates, and Formatting (`01_data_overview.ipynb`)
-  Checked for missing (null) values and applied appropriate handling strategies.
-  Identified and removed duplicate records.
-  Analyzed the number of unique values in key columns. to assess data integrity.
-  Extracted date and hour components from the event_time column for further analysis.

### 4. Exploratory Data Analysis - EDA
  - Number of unique users for each event type 
   
  - Event Distribution Over the Day<br>
       - Grouped and counted all events per hour
       - Plotted using a line chart with `pandas.plot()`
        ![Distribution of Event Types](/outputs/plots/evetType_distrb.png)
  - Most popular product categories (Top 10)
       - ![Distribution of Event Types](/outputs/plots/Top_10_Product_Categories.png)
  - Event Distribution Over the Day
       - Grouped and counted all events per hour
        ![Distribution of Event Types](/outputs/plots/event_per_hour.png)
  - Conversion Rate Analysis <br>
      - Calculated relative frequency of `event_type` values (e.g., view, cart, purchase)
      - Calculated conversion rate from views to purchases:
    ```python
    conversion_rate = (purchase_count / view_count) * 100
    ```

### 5. Analyze Customer Buying Patterns
- Top 10 Hours for Purchases
   - Filtered the dataset to include only records where `event_type` is "purchase".
   - Grouped the data by event_hour to calculate the total number of purchases per hour.<br>
   - Visualized the top 10 purchasing hours using `seaborn.barplot` and `plt.bar` from `matplotlib.pyplot` 
  
  ![Distribution of Event Types](/outputs/plots/10_top_shopping_hours.png)
<br>
<br>
<br>


---



## 🚀 How to Run This Project

1. Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/customer-behavior-analysis.git
cd customer-behavior-analysis
```

2. Create and activate a virtual environment:

```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

3. Install the required packages:

```bash
pip install -r requirements.txt
```

4. Run the Jupyter notebook:

```bash
jupyter notebook
```
<br><br>
---

## 📌 Next Steps

- Create a second notebook: cart analysis
- Perform user and session analysis
- Improve visualizations and save plots in `outputs/plots/`
- Release version 2.0 with improvements and new features


---

> To view the charts and analysis, please open the notebook `01_data_overview.ipynb` in the `notebooks/` folder.