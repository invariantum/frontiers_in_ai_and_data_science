# What changed in each file

Upload `environment.yml` and the `content` folder to the top level of your repository.
This file is just for your reference; you don't need to upload it.


## `content/Week 1-7/Week 2/Lab_2/03-DataFrames.ipynb`
- df.xs(['G1',1]) -> df.xs(('G1',1))  (pandas now needs a tuple for multi-level keys)

## `content/Week 1-7/Week 2/Lab_2/05-Groupby.ipynb`
- by_comp.mean() -> by_comp.mean(numeric_only=True)
- df.groupby('Company').mean() -> .mean(numeric_only=True)
- by_comp.std() -> by_comp.std(numeric_only=True)

## `content/Week 1-7/Week 2/Lab_2/08-Data Input and Output.ipynb`
- read_excel(sheetname=...) -> read_excel(sheet_name=...)  (argument was renamed)
- HTML intro: replaced 'conda install' instructions with a note about the browser environment
- read_html from fdic.gov (needs internet) -> read_html from a local HTML file; result stored in `tables` so `df` stays a DataFrame for the SQL section
- df[0] -> tables[0]

## `content/Week 1-7/Week 3/Lab_3/data-prep-week-2-lecture-demo.ipynb`
- Kaggle path '../input/ecommerce-purchases/...' -> 'Ecommerce Purchases.csv' (the file next to the notebook)
- drop('c_price') ran before c_price is created (cells were run out of order) -> errors='ignore'

## `content/Week 1-7/Week 3/Lab_3/week-2-titanic-eda-example.ipynb`
- Kaggle path '../input/traindataset/train.csv' -> 'train.csv' (the file next to the notebook)
- CatBoost import -> falls back to scikit-learn gradient boosting when CatBoost is unavailable (browser)
- .iteritems() -> .items()  (3 places; iteritems was removed)
- apriori(...) now gets a True/False table (.astype(bool)); mlxtend is dropping support for 0/1 numbers

## `content/Week 1-7/Week 4/Lab_4/Associate_rule_mining_exercise_solution.ipynb`
- removed '!!pip install mlxtend' (mlxtend is pre-installed)
- apriori(...) now gets a True/False table (.astype(bool)); mlxtend is dropping support for 0/1 numbers
- sns.distplot -> sns.histplot(..., kde=True)  (distplot is deprecated)
- last cell contained pasted output, not code (SyntaxError) -> turned into a markdown note

## `content/Week 1-7/Week 7/Lab_7/Associate_rule_mining_exercise_solution.ipynb`
- removed '!!pip install mlxtend' (mlxtend is pre-installed)
- apriori(...) now gets a True/False table (.astype(bool)); mlxtend is dropping support for 0/1 numbers
- sns.distplot -> sns.histplot(..., kde=True)  (distplot is deprecated)
- last cell contained pasted output, not code (SyntaxError) -> turned into a markdown note

## `content/Week 1-7/Week 4/Lab_4/association-rule-mining-practice.ipynb`
- read_excel from archive.ics.uci.edu (needs internet, 23 MB) -> local CSV with France+Germany rows
- applymap -> map (applymap was removed in pandas 3); .astype(bool) is what mlxtend now expects
- applymap -> map for the Germany basket

## `content/Week 1-7/Week 7/Lab_7/association-rule-mining-practice.ipynb`
- read_excel from archive.ics.uci.edu (needs internet, 23 MB) -> local CSV with France+Germany rows
- applymap -> map (applymap was removed in pandas 3); .astype(bool) is what mlxtend now expects
- applymap -> map for the Germany basket

## `content/Week 1-7/Week 4/Lab_4/retail_dataset.csv`
- copied from Week 7/Lab_7 (the Week 4 notebook needs it)

## `content/00_Environment_Check.ipynb`
- Now also checks missingno, bs4, html5lib, sqlite3, sqlalchemy, and tests HTML and SQL round-trips

## `environment.yml`
- Added beautifulsoup4, soupsieve, html5lib, six, webencodings (for `pd.read_html`)
- Added sqlalchemy, typing-extensions (for `to_sql` / `read_sql`)
- Added missingno (Week 3 Titanic notebook)
## Kernel setting (all 24 notebooks in `Week 1-7`)
- Every notebook in `Week 1-7` is now set to the **Python (XPython)** browser kernel, so it opens without a "Select Kernel" prompt. Before, they were set to `python3` or even `python2`.
- `Extras` and `Week 15-16` were left alone on purpose: they need a GPU or libraries that can't run in a browser, so they belong on Colab.
