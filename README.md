# California Housing Dataset Exploration

## Overview
This project performs an initial exploratory data analysis (EDA) on the California Housing Prices dataset. The notebook loads the data, inspects its structure, and visualizes distributions using histograms.

## Dataset
The dataset (`housing.csv`) is the California Housing Prices dataset, containing 20,640 samples with 10 attributes:
- **Features** (9 numerical): 
  - longitude
  - latitude
  - housing_median_age
  - total_rooms
  - total_bedrooms (has 207 missing values)
  - population
  - households
  - median_income
  - median_house_value (target variable)
- **Categorical**: ocean_proximity (values: <1H OCEAN, INLAND, NEAR OCEAN, NEAR BAY, ISLAND)

This dataset is commonly used for regression tasks to predict median house values based on census data.

## Project Structure
- **Housing Dataset Exploration.ipynb**: Jupyter notebook containing the code for data loading, inspection, and visualization.
- **housing.csv**: The dataset file (not included in this repository; download from sources like Kaggle or scikit-learn datasets).

## Prerequisites
To run the notebook, install the required Python libraries:
```bash
pip install pandas matplotlib
```

## Steps in the Notebook
1. **Data Loading**:
   - Load the dataset into a pandas DataFrame from `housing.csv`.
   - Display the first few rows using `head()`.

2. **Data Inspection**:
   - Use `info()` to show data types, non-null counts, and memory usage (reveals missing values in total_bedrooms).
   - Use `value_counts()` on `ocean_proximity` to see category distributions.

3. **Data Visualization**:
   - Generate histograms for all numerical columns using `hist()` with 50 bins to visualize distributions.

## Results
- The dataset has 20,640 entries.
- `ocean_proximity` categories: <1H OCEAN (9136), INLAND (6551), NEAR OCEAN (2658), NEAR BAY (2290), ISLAND (5).
- Histograms provide insights into feature distributions, such as skewed median_house_value and varying scales across features.

## How to Run
1. Clone this repository:
   ```bash
   git clone <repository-url>
   ```
2. Place the `housing.csv` dataset in the appropriate directory.
3. Open the Jupyter notebook:
   ```bash
   jupyter notebook Housing Dataset Exploration.ipynb
   ```
4. Run all cells to reproduce the EDA.

## License
This project is licensed under the MIT License.
