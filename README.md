# IMDb Dataset Cleaning: Excel and Pandas

A data-cleaning exercise using a messy IMDb dataset, with two separate workflows: one in Microsoft Excel and another in Python with Pandas.

The purpose is to show how inconsistent formats, missing values, and invalid entries can be identified and handled before exploratory analysis.

## Project structure

~~~text
IMDB-Dataset-Cleaning/
├── raw_data/
│   └── messy_IMDB_dataset.csv
├── cleaned_data/
│   ├── Cleaned-csv.csv
│   └── Cleaned-excel.xlsx
├── scripts/
│   └── messy.ipynb
└── README.md
~~~

## Cleaning workflow

### Excel

- Standardizing column names and removing unwanted spaces or characters.
- Cleaning numeric fields such as income and votes.
- Standardizing duration and release-year formats where possible.
- Handling missing values with spreadsheet formulas.
- Reviewing and correcting selected invalid records.
- Exporting the cleaned result to an Excel workbook.

### Python and Pandas

- Reading a semicolon-delimited CSV with an explicit encoding.
- Removing unwanted symbols from numeric fields.
- Converting columns with pandas.to_numeric().
- Parsing release-year values with pandas.to_datetime() and error handling.
- Handling missing score and duration values.
- Reviewing selected corrupted rows.
- Exporting the cleaned dataset to CSV.

## Tools used

- Microsoft Excel
- Python
- Pandas
- NumPy
- Jupyter Notebook

## Run the notebook

~~~bash
git clone https://github.com/AshishRaj97/IMDB-Dataset-Cleaning.git
cd IMDB-Dataset-Cleaning
pip install pandas numpy jupyter
jupyter notebook
~~~

Open scripts/messy.ipynb and update the input and output paths if your local folder structure differs.

## Data quality note

Imputation choices can affect downstream analysis. Mean imputation is used in parts of this exercise for numeric columns, but it is not always the best choice: the distribution, missingness mechanism, and purpose of the analysis should be considered before selecting an imputation strategy.

## Author

**Ashish Raj** · [GitHub](https://github.com/AshishRaj97) · [LinkedIn](https://www.linkedin.com/in/ashish-raj-327596306/)
