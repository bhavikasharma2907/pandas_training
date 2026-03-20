🐼 Pandas Tutorial: Data Analysis in Python

This repository demonstrates the use of Pandas, a powerful Python library for analyzing, cleaning, and manipulating structured data in tabular form. It covers DataFrame creation, basic operations, filtering, handling missing values, and working with dates.

📌 Features

Create DataFrames from lists or dictionaries

Inspect data using head(), tail(), shape, columns, and info()

Perform row and column operations (add, update, delete)

Filter data using conditions (loc, where)

Handle missing values and NaNs

Work with dates using pd.to_datetime() and Timedelta

Save and load CSV files

🛠️ Installation
!pip install pandas

Check version:

import pandas as pd
print(pd.__version__)
💻 Example Code
Create DataFrame
import pandas as pd

data = {'Name':['Madhav','Vishakha','Lalita','Hrishabh'],
        'age':[16,17,18,19],
        'salary':[90000,70000,80000,50000]}
df = pd.DataFrame(data)
print(df)
Basic Operations
df.head(2)           # First 2 rows
df.tail(2)           # Last 2 rows
df.rename(columns={'salary':'Monthly_salary'}, inplace=True)
df['Bonus'] = df['Monthly_salary']*0.2
df['DOJ'] = pd.to_datetime(['2024-01-01','2024-01-15','2024-03-28','2024-03-03'])
Filtering
df[df['age']>=18]
df[(df['age']>=18) & (df['Monthly_salary']>=50000)]
Save & Load CSV
df.to_csv('Test_data.csv', index=False)
load_df = pd.read_csv('Test_data.csv')
📖 Learning Outcomes

DataFrame creation and inspection

Row and column selection and operations

Filtering and conditional operations

Handling missing values and dates

Reading and writing CSV files

👨‍💻 Author

Bhavika Sharma
