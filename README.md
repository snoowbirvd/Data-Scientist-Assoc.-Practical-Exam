# DSA Practical Exam

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
   - Task 3 is exploring the relationship between a specific house features and sale price. "bedrooms" (x) is identified as biggest driver in this task
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
The team at RealAgents have told you that they have always believed that the number of bedrooms is the biggest driver of house price. 
Producing a table showing the difference in the average sale price by number of bedrooms along with the variance to investigate this question for the team.
  - This is the probably the easiest task in terms of coding solution

**My Approach**:
  - Store in dataframe called `price_by_rooms`, groupby("bedrooms"), agg. the "sales price" by mean and variance and round the results by 1
   - Visualize the relationaship of bedroom (x) and average sales price/variance (y) with bar chart + trend  line (not part of the grading)

     
In perspective, the goal of this task was to investigate the relationship between the number of bedrooms and house prices, focusing on two key metrics:
1. **Average Sale Price: Helps determine the typical price of houses based on the number of bedrooms. 
2. **Variance in Sale Price: Indicates the spread or variability of house prices within each bedroom category.

### Task 4 & 5: Implement standard modeling approaches for supervised learning problems

We are asked to use new dataset, train.csv (not the house_sales.csv that we prep) and use validation.csv to predict new values. Show df results for x 'house_id', y 'price'
Also, this is just focus on getting a baseline model working (no error metrics conducted

**Task 4 approach**:

**0. Define the Problem**
   - Target Variable (Y) is sales_price (continuous variable, making linear regression appropriate).
   - Features (X): All columns except house_id, sale_price, and sale_date
   - import sklearn
     
**1. Load the datasets**
```
train_data = pd.read_csv('train.csv')
validation_data = pd.read_csv('validation.csv')
```
**2. Prepare training data**
```
X_train = train_data.drop(columns=['house_id', 'sale_price', 'sale_date'])
y_train = train_data['sale_price']
```
**4. Create preprocessing pipeline**

**5. Create and train model pipeline**

**6. Fit the model**

**7. Prepare validation data**

**8. Make predictions**

**9. Create result dataframe**
