# Python-Project-2
# Project Description: Organisational Data Analysis

This project processes a CSV file containing information about organisations and performs various statistical analyses on the data. The goal is to extract insights such as T-scores, Minkowski distances, and profit changes, while handling missing or invalid data points. The project includes functions that handle file processing, compute statistical metrics, and rank organisations within different categories.

## Functions Overview:

### 1. `file_processing(csvfile)`
   - This function reads a CSV file and processes its contents into a dictionary. Each row is represented by a dictionary with column headers as keys.
   - It ensures that numerical data is correctly typed, converts non-numeric values to 'null', and handles missing data. The first column value is used as the primary key.
   - If the file is empty or cannot be processed, it returns `None`.

### 2. `t_testscore(data)`
   - This function calculates T-scores to compare the profits of organisations between 2020 and 2021 for each country.
   - It performs a T-test on the profit data, skipping rows where data is missing or invalid. The results are returned as a dictionary with countries as keys and T-scores as values.
   
### 3. `minkowski_distance(data)`
   - This function calculates the Minkowski distance (with an order of 3) between the number of employees and the median salary for each country.
   - It processes the data to remove duplicates and invalid entries, then calculates and returns the Minkowski distance for each country.

### 4. `answer2(data)`
   - This function calculates the percentage change in profits between 2020 and 2021 for each organisation, grouped by category.
   - It ranks organisations within each category based on the number of employees and profit change, returning the final ranked data.

### 5. `main(csvfile)`
   - The main function integrates all the above functions, orchestrating the flow of data processing and analysis.
   - It reads the CSV file, processes the data, and computes the T-scores, Minkowski distances, and profit changes.
   - The results are returned as two dictionaries: one for statistical metrics (T-scores and Minkowski distances) and another for ranked organisation data.
   - If the file is not found or the data is invalid, it returns empty dictionaries.

### Usage:

1. Provide a CSV file with relevant organisation data (e.g., organisation ID, country, number of employees, profits for 2020 and 2021, etc.).
2. The main function will process the data and return insights in the form of T-scores, Minkowski distances, and ranked categories of organisations.

### Key Features:
- **T-scores**: Measure the statistical significance of profit differences between 2020 and 2021 for each country.
- **Minkowski distance**: Provides a metric that compares the number of employees and median salary for organisations within each country.
- **Profit change analysis**: Calculates the percentage change in profits between 2020 and 2021 for organisations, with rankings based on employee numbers and profit changes.
- **Data handling**: The project automatically skips invalid, missing, or duplicate data entries, ensuring that the results are accurate and reliable.

### Insights:
- **Country-specific T-scores**: Determine how significant the profit differences are between 2020 and 2021 for organisations in different countries.
- **Minkowski distances**: Compare the difference between number of employees and median salary for organisations in each country.
- **Ranked categories**: Understand how organisations are performing within their category, based on employee size and profit growth.

This project provides valuable tools for analysing organisational performance and profitability across different regions and categories, ensuring comprehensive insights into the data.
