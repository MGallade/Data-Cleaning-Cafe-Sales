Restaurant Sales Data Cleaning Project

Overview
This project focuses on cleaning a restaurant transaction dataset containing 10,000 rows sourced from Kaggle. The dataset included missing values, inconsistent formats, and invalid entries. The goal was to clean and standardize the data so it can be used for analysis or machine learning.

Dataset
Source: Kaggle
Size: 10,000 rows

Columns:
Transaction ID
Item
Quantity
Price Per Unit
Total Spent
Payment Method
Location
Transaction Date

Data Cleaning Steps

1. Item Column
Invalid values such as 'Unknown' and 'Error' were removed.
Text was cleaned using strip() to remove spaces and capitalize() to standardize format.

2. Quantity Column
Converted to numeric using pd.to_numeric(errors='coerce').
Invalid values like 'ERROR' and 'UNKNOWN' were converted to null and handled.

3. Price Per Unit
Missing values were filled using a predefined price dictionary based on item names.
Ensured correct mapping after cleaning item names.

4. Total Spent
Validated using the formula:
Total Spent = Quantity * Price Per Unit
Incorrect values were recalculated where necessary.

5. Payment Method
Standardized values such as Cash, Card, and Digital Wallet.
Missing values were filled using the most frequent method (mode).

6. Location Column
Cleaned formatting inconsistencies.
Handled missing or invalid entries.

7. Transaction Date
Converted to datetime using pd.to_datetime(errors='coerce').
Invalid values such as 'ERROR' were converted to null and handled.

Price List Used

Coffee      2
Tea         1.5
Sandwich    4
Salad       5
Cake        3
Cookie      1
Smoothie    4
Juice       3

Key Outcomes
All major inconsistencies and invalid values were removed.
Categorical data was standardized.
Numerical columns were converted to proper data types.
Dataset is now clean and ready for analysis or machine learning.

Tech Stack
Python
Pandas
NumPy

Conclusion
This project demonstrates essential data cleaning techniques such as handling missing values, correcting data formats, and ensuring consistency across columns. These steps are necessary before performing any meaningful data analysis or building models.
