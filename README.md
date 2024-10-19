# Housing Price Prediction Project

## Authors
- **Jiaqi(Scarlett) He**
- **Zhehong Lim**
- **Yangchang Liang**

## Content
1. Data Cleaning
2. Exploratory Data Analysis
3. Modeling
4. Diagnostics

## Data Cleaning

### Cleaning Process
- Converted binary and categorical variables to dummy variables
- Resulted in a cleaned dataset ready for analysis

## Exploratory Data Analysis

### Correlation Matrix
- Examined linear relationships between predictors
- Identified that the number of bedrooms likely to be an insignificant predictor

## Modeling

### Basic Model
- Initial model included variables such as bedrooms and status of furnishing
- P-values indicated some predictors were not significant

### Reduced Model
- Removed features with high p-values: bedrooms, semi-furnished, furnished, and guestroom

### Scaled Model
- Applied scaling: 
  - Price ~ 10^7
  - Area ~ 10^4
  - Bedrooms < 10

### Logged Model
- Conducted log transformation due to right-skewed price distribution
- Transformation was effective, resulting in a high R² value
- Confirmed bedrooms were not necessary in the model after log transformation


## Diagnostics

- Used `par()` function for initial analysis
- Identified and dropped outliers (rows 1, 3, 5, 16)
- Developed a reduced model with outliers dropped

### Model Analysis
- Predictors with high variance were identified, indicating wide range of area and price
- Considered potential solutions such as scaling and log transformation

## Conclusion
- No high correlation between any two predictors
- Bedrooms showed a linear relationship with price but were not necessary in the final model
- Reduced model improved prediction accuracy
- Log transformation of the model yielded excellent results

## Repository Contents

- `Housing Price Prediction Slides.pdf`: Presentation slides for the project
- `Housing.Rmd`: R Markdown file for the analysis and modeling
- `Housing.csv`: Contains the datasets used for analysis.

## References
- [Kaggle: Multiple Linear Regression Housing Price Detection](https://www.kaggle.com/datasets/gauravbr/multiple-linear-regression-housing-price-detection)
