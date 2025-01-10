# DSA Practical Exam
Dataset: [HouseSales.csv](https://github.com/snoowbirvd/Data-Scientist-Assoc.-Practical-Exam/blob/62cdec419d676ac7ebe4ba0650c76f2b9befa1ad/house_sales.csv)
Dataset Tasks: 

**Project Instructions:**
- The object you have been asked to create will be graded, not the code.
- Ensure you match any column name or object requirements.
- The fit of your models will be compared to held back values from the test set provided to you. We will calculate the Root Mean Squared Error of your predictions.
- At least one of your two models must have a Root Mean Squared Error below 30,000 to pass
- All required data has been created and has the required columns

Submission/Grading Objective:

**All required data has been created and has the required columns**
   - My assessment: All of the columns should match of what DataCamp have asked to follow

**Task 1: Identify and replace missing values.**
   - My assessment: Show how you identify standard or non-standard missing values (there are other unexpected format) in a specific column and replace them based on what value DataCamp have asked

**Task 2: Identify and replace missing values.**
   - My assessment: Show how you identify standard or non-standard missing values (there are other unexpected format) in a specific column and replace them based on what value DataCamp have asked

Task 2: Clean categorical and text data by manipulating strings.

Do you know what categories are meant to be possible in each column in your data? Are they the only categories that are actually there? If you have extra categories because of spelling mistakes or differences in capitalisation, your analysis may end up being wrong.

Task 2: Convert values between data types.

Task 3: Aggregate numeric, categorical variables and dates by groups.

Task 4 & 5: Implement standard modeling approaches for supervised learning problems.

## Project Context
I successfully completed and passed this assessment on attempt 2/2. The assessment consisted of five main tasks:

### Assessment Overview
1. **Data Validation & Missing Values**
   - Challenge encountered: Identifying non-standard missing value formats
       - I found that some missing values containing or appearing as dashes (-) and some other unexpected format which I think is a good way to represent a real-world data scenario
       - This makes us do some holistic data quality inspection before and after cleaning including checking Missing Value Patterns, unique values analysis, Capitalization and Spelling Analysis

2. **String Manipulation & Categorical Data**
   - Key Learning: The importance of standardization in categorical variables
       - Discovered issues with inconsistent capitalization and spelling variations
       - Learned to always check unique values in categorical columns before proceeding with analysis
       - Real-world data rarely comes clean - careful string manipulation is crucial

3. **Data Type Conversions & Aggregations**
   - Critical Insights:
       - Proper data type conversion is fundamental for accurate analysis
       - Learned to carefully handle date formats and numeric conversions
       - Understanding grouping operations helped in creating meaningful summaries

4. **Base Model Implementation (Linear Regression)**
   - Important Realizations:
       - First attempt failed because I didn't display the final DataFrame
       - Learned the importance of following output format requirements exactly
       - Understanding preprocessing steps (especially OneHotEncoder for categorical variables)
       - Gained insights on pipeline creation for reproducible modeling

5. **Advanced Model Comparison (Random Forest)**
   - Key Success Factors:
       - Built upon learnings from the base model implementation
       - Proper handling of categorical variables through preprocessing pipeline
       - Importance of displaying final predictions in required format
       - Understanding model comparison methodology

## Critical Learnings from Failed First Attempt
1. **Attention to Detail**
    - Output format matters as much as model accuracy
    - Always verify column names and DataFrame structure
    - Double-check all requirements before submission

2. **Data Preprocessing Importance**
    - Real-world data requires thorough cleaning
    - Never assume data is in standard format
    - Document cleaning steps for reproducibility

3. **Model Implementation**
    - Start simple with base model
    - Build complexity gradually
    - Verify predictions format matches requirements

## Personal Growth Areas
1. **Technical Skills Enhanced**
    - Improved data cleaning methodology
    - Better understanding of sklearn Pipeline
    - Learned to handle various data formats effectively

2. **Problem-Solving Approach**
    - Developed more systematic data validation process
    - Improved attention to requirement details
    - Better understanding of model comparison

## Future Learning Goals
1. **Expand Knowledge**
    - Explore more advanced preprocessing techniques
    - Learn additional modeling approaches
    - Deepen understanding of feature engineering

2. **Best Practices**
    - Develop better documentation habits
    - Create more robust validation checks
    - Build more efficient data processing pipelines

## Tools and Technologies Used
- Python
- pandas for data manipulation
- scikit-learn for modeling
- Pipeline for streamlined processing
- Various preprocessing techniques

*Note: This reflection documents my personal learning journey through this assessment, highlighting both challenges and growth opportunities.*
