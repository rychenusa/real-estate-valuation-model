# Math 148 Capstone Project, Group 1

The original dataset can be accessed here: https://archive.ics.uci.edu/dataset/555/apartment+for+rent+classified  <br />
It's from the UCI repository.

## What are in the datasets?
`NRI_Table_Counties.csv`: risk scores and ratings by county and state<br />
Obtained from: https://hazards.fema.gov/nri/data-resources  <br /><br />

`Unemployment and median household income for US (States, and counties, 2000–22).csv` is self-explanatory<br />
Obtained from: https://www.ers.usda.gov/data-products/county-level-data-sets/county-level-data-sets-download-data  <br /><br />

`arizona.csv`, `california.csv`, `nevada.csv`, `oregon.csv`, `washington.csv`: matching up the counties, states, and zipcodes for our selection of 5 western states<br />
Obtained from
- https://www.azleague.org/199/Arizona-City-Town-Data
- https://data.ca.gov/dataset/california-incorporated-cities
- https://www.gigasheet.com/sample-data/spreadsheet-list-of-all-cities-in-nevadacsv
- https://data.oregon.gov/Business/Oregon-City-Zipcode-Counties/g44a-nzix/about_data
- https://data.wa.gov/demographics/Washington-State-Cities-and-Counties/g2kf-7usg/about_data
<br /><br />

`avg_temperature_by_county.csv`: average temperature by county<br />
Obtained from: https://www.ncei.noaa.gov/access/monitoring/climate-at-a-glance/county/mapping/110/tavg/201712/24/value  <br /><br />

`crime_in_US_2017.xls`, `crime_in_US_2018.xls`, `crime_in_US_2019.xls`: crime rates across 3 years<br />
Obtained from
- https://ucr.fbi.gov/crime-in-the-u.s/2019/crime-in-the-u.s.-2019/topic-pages/tables/table-6
- https://ucr.fbi.gov/crime-in-the-u.s/2018/crime-in-the-u.s.-2018/topic-pages/tables/table-6
- https://ucr.fbi.gov/crime-in-the-u.s/2017/crime-in-the-u.s.-2017/topic-pages/tables/table-6
<br /><br />

`zip_code_demographics.csv`: Distance to highway, a large airport, medium airport,	and shore,	number of businesses, adjusted gross income,	and total income.<br />
Obtained from: https://www.kaggle.com/datasets/erdi28/zip-codes-demographics

## Main Dataset Construction

`data_merged.Rmd` : This R Markdown file performs additional preprocessing and cleaning on the aggregated datasets. It then merges these datasets to create a comprehensive dataset that integrates information from all available sources.

## Exploratory Data Analysis

`EDA_compiled.ipynb`:  This notebook performs an exploratory data analysis (EDA) on the compiled dataset to understand its structure, distribution, and key characteristics. The analysis includes data cleaning, summary statistics, outlier detection, and visualizations to gain insights into the dataset.  

### 1. **Data Distribution Analysis**  
- Summary statistics such as mean, median, and standard deviation are computed.  
- The presence of missing values is checked.  

### 2. **Outlier Detection**  
- The dataset is examined for outliers using statistical measures.  
- Boxplots and histograms are used to visualize outliers.  

### 3. **Feature Analysis and Correlations**  
- Relationships between numerical features are explored using correlation matrices.  
- Heatmaps are generated using `seaborn` to highlight correlated variables.  

### 4. **Data Visualization**  
- Various visualizations, including histograms, scatter plots, and boxplots, are created to better understand feature distributions.  
- `matplotlib` and `seaborn` are used for visualizations.  

### 5. **Handling Missing Data**  
- Strategies such as imputation or dropping missing values are used.  
  

## Model Development and Results

`M148_model_development.ipynb`: This notebook develops a machine learning model to predict apartment rental prices based on various features. The analysis includes data preprocessing, feature selection, model training, and evaluation using regression techniques. 

### 1. **Data Preprocessing**  
- Encoding categorical features using `OneHotEncoder`.  
- Standardizing numerical features using `StandardScaler`.  

### 2. **Feature Selection and Engineering**  
- Identifying relevant variables for the model.  
- Creating new features if necessary.  

### 3. **Model Training and Hyperparameter Tuning**  
- Splitting data into training and test sets using `train_test_split`.  
- Training models.
- Using `GridSearchCV` to optimize hyperparameters.  

### 4. **Model Evaluation**  
- Assessing model performance using Mean Squared Error (MSE) and $R^2$.  
- Visualizing model predictions versus actual values.  

### Running the Notebook  
1. Ensure the dataset (`no_nas_master_dataset.csv`) is available in the working directory.  
2. Run all cells sequentially to execute the analysis and train the model.  




