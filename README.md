## The Next Best Movie 

## Project Overview
This project uses machine learning models to explore and predict insights from the top films of the last 20 years. Using the TMDb dataset, we analyse key factors that influence the success of films, focusing on revenue prediction and genre classification.

## Datasets
We analyzed the [TMDb Movies Dataset](https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies), a comprehensive resource with over 1 million movies, updated daily. It includes information such as titles, ratings, release dates, revenue, genres, and more.

## Project Structure
- **Data**: Contains raw and cleaned datasets in CSV format.  
- **Notebooks**: Jupyter notebooks with data cleaning, preprocessing, model training and analysis code.  
- **Slides**: Presentation slides. 

## Analysis Approach

### 1. Data Cleaning
Data cleaning was critical due to the large dataset size (1 million+ records):

- **Dropped irrelevant columns** to streamline the dataset.  
- **Filtered data**: Retained only movies released in the last 20 years, focusing on "Released" status.  
- **Outlier handling**: Removed entries with unusual values for runtime, budget, and revenue.  
- **Sorted by revenue** to prioritize high-performing movies.

### 2. Feature Engineering and Selection 
Feature engineering was essential to improve model inputs. We used techniques such as:

- **Scaling**: Applied MinMaxScaler to normalize numeric variables.
- **Date Features**: Split the release_date into release_month and release_day.
- **Genres**: Normalized and tokenized genres for multi-label classification.
- **Text Features**: Extracted key trends from movie titles for feature representation.

### 3. Model Building and Evaluation

**Revenue Prediction Model: RandomForestRegressor**
- Input Features: budget, runtime, release_year
- Evaluation Metric: Mean Absolute Error (MAE)
- Performance: Achieved MAE of $X.
- Genre Classification:
  
**Revenue Prediction Model: RandomForestClassifier**
- Input Features: budget, runtime, release_year
- Evaluation Metric: Accuracy
- Performance: Achieved accuracy of X%.

**Validation Techniques**
- Train-Test Split: 80/20 split for training and testing.
- Cross-Validation: Employed k-fold cross-validation to ensure robust performance.

### 4. Hyperparameter Tuning and Model Optimization
We optimized models using the following techniques:

- **Random Search & Grid Search**: Tuned hyperparameters like the number of estimators and tree depth.
- **Feature Pruning**: Reduced features to minimize noise and enhance interpretability.

## Key Findings & Implications
- **Revenue Drivers**: High budgets and longer runtimes correlate with higher revenue but show diminishing returns beyond a threshold.
- **Genre Trends**: Action, adventure, and family genres dominate top revenue earners.
- **Title Impact**: Short, impactful titles with emotional or intriguing keywords perform better.
