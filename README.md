# Applied Data Science Capstone
# SpaceX Falcon 9 First Stage Landing Prediction

## Description
In this case study, we forecast whether the Falcon 9 first stage will successfully land.  
SpaceX offers Falcon 9 rocket launches for **$62 million**, while other providers charge up to **$165 million**. Much of the cost savings comes from SpaceX's ability to **reuse the first stage**. By predicting first-stage landing success, companies can better estimate launch costs. This dataset and analysis are especially useful for startups competing with SpaceX for rocket launches.

This capstone project guides you through the **full data science methodology**, including data collection, wrangling, exploratory data analysis, visualization, predictive modeling, and reporting results.

---

## Methodology

1. **Data Collection**
   - **API:** Request and parse SpaceX launch data; filter for Falcon 9 launches.
   - **Web Scraping:** Extract Falcon 9 launch records from Wikipedia using BeautifulSoup; parse HTML tables into Pandas DataFrames.

2. **Data Wrangling**
   - Handle missing values.
   - Clean and map data into usable formats.
   - Feature engineering: create dummy variables, cast numeric columns to float64.

3. **Exploratory Data Analysis (EDA)**
   - SQL-based analysis for deeper insights.
   - Visualizations include:
     - Flight number vs. Launch site
     - Payload vs. Launch site
     - Success rate by orbit type
     - Flight number vs. Orbit type
     - Payload vs. Orbit type
     - Yearly success trends

4. **Launch Site Analysis with Folium**
   - Map launch sites and mark success/failure of each launch.
   - Analyze proximities to coastlines, cities, and infrastructure.

5. **Machine Learning Prediction**
   - Define class labels for landing success.
   - Standardize features, split data into training and test sets.
   - Train and evaluate models:
     - Logistic Regression
     - Support Vector Machine (SVM)
     - Decision Tree
     - K-Nearest Neighbors (KNN)
   - Hyperparameter tuning via GridSearchCV.
   - Evaluate model performance using **accuracy, precision, recall, and F1-score**.

---

## Step-by-Step Process

### 1. Collect Data
- **Task 1:** Request SpaceX launch data via API.
- **Task 2:** Filter dataset for Falcon 9 launches.
- **Task 3:** Handle missing values.

### 2. Web Scraping
- Extract Falcon 9 launch tables from Wikipedia.
- Parse column headers and create DataFrame.

### 3. Data Wrangling
- Analyze launches per site and per orbit type.
- Generate landing outcome labels.

### 4. EDA & Visualization
- Explore relationships between payload, orbit, flight number, and success.
- Yearly trends and success rates per site/orbit.

### 5. SQL Analysis
- Load dataset into Db2.
- Perform queries to:
  - Identify unique launch sites
  - Calculate payload statistics
  - Rank landing outcomes
  - Determine booster performance and first successful landings

### 6. Launch Site Location Analysis
- Map sites and successes/failures.
- Calculate distances and proximity factors affecting launch success.

### 7. Machine Learning Prediction
- Prepare features and labels.
- Standardize and split data.
- Train models and tune hyperparameters.
- Evaluate models and identify the best-performing algorithm (SVM in this case).

---

## Results
- **EDA Findings:**  
  - Successful landings increased significantly since 2015.  
  - Coastal sites facilitate water landings and logistics.  
  - Payload mass, orbit type, and flight number influence success rates.

- **Machine Learning Findings:**  
  - SVM achieved the **highest accuracy: 83.33%**.  
  - Predictive models help estimate landing success and, indirectly, launch costs.  
  - Main limitation: some **false positives** where unsuccessful landings were predicted as successful.

---

## Conclusion
- Launch success is influenced by **site, payload, orbit, booster version, and technological improvements**.  
- Historical trends and predictive models enable **data-driven decisions** for launch planning.  
- The analysis provides actionable insights for startups aiming to compete with Sp

