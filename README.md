# E-commerce Business Analysis

## Project Overview

This project aims to analyze customer data from an e-commerce business to find effective ways to increase sales. The data includes customer information, product preferences, and sales data. The project focuses on data cleaning, preprocessing, and visualization to provide insights into customer behavior and sales trends.

Imagine a fruit shop within a supermarket that operates without a shopkeeper. If a customer wants to buy some fruit, they can enter their information (such as name, phone number, address, and whether they would like to be `contact later` for offers or discounts) into a dashboard. After payment, the fruit(s) will be automatically packaged using robotics, and the customer can pick it up from a tray.

The dataset for this project is named `customer_data.csv`.

Our primary focus is on `data cleaning` because only the necessary and relevant data should be used for analysis.

By analyzing customers' previous buying data, we can identify products with poor or strong sales each month. This allows us to offer those products to customers who have shown interest in being contacted later for offers. We can reach out to these customers via their `Gmail address` or `phone number`.

## Data Preprocessing

### Initial Data Inspection

- **Shape of Data**: The dataset contains multiple rows and columns with various customer and product details.
- **Summary Statistics**: The data was examined for summary statistics such as mean, median, standard deviation, etc.
- **Data Types**: Each column's data type was inspected, and non-null values were counted.
- **Duplicate Data**: Duplicate rows were identified and removed from the dataset.
- **Missing Values**: The count of missing values was checked across all columns.

### Data Cleaning

1. **Customer ID**: The `Customer ID` column had inconsistent formatting (e.g., "1 || CusID- 2"). The data was cleaned to contain only numeric values.
2. **Last Name**: The `Last Name` column contained unexpected symbols (e.g., `_`, `|`, `...`). These were stripped out to clean the data.
3. **Gender**: The `Gender` column had inconsistent entries (e.g., "Male", "M", "m", "Female", "F", "f"). The data was standardized to "Male" and "Female".
4. **Phone Number**: The `Phone Number` column contained various symbols (e.g., `-`, `\`, `|`). The data was cleaned to a consistent format (e.g., "123-456-7890").
5. **Address**: The `Address` column was split into separate columns for `State`, `Street`, and `Zip Code`. The original `Address` column was then removed.
6. **Contact Later**: The `Contact Later` column had inconsistent entries (e.g., "Yes", "Y", "y", "No", "N", "n"). The data was standardized to "YES" and "NO".

## Data Visualization

### Gender Distribution
- A count plot was generated to show the distribution of male and female customers.
- ![Male_Female_count](https://github.com/user-attachments/assets/3321a553-d529-45cf-b6a6-3095a851b177)


### Fruit Preferences
- **Fruit vs Price State**: The data was grouped by fruit and visualized to show how many males and females participated in purchasing each fruit.
- ![Fruit vs price with male and female counter](https://github.com/user-attachments/assets/31267b64-771e-4c3c-95a0-ee40019e1b59)
- **Density Graph**: A density plot was created for each fruit to show the price distribution.
- ![Density Graph](https://github.com/user-attachments/assets/7ef973cc-a21b-40d6-8ecd-b8cb5d637a66)


### Date and Time Analysis
- The dataset was sorted by `Date` and `Time` to analyze price trends over different periods.

### Country vs Fruit Sales
- Bar plots were created to visualize how different fruits are sold across various countries.
- ![Apple country VS Fruit](https://github.com/user-attachments/assets/641df486-5957-4b2b-be71-c4cbd3dc2589)
- ![Banana country VS Fruit](https://github.com/user-attachments/assets/45d82b24-667d-4583-9e07-9b69496e3b20)


### Male and Female Count per Fruit
- A bar chart was created to count the number of males and females who purchased each fruit.
- ![male female counter for each fruit](https://github.com/user-attachments/assets/e0ba00d1-9a38-4a64-b247-cfec167f50f2)


### Monthly Frequency Analysis
- The frequency of each fruit's sales was analyzed on a monthly basis.
- ![Blueberry month VS Fruit](https://github.com/user-attachments/assets/ce063b27-c076-4776-b39e-c68a00d5b00c)
- ![Apple month VS Fruit](https://github.com/user-attachments/assets/83667781-81b1-48a1-986c-41d09b6e8465)


## Saving Cleaned Data

- The cleaned dataset was saved as a new CSV file (`final_Customer_data.csv`).
- Separate CSV files were created for each fruit in `Fruit` directory, containing relevant customer information and product details.

## Project Requirements

To run this project, the following Python libraries are required:

- `pandas`
- `matplotlib`
- `seaborn`
- `plotly`

You can install the required libraries using the following commands:

```bash
pip install pandas
pip install matplotlib
pip install seaborn
pip install plotly
```



