# DSA Practical Exam
Dataset: [HouseSales.csv](https://github.com/snoowbirvd/Data-Scientist-Assoc.-Practical-Exam/blob/62cdec419d676ac7ebe4ba0650c76f2b9befa1ad/house_sales.csv)

**Project Instructions:**
- The object you have been asked to create will be graded, not the code.
- Ensure you match any column name or object requirements.
- The fit of your models will be compared to held back values from the test set provided to you. We will calculate the Root Mean Squared Error of your predictions.
- At least one of your two models must have a Root Mean Squared Error below 30,000 to pass
- All required data has been created and has the required columns
- 2 Attempts to submit and grade 

### Initial Data Assessment
**My Approach**: Before diving into specific tasks, I analyzed the overall goal of this project (although, its not the focus of the test, it's important that we com

Goal: To help RealAgents optimize the listing prices of houses by predicting house sale prices based on their characteristics. By achieving this, RealAgents can reduce the time required to sell houses and improve competitiveness. This involves:

- Cleaning and preparing the dataset for reliable analysis.
- Exploring the relationship between house features (e.g., bedrooms, area, location) and sale price.
- Building a baseline predictive model to estimate sale prices based on available features.

Also, I conducted a comprehensive data quality inspection to:
- Verify all required columns exist with correct data types
- Understand the nature and extent of data quality issues
- Plan the cleaning strategy based on actual data patterns

### Task 1: Missing Value Identification and Treatment
**My Assessment & Strategy**:
1. **Holistic Inspection Approach**
   - Performed column-by-column quality analysis
   - Discovered non-standard missing value patterns (e.g., dashes, N/A variations)
   - Found that missing values weren't just NULL/NaN but included:
     - Empty strings
     - Various dash patterns (-, --, - -)
     - Different NA formats (NA, N/A, na)

2. **Column-Specific Findings**
   - Numeric columns: Found both NULL values and potential placeholder zeros
   - Text columns: Discovered multiple missing value representations
   - Date columns: Identified invalid date formats and missing timestamps

3. **Treatment Strategy**
   - Used column-appropriate replacement methods
   - Considered data distribution when replacing values
   - Documented all replacements for reproducibility

### Task 2: Data Cleaning and Type Conversion
**My Assessment & Approach**:

1. **String Data Cleaning**
   - Found inconsistencies in:
     - Capitalization (NEW YORK, New york, new York)
     - Spelling variations (Appartment vs Apartment)
     - Extra spaces and special characters
   - Standardized text formatting for consistency

2. **Data Type Conversion Challenges**
   - Identified mixed format dates
   - Found numeric values stored as text
   - Discovered categorical variables needing encoding

### Task 3: Data Aggregation
**My Strategy**:
- Identified logical grouping variables
- Determined appropriate aggregation methods per column
- Validated aggregated results for business sense

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
