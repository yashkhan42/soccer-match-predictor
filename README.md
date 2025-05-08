# EPL Match Outcome Predictor

Predicting the winner of English Premier League (EPL) matches using historical performance data and machine learning.

## Project Overview

This project explores the relationship between match statistics (such as possession, shooting metrics, and opponent strength) and the final result of Premier League games. By scraping and analyzing historical data, we build a classification model to predict whether a specific team will win their next fixture.

## Key Features

* **Automated Web Scraping**: Data collection from [FBref](https://fbref.com/en/comps/9/Premier-League-Stats) using `BeautifulSoup` and `requests`.
* **Data Processing**: Cleaning match logs across multiple seasons and merging shooting statistics with general match data using `pandas`.
* **Feature Engineering**: Implementing rolling averages to capture a team's recent form (e.g., goals scored, shots on target, and goals against).
* **Machine Learning**: Training a `RandomForestClassifier` to predict match outcomes based on time, venue, and historical performance.
* **Evaluation**: Measuring accuracy and precision scores to refine the model's reliability for football betting or performance analysis.

---

## File Structure

| File | Description |
| :--- | :--- |
| `scraping.ipynb` | The primary notebook for gathering data. It navigates through league standings and team pages to compile match logs. |
| `prediction.ipynb` | The core machine learning notebook where data is preprocessed, models are trained, and predictions are evaluated. |
| `matches.csv` | The dataset generated from the scraping process, containing detailed match records and shooting stats. |

---

## Local Setup

### Prerequisites
* Python 3.8+
* Jupyter Notebook or JupyterLab

### Installation
Clone the repository and install the required Python packages:

```bash
pip install pandas requests beautifulsoup4 scikit-learn