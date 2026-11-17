# Superstore Sales Analysis

A sales exploration project based on the Sample - Superstore dataset, using Python and Jupyter. The notebook analyzes sales, profits, customers, products, regions, and time-based trends.

## Project Structure

```text
.
|-- data/
|   `-- superstore.csv
|-- notebooks/
|   `-- analyse_superstore.ipynb
|-- visualization/
|   `-- .gitkeep
|-- .gitignore
|-- README.md
`-- requirements.txt
```

The local virtual environment (`myenv/`) is not included in the shared project. It is ignored by Git.

## Installation

From the project root directory, create a virtual environment and install the dependencies:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

In VS Code, select this Python environment and open `notebooks/analyse_superstore.ipynb`.

## Data and Execution

The `data/superstore.csv` file is provided. The notebook reads the file without downloading or modifying it. Run the notebook cells in order, either from the project root directory or from the `notebooks/` directory.

To launch Jupyter from the project root directory:

```powershell
jupyter notebook notebooks/analyse_superstore.ipynb
```

## Analyses

- Data quality and structure: data types, missing values, duplicates, and dates.
- Overall metrics: sales, profits, margins, orders, and customers.
- Comparisons by category, sub-category, region, segment, and shipping mode.
- Descriptive comparison of sales and profit margins based on discount rates.
- Time-based trends and exploratory visualizations.

The notebook saves the generated charts as PNG files in `visualization/`. Discount comparisons are descriptive and do not establish a cause-and-effect relationship.