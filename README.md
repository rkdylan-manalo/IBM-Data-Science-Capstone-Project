# IBM Data Science Professional Certificate - Capstone Project
## Project Overview
SpaceX advertises Falcon 9 rocket launches at a cost of $74 million, with much of this cost savings attributed to SpaceX's ability to reuse the first stage of the rocket.

The objective of this project is to predict whether the Falcon 9 first stage will land successfully. By accurately predicting landing outcomes, we can estimate the true cost of a launch, providing valuable intelligence for alternative companies bidding against SpaceX.

## Business Problem
If we can determine if the first stage will land, we can determine the cost of a launch. This information can be used to provide reliable cost estimates for potential clients, improving financial planning and bid pricing.

## Tech Stack & Tools
* Languages: Python, SQL

* Data Collection: SpaceX REST API, Web Scraping (BeautifulSoup)

* Data Wrangling & EDA: Pandas, NumPy, SQL Magic Commands

* Data Visualisation: Matplotlib, Seaborn, Folium (Interactive Maps), Plotly Dash (Interactive Dashboard)

* Machine Learning: Scikit-Learn (Logistic Regression, SVM, Decision Trees, KNN, GridSearchCV)

## Methodology & Workflow
1. Data Collection & Wrangling

* Collected historical launch data using the SpaceX API and scraped Wikipedia tables via BeautifulSoup.

* Handled missing values (imputed Payload Mass with the mean, kept LaunchPad nulls representing unused pads).

* Mapped 8 different mission outcomes into a binary classification (Class: 0 = Failure, 1 = Success).

* SQL Analysis: Used SQL magic commands to isolate target variables and identify data imbalances (e.g., 98 successes vs. 1 failure). Recognising this early indicated the need for a Confusion Matrix during ML evaluation, rather than relying solely on accuracy.

2. Exploratory Data Analysis (EDA) & Visual Analytics

* Data Visualisation: Identified patterns across launch sites, payload mass, orbit types, and flight numbers. Success rates have significantly increased over time, particularly after 2013.

* Geospatial Analysis (Folium): Created interactive maps to analyse launch site proximities. Discovered that optimal launch sites are strategically located near the coast (for safety) and the equator (for orbital mechanics).

* Interactive Dashboard (Plotly Dash): Built a real-time dashboard with dropdowns and range sliders, allowing users to filter data by launch site, payload mass, and booster version.

3. Predictive Analysis (Machine Learning)

* Standardised the data using StandardScaler and split it into training and testing sets.

* Trained and tuned four classification models using GridSearchCV (10-fold cross-validation).

* Evaluated models using Accuracy Scores and Confusion Matrices.

## Key Results & Findings
1. Best Performing Model: The Decision Tree Classifier was selected as the optimal model. While all four models achieved a competitive 83.33% Test Accuracy, the Decision Tree outperformed the others in Cross-Validation Training Accuracy (86.07%).

2. Launch Site Success: KSC LC-39A demonstrated the highest success rate among all launch sites.

3. Key Predictors: Flight Number (experience over time), Launch Site, and Payload Mass were identified as the strongest features for predicting a successful landing.

4. Model Evaluation: The confusion matrix revealed 3 False Positives and 0 False Negatives for the best model, indicating the model is highly reliable at predicting successful landings.

## Repository Structure
```
data/                 							Jupyter Notebooks
│   ├── 01_jupyter-labs-spacex-data-collection-api.ipynb
│   ├── 02_jupyter-labs-webscraping.ipynb
│   ├── 03_labs-jupyter-spacex-Data wrangling.ipynb
│   ├── 04_jupyter-labs-eda-sql-coursera_sqllite.ipynb
│   ├── 05_edadataviz.ipynb
│   ├── 06_lab_jupyter_launch_site_location.ipynb
│   └── 07_spacex-dash-app.py
│   └── 08_SpaceX_Machine Learning Prediction_Part_5.ipynb
├── presentation           						Final PDF presentation slides
└── README.md
```

## How to Run
Clone the repository:
git clone https://github.com/yourusername/spacex-falcon9-prediction.git

Install the required libraries:
pip install -r requirements.txt

Run the Jupyter Notebooks sequentially in the notebooks/ folder.

To launch the dashboard, run: python 06_plotly_dash.py
