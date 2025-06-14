# IMDB-Dataset-Cleaning

This repository contains the full data cleaning process applied to a messy IMDB dataset.  
The cleaning has been performed **separately using both Excel and Pandas**, demonstrating data wrangling skills in both manual and programmatic environments.

### Why This Project?
- Demonstrates ability to handle messy real-world datasets.
- Shows both manual data wrangling (Excel) and programmatic data cleaning (Python).
- Prepares clean dataset ready for EDA, visualization, or machine learning.

## Project Structure

```bash
IMDB-Dataset-Cleaning/
│
├── raw_data/
│   └── messy_IMDB_dataset.csv           # Original messy dataset
│
├── cleaned_data/
│   ├── Cleaned-csv.csv             # Cleaned manually using Excel
│   └── Cleaned-excel.xlsx            # Cleaned programmatically using Pandas
│
├── scripts/
│   └── messy.ipynb            # Full pandas cleaning code
│
└── README.md                            # Project documentation
```

### Excel Cleaning

- Corrected column names and removed any special characters or extra spaces.
- Standardized formats of incorrectly formatted columns:
  - Converted `INCOME` and `VOTES` columns to numeric by removing `$`, `,`, and `.` separators.
  - Converted `Duration` column into proper `hr:min:sec` format.
  - Adjusted `RELEASE YEAR` formats where possible.
- Handled missing values using Excel formulas:
  - Used `MEAN` (AVERAGE) function to fill missing `SCORE` values.
  - Used `MEAN` function to fill missing `DURATION` values.
  - Used `MODE` function wherever applicable for categorical columns.
  - Manually verified and corrected rows with invalid entries.
- Saved fully cleaned dataset into `Cleaned-excel.xlsx`.

### Pandas Cleaning
- Loaded data using:
  - pd.read_csv() with custom delimiter (;) and encoding (ISO-8859-1).
- Removed special characters ($, ,, .) from fields like INCOME and VOTES.
- Converted columns to appropriate numeric types using pd.to_numeric().
- Converted RELEASE YEAR to datetime using pd.to_datetime() with error handling.
- Handled missing values:
- Filled missing SCORE with column mean.
- Filled missing DURATION with column mean (rounded to 1 decimal place).
- Manually fixed specific corrupted rows using iloc.
- Exported cleaned file as CSV.

### Tools & Technologies Used
- Excel — Manual cleaning, formulas, formatting.
- Python — Programmatic cleaning.
  - pandas
  - numpy
- Jupyter Notebook — For step-by-step cleaning & visualization.
- Git & GitHub — Version control and hosting.

### **Clone the repository**
   ```bash
   git clone https://github.com/AshishRaj97/IMDB-Dataset-Cleaning.git
   cd IMDB-Dataset-Cleaning
   ```

##  Author
- **Ashish Raj**
- [LinkedIn](https://in.linkedin.com/in/ashish-raj-327596306)
