# MSCS_634_Lab_1: Data Visualization, Preprocessing, and Statistical Analysis

**Author:** Vishnu Mallam  
**Course:** Advanced Big Data and Data Mining  
**Assignment:** Lab 1 - Data Visualization, Preprocessing, and Statistical Analysis

## Purpose

This lab demonstrates the complete data science pipeline including data collection, visualization, preprocessing, and statistical analysis using Python in Jupyter Notebook. The project focuses on exploring sales data to extract meaningful insights through various analytical techniques.

## Dataset

- **Dataset:** Sales Data Sample (sales_data_sample.csv)
- **Original Size:** Multiple rows with comprehensive sales information
- **Encoding:** ISO-8859-1
- **Key Variables:** QUANTITYORDERED, SALES, PRICEEACH, MSRP, DEALSIZE, and various location/customer attributes


```

## Key Insights

### 1. Data Visualization Insights

- **Scatter Plot (Quantity vs Sales):** Reveals a positive relationship between quantity ordered and sales amount, indicating that larger orders generally generate higher revenue.

- **Histogram (Sales Distribution):** Shows the distribution of sales amounts, revealing the concentration of sales values and identifying the most common sales ranges.

### 2. Data Quality Assessment

- **Missing Values Handled:**
  - ADDRESSLINE2: Filled with 'Not Available'
  - STATE: Filled with 'Unknown'
  - POSTALCODE: Forward fill method applied
  - TERRITORY: Filled with 'Unassigned'

- **Outlier Management:**
  - Used IQR method for outlier detection in SALES column
  - Identified and removed extreme outliers for cleaner analysis
  - Maintained data integrity while improving statistical reliability

### 3. Data Preprocessing Results

- **Data Reduction:** Successfully reduced dataset to 70% through sampling while maintaining representativeness
- **Dimension Reduction:** Removed less relevant columns (ADDRESSLINE2, PHONE, contact names) to focus on key business metrics
- **Scaling:** Applied Min-Max scaling to numerical variables for standardization
- **Discretization:** Converted continuous SALES data into meaningful categories (Low, Medium, High)

### 4. Statistical Analysis Findings

#### Central Tendency Measures
- Calculated comprehensive statistics including mean, median, and mode for all numerical variables
- Identified key business metrics ranges and typical values

#### Dispersion Measures
- Computed variance, standard deviation, and IQR for understanding data spread
- Analyzed quartiles to understand data distribution patterns

#### Correlation Analysis
- Generated correlation matrix to identify relationships between variables
- Discovered significant correlations between key business metrics
- Created heatmap visualization for easy interpretation of variable relationships

## Technical Implementation

### Libraries Used
- **pandas:** Data manipulation and analysis
- **numpy:** Numerical computing
- **matplotlib:** Basic plotting and visualization
- **seaborn:** Statistical data visualization
- **scipy:** Statistical functions
- **sklearn:** Machine learning preprocessing tools

### Key Techniques Applied
1. **Data Loading:** Proper handling of encoding issues
2. **Missing Value Imputation:** Multiple strategies based on data type and context
3. **Outlier Detection:** IQR-based method for robust outlier identification
4. **Data Scaling:** Min-Max normalization for feature standardization
5. **Statistical Analysis:** Comprehensive descriptive statistics computation

## Challenges and Solutions

### Challenge 1: Missing Data Handling
- **Issue:** Multiple columns had missing values with different patterns
- **Solution:** Applied context-appropriate imputation strategies for each column type

### Challenge 2: Outlier Detection
- **Issue:** Determining appropriate outlier removal threshold
- **Solution:** Used IQR method with 1.5 * IQR rule for balanced outlier removal

### Challenge 3: Data Reduction
- **Issue:** Maintaining data representativeness while reducing size
- **Solution:** Used random sampling with fixed seed for reproducibility

### Challenge 4: Visualization Clarity
- **Issue:** Large dataset making scatter plots cluttered
- **Solution:** Applied alpha transparency and appropriate figure sizing

## Key Decisions Made

1. **Outlier Removal:** Chose to remove rather than transform outliers to ensure cleaner statistical analysis
2. **Sampling Strategy:** Used 70% random sampling to balance computational efficiency with data completeness
3. **Scaling Method:** Selected Min-Max scaling over standardization for interpretability
4. **Discretization:** Used quantile-based binning for balanced category creation

## Results Summary

- **Data Quality:** Successfully cleaned dataset with 100% missing value resolution
- **Outlier Management:** Removed identified outliers while preserving data integrity
- **Statistical Insights:** Generated comprehensive statistical profile of the dataset
- **Visualization:** Created informative plots revealing key data patterns and relationships

## Future Work

- Implement advanced outlier detection methods (Isolation Forest, Local Outlier Factor)
- Explore feature engineering opportunities
- Apply clustering analysis for customer segmentation
- Develop predictive models using the preprocessed data

## How to Run

1. Clone the repository
2. Install required libraries: `pip install pandas numpy matplotlib seaborn scipy scikit-learn`
3. Open `Lab1_Data_Analysis.ipynb` in Jupyter Notebook
4. Run all cells sequentially
5. Review generated visualizations and statistical outputs

## Screenshots

All required screenshots are organized in the `/screenshots` folder:
- Dataset head display
- Data visualizations (scatter plot, histogram)
- Before/after missing value handling
- Outlier detection and removal process
- Data reduction results
- Scaling and discretization outputs
- Statistical analysis results
- Correlation matrix heatmap

---

**Note:** This project demonstrates fundamental data science techniques essential for any data-driven analysis. The methodology can be adapted and scaled for larger, more complex datasets in real-world applications.
