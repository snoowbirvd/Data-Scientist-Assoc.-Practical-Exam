# DSA Practical Exam
Dataset: [HouseSales.csv](https://github.com/snoowbirvd/Data-Scientist-Assoc.-Practical-Exam/blob/62cdec419d676ac7ebe4ba0650c76f2b9befa1ad/house_sales.csv)

**Project Instructions:**
- Use Python to perform each of the tasks (5 Tasks).
- The object you have been asked to create will be graded, not the code.
- Ensure you match any column name or object requirements.
- Only 2 opportunities to submit the exam for grading
- You must be successful in all tasks to pass this exam
- The fit of your models will be compared to held back values from the test set provided to you. We will calculate the Root Mean Squared Error of your predictions.
- At least one of your two models must have a Root Mean Squared Error below 30,000 to pass
  

### Initial Data Assessment
**My Approach**: 2 things I practice before diving into the specific tasks
1. Understanding the overall goal of this project (to properly absorb the approach and learnings to this case)
   - Task 1 & 2 is about cleaning and preparing the dataset for reliable analysis
   - Task 3 is exploring the relationship between house features (e.g., bedrooms, area, location) and sale price
   - Rask 4 & 5 is building a baseline predictive model to estimate sale prices based on available features
   - In perspective, this is to help optimize the listing prices of houses by predicting house sale prices based on their characteristics
   
2. Conducting a comprehensive dataframe inspection to have an overview of the data variables

### Task 1 & 2:  Identify and replace missing values/Clean categorical and text data by manipulating strings/Convert values between data types.
**My Assessment & Strategy**:
1. **Holistic Inspection Approach**
   - Performed a for loop column-by-column quality analysis (I include unique values, potential missing value patterns, capitalization and spelling Analysis for object types, statistics for numeric columns)

   **Data Issues Identified:**
   - `city` column contained placeholder values (`'--'`) indicating missing data.
   - `house_type` column had inconsistent abbreviations for house types (e.g. semi:semi-detached, det:detached)
   - `area` column stored numerical values as strings with units (`'sq.m.'`), making them unsuitable for analysis.
   - `months_listed` column had (`'nan'`) missing values pattern.
   - `sale_date` column needed to ensure proper datetime formatting.
  
   - After cleaning (via data imputation, string replacement and mapping and type conversion), I performed after inspection analysis to verify clean data
     
### Task 3: Aggregate numeric, categorical variables and dates by groups
  - The task already advised that the number of bedrooms is the biggest driver of house price, so we don't have to do any EDA or addtional regression analysis
  - This is the easiest task for me :). Actually, GPT 4 can accurately handle this with little guidance
    
**My Approach**:
  Store in dataframe called `price_by_rooms`
   - groupby("bedrooms")
   - agg. the "sales price" by mean and variance and round the results by 1
     
In perspective, the goal of this task was to investigate the relationship between the number of bedrooms and house prices, focusing on two key metrics:
1. **Average Sale Price (`avg_price`)**: Helps determine the typical price of houses based on the number of bedrooms.
2. **Variance in Sale Price (`var_price`)**: Indicates the spread or variability of house prices within each bedroom category.

### Tasks 4 & 5: Model Implementation
**My Approach to Modeling**:
1. **Pre-modeling Analysis**
   - Feature selection based on cleaned data
   - Split data ensuring representative samples
   - Established baseline metrics

2. **Model Strategy**
   - Focus on achieving RMSE < 30,000
   - Selected models suitable for housing price prediction
   - Implemented cross-validation for robust evaluation

## Key Insights and Decisions
1. **Data Quality**
   - Missing data patterns varied significantly by column
   - Text standardization was crucial for accurate analysis
   - Date formats needed careful handling

2. **Modeling Considerations**
   - Feature engineering importance
   - Balance between model complexity and performance
   - Focus on RMSE optimization

## Lessons Learned
1. **Data Cleaning**
   - Importance of thorough initial data inspection
   - Value of systematic pattern detection
   - Need for column-specific cleaning approaches

2. **Model Development**
   - Feature selection impact on RMSE
   - Importance of validation strategy
   - Balance of model complexity vs performance

## Future Improvements
- Enhanced missing value detection patterns
- More sophisticated text standardization
- Additional feature engineering possibilities
