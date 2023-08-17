## Predicting Road Crash Severity - Data Science Project
Welcome to the Predicting Road Crash Severity data science project repository! This project aims to develop a machine learning predictive model to classify road crash severity in the state of Victoria, Australia. By leveraging advanced statistical techniques, machine learning algorithms, and comprehensive data analysis, I seek to gain valuable insights into the factors that contribute to road accidents and their severity, ultimately aiding in the enhancement of road safety measures.

### Overview
Road accidents pose a significant societal issue with global implications. In Victoria, Australia, an average of 240 people lose their lives annually in such incidents (Transport Accident Commission, 2021). Analyzing accident severity and identifying contributing factors has become increasingly critical. To address this challenge, I have gathered a comprehensive dataset of 60,680 instances and 49 variables, including police report observations for a 5 year period (2015 - 2019) compiled by VicRoads and available from [Department of Transport](data.vic.gov.au), as well as historical localised meteorological observations using [Visual Crossing Weather API](https://www.visualcrossing.com/weather-api).

### Table of Contents
1. [Data gathering and cleaning - initial inspection and processing](https://github.com/MarkStephens060482/Big-Data-projects/blob/main/Road%20Accident%20Severity%20-%20Data%20Cleaning.ipynb)
2. [Exploratory Data Analysis - Part 1](https://github.com/MarkStephens060482/Big-Data-projects/blob/main/Road_Accident_Severity_EDA_part_1.ipynb)
3. [Exploratory Data Analysis - Part 2](https://github.com/MarkStephens060482/Big-Data-projects/blob/main/Car_Accident_Severity_EDA_part_2.ipynb)
4. [Data Modelling and Evaluation](https://github.com/MarkStephens060482/Big-Data-projects/blob/main/Severity_of_Road_Accidents_modelling%20and%20evaluation.ipynb)

### Data Cleaning
I began by cleaning the road crash data, inspecting variable, checking type and unique values. I developed a concurrent Weather API call function to gather historical meteorological observations based on longitude and latitude and time and date of all road crash incidences. Also, historical Public holiday and Long Weekend dates were collated using a [date nager API](https://date.nager.at/api/v3/LongWeekend). Imputation strategies were employed to address missing values before remaining null values were removed. 
### Data Exploration
I performed an exploratory data analysis (EDA) to understand the distribution and relationships within the dataset. The dataset comprises of two main groups of variables: pre-accident variables, which are known prior to the accident, and post-accident variables, which can only be determined once the accident has occurred. The EDA will delve into feature distributions, correlations, and class proportions, enabling us to gain essential insights before developing the predictive model. Further cleaning and processing of high cardinality categorical variables was performed. Base models were fitted on preprocessed data to examine feature importances and set a performance baseline. Feature Selection was performed using Boruta Algorithm to identify a subset of key features. Clustering was performed using HDBSCAN with Gower distance and a 2D projection of the data was visualised with t-SNE. 

### Machine Learning Model
Building upon the insights from our EDA, we will develop a multivariate time series imbalanced classification model. The multiclass classification task involves four classes of severity levels, each with varying proportions. We will explore various machine learning algorithms, perform feature engineering, and experiment with different strategies to handle the class imbalance.

### Evaluation and Results
Our model will be evaluated using appropriate metrics for imbalanced datasets, such as precision-recall curves and F1-score. We will conduct cross-validation to assess the model's performance and fine-tune hyperparameters to achieve optimal results. The project aims to produce a robust predictive model that accurately classifies road crash severity in real-world scenarios.

### Repository Structure
data: Contains the dataset used for analysis (for confidentiality reasons, the actual data is not provided).
notebooks: Jupyter notebooks with data exploration, model development, and evaluation.
images: Charts and visualizations generated during EDA and model evaluation.
models: Saved trained models and model performance results.
documentation: Additional resources and documentation related to the project.
How to Contribute
We welcome contributions to this project! If you find any issues or have ideas for improvements, please feel free to open an issue or submit a pull request. Let's collaborate to make our roads safer through data-driven insights!

Acknowledgments
We extend our gratitude to [Data Vic](https://www.data.vic.gov.au/) for providing the road crash dataset for this project.

Let's embark on this exciting data science journey together and make a positive impact on road safety in Victoria, Australia! Happy coding! 🚗🛣️
