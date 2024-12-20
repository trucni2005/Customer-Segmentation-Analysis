# :bar_chart: Customer Segmentation Project

## :mag_right: About the Dataset

The dataset contains information about customers, their purchasing behavior, and various attributes. The data is split into three major categories: **People**, **Products**, **Promotion**, and **Place**. Below are the attributes of each category:

### 1. :bust_in_silhouette: People

- **ID**: Unique identifier for each customer
- **Year_Birth**: The customer's birth year
- **Education**: Customer’s education level (e.g., PhD, Master, Bachelor)
- **Marital_Status**: Customer’s marital status (Single, Married, Divorced, etc.)
- **Income**: Customer’s yearly household income
- **Kidhome**: Number of children in the customer’s household
- **Teenhome**: Number of teenagers in the customer’s household
- **Dt_Customer**: Date of customer’s enrollment with the company
- **Recency**: Number of days since the customer’s last purchase
- **Complain**: Whether the customer has complained in the last two years (1: Yes, 0: No)

### 2. :shopping_cart: Products

- **MntWines**: Amount spent on wine in the last 2 years
- **MntFruits**: Amount spent on fruits in the last 2 years
- **MntMeatProducts**: Amount spent on meat products in the last 2 years
- **MntFishProducts**: Amount spent on fish products in the last 2 years
- **MntSweetProducts**: Amount spent on sweets in the last 2 years
- **MntGoldProds**: Amount spent on gold in the last 2 years

### 3. :ticket: Promotion

- **NumDealsPurchases**: Number of purchases made with a discount
- **AcceptedCmp1** to **AcceptedCmp5**: Whether the customer accepted offers in the 5 different campaigns (1: Yes, 0: No)
- **Response**: Whether the customer accepted the offer in the last campaign (1: Yes, 0: No)

### 4. :world_map: Place

- **NumWebPurchases**: Number of purchases made through the company’s website
- **NumCatalogPurchases**: Number of purchases made using a catalog
- **NumStorePurchases**: Number of purchases made directly in stores
- **NumWebVisitsMonth**: Number of visits to the company’s website in the last month

---

## :rocket: Project Overview

The goal of this project is to perform customer segmentation based on the dataset provided. This process involves:

1. **Data Cleaning**: Preprocessing the data to handle missing values, remove outliers, and standardize the dataset.
2. **Feature Engineering**: Creating new features or transforming existing ones to enhance the model's ability to segment the customers.
3. **Data Processing**: Performing necessary transformations and preparing the data for modeling.
   
### :package: Key Deliverables:

- **Customer Segments**: Grouped customers into clusters based on spending patterns and demographic characteristics.
- **Cluster Profiles**: Descriptive analysis of each cluster to understand their spending habits, preferences, and behavior.

---

## :wrench: Project Workflow

This project is divided into several stages, which are represented in the following Jupyter Notebooks:

1. **01_Data_Cleaning.ipynb**: Data preprocessing, including handling missing data, outliers, and data transformation.
2. **02_Feature_Engineering.ipynb**: Feature transformation and creation of new variables to enhance the performance of the clustering model.
3. **03_Data_Processing.ipynb**: Further processing and preparation of data, including scaling and encoding.

---

## :chart_with_upwards_trend: Results and Insights

After applying clustering algorithms **Hierarchical Clustering**, we were able to identify distinct customer segments with the following characteristics:

### **Cluster 1: High-income families with teenage children** :moneybag:
- **Income**: High
- **Family Size**: Larger families with teenage children
- **Spending Habits**: This group tends to focus their spending on valuable items such as **wine** and **gold**.
- **Behavior**: These customers are typically financially stable, with a strong preference for premium products. Their needs are likely related to family-oriented purchases and luxury items.

### **Cluster 2: High-income individuals with no children** :older_adult:
- **Income**: Very High
- **Family Size**: Smaller families or individuals with no children
- **Spending Habits**: They spend their money evenly across a variety of product categories, such as **wine**, **fruits**, **meat**, **fish**, and **gold**.
- **Behavior**: These customers have a flexible budget and tend to purchase higher-end products. This segment is more likely to invest in luxury goods and have disposable income for various categories of spending.

### **Cluster 3: Low-income families with children** :house_with_garden:
- **Income**: Low
- **Family Size**: Large families, generally with younger children
- **Spending Habits**: Despite their lower income, they prioritize **gold** and **wine** over other categories.
- **Behavior**: This segment shows signs of financial strain, but they still value long-term investments like **gold**. Their spending on non-essentials, such as **wine**, might be driven by emotional or cultural factors.

### **Cluster 4: Lower-income individuals with small families** :family_man_woman_boy:
- **Income**: Low
- **Family Size**: Small families or individuals
- **Spending Habits**: They focus their spending on **affordable products**, with higher spending on **gold** and **food items** such as **fish** and **fruits**.
- **Behavior**: These customers are budget-conscious but still make select purchases in higher-value categories, primarily focusing on food and gold.

### Key Insights:
- **Income** is the primary driver of spending patterns, with higher-income segments tending to spend more on luxury goods like **gold** and **wine**.
- **Family Size** also plays a significant role in spending patterns, with larger families prioritizing more practical and long-term investments.
- **Emotional/Cultural Factors**: In Cluster 3, the emphasis on **wine** may suggest cultural or psychological factors influencing their purchasing decisions.
  
These insights can be used to design targeted marketing strategies for each cluster to increase customer engagement and sales.

---

## :gear: How to Run the Project

# Running the Notebooks

To run the Jupyter Notebooks for this project, follow the steps below:

### 1. Clone or Download the Repository
Clone the repository to your local machine or cloud environment.

### 2. Install Dependencies
Install the required dependencies by running the following command in your terminal:

```bash
pip install -r requirements.txt
```
### 3. Running the Notebooks
After installing the dependencies, you can run the Jupyter notebooks sequentially as follows:

**3.1. Run 01_Data_Cleaning.ipynb**

Open 01_Data_Cleaning.ipynb in Jupyter Notebook or JupyterLab.

Execute each cell to perform data cleaning tasks, including handling missing values, duplicates, and outliers.

**3.2. Run 02_Feature_Engineering.ipynb**

After completing the data cleaning, move on to 02_Feature_Engineering.ipynb.

This notebook will guide you through creating and transforming new features from the cleaned data, such as age, spending, and family size.

**3.3. Run 03_Data_Processing.ipynb**

Finally, open 03_Data_Processing.ipynb.

This notebook will perform additional data processing steps such as scaling and dimensionality reduction (PCA), followed by clustering on the processed data.
