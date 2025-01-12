# DSA Practical Exam
Note: I didn't upload the notebook file here but here's the overview of how I approach the test

**Project Instructions:**
- Use Python to perform each of the tasks (5 Tasks).
- The object you have been asked to create will be graded, not the code.
- Ensure you match any column name or object requirements.
- Only 2 opportunities to submit the exam for grading
- You must be successful in all tasks to pass this exam
- The fit of your models will be compared to held back values from the test set provided to you. We will calculate the Root Mean Squared Error of your predictions.
- At least one of your two models must have a Root Mean Squared Error below 30,000 to pass  

### Initial Data Assessment

### Task 1 & 2:  Identify and replace missing values/Clean categorical and text data by manipulating strings/Convert values between data types.
**My Assessment & Strategy**:
1. **Holistic Inspection Approach**
    - Conducting a comprehensive dataframe inspection to have an overview of the data variables
   - Performed a for loop column-by-column quality analysis (I include unique values, potential missing value patterns, capitalization and spelling Analysis for object types, statistics for numeric columns)

   **Data Issues Identified:**
   - `city` column contained placeholder values (`'--'`) indicating missing data.
   - `house_type` column had inconsistent abbreviations for house types (e.g. semi:semi-detached, det:detached)
   - `area` column stored numerical values as strings with units (`'sq.m.'`), making them unsuitable for analysis.
   - `months_listed` column had (`'nan'`) missing values pattern.
   - `sale_date` column needed to ensure proper datetime formatting.
  
   - After cleaning (via data imputation, string replacement and mapping and type conversion), I performed after inspection analysis to verify clean data
     
### Task 3: Aggregate numeric, categorical variables and dates by groups
Task Narrative: "The team at RealAgents have told you that they have always believed that the number of bedrooms is the biggest driver of house price.
Producing a table showing the difference in the average sale price by number of bedrooms along with the variance to investigate this question for the team."

**My Approach**:
  - Store in dataframe called `price_by_rooms`, groupby("bedrooms"), agg. the "sales price" by mean and variance and round the results by 1
   - Visualize the relationaship of bedroom (x) and average sales price/variance (y) with bar chart + trend  line (not part of the grading)
     
This task was just to investigate the relationship between the number of bedrooms and house prices, focusing on two key metrics:
1. **Average Sale Price:** Helps determine the typical price of houses based on the number of bedrooms. 
2. **Variance in Sale Price:** Indicates the spread or variability of house prices within each bedroom category.

### Task 4: Implement standard modeling approaches for supervised learning problems

We are asked to use new dataset, train.csv (not the house_sales.csv that we prep) and use validation.csv to predict new values. Show df results for x 'house_id', y 'price'
Also, this is just focus on getting a baseline model working

**Task 4 approach**:

**0. Define the Problem**
   - Target Variable (Y) is sales_price (continuous variable, making linear regression appropriate).
   - Features (X): All columns except house_id, sale_price, and sale_date (Need categorical encoding for object features)
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
**4. Identify categorical column apply OneHotEncoder via preprocessing pipeline**

**5. Create and train model pipeline**
- Fitted the Pipeline (preprocessing + regression) to X_train and y_train

**6. Fit the model**
```
model.fit(X_train, y_train)
```
**7. Prepare validation data**
```
X_validation = validation_data.drop(columns=['house_id', 'sale_date'])
```
**8. Make sample predictions and create result dataframe**
```
validation_data['price'] = model.predict(X_validation)
base_result = validation_data[['house_id', 'price']]
```
```
Model Training Summary:
Training data shape: (1200, 8)
Validation data shape: (300, 8)

Features used:
Categorical: ['city', 'house_type']
Numeric: ['months_listed', 'bedrooms', 'area']

First few predictions:
   house_id          price
0   1331375  121527.827316
1   1630115  304386.625267
2   1645745  384760.100656
3   1336775  123976.268985
4   1888274  271186.199353
```
**9. Comparison to the test set provided**

### Task 5: Implement standard modeling approaches for supervised learning problems
Same data with Task 4 but we're going to fit a comparison using different model, which is capable of capturing non-linear relationships and interactions, check if it result in better performance
```
Random Forest Model Summary:
Training data shape: (1200, 8)
Validation data shape: (300, 8)

First few predictions:
   house_id      price
0   1331375   82582.62
1   1630115  303256.87
2   1645745  404809.08
3   1336775  106624.68
4   1888274  267768.22
```
