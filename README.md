# ⚽ Serie A Match Predictor & Season Simulator

![alt text](https://img.shields.io/badge/Python-3.8%2B-blue)

![alt text](https://img.shields.io/badge/Pandas-Scikit--Learn-orange)

![alt text](https://img.shields.io/badge/Status-Completed-green)

## 📌 Overview

This project is a **Data Science & Machine Learning** application designed to predict the outcomes of **Italian Serie A matches**. 
Beyond simple match prediction, the system uses **Monte Carlo Simulations** to play out the remainder of the season thousands of times, providing statistical probabilities for the final league winner.  

It transforms raw match data into actionable insights using metrics like **Attack Strength**, **Defense Strength**, and **Current Form**.

---

## 🚀 Key Features

- **Automated Data Pipeline**  
  Fetches historical and current season data directly from reliable sources ([football-data.co.uk](https://www.football-data.co.uk/)).

- **Advanced Feature Engineering**  
  Calculates dynamic team stats:
  - Home/Away **Attack Strength** (Goals Scored per Game)  
  - Home/Away **Defense Strength** (Goals Conceded per Game)

- **Machine Learning Model**  
  Uses a **Random Forest Classifier** to predict match outcomes:  
  **Home Win**, **Draw**, **Away Win**.

- **Monte Carlo Simulation**  
  Simulates remaining unplayed fixtures **1,000 times** to determine the probability of each team winning the **Scudetto**.

- **Market Analysis**  
  - **Single Match Oracle**: Predicts outcomes for specific matchups (e.g., Inter vs Juventus)  
  - **Goal Expectancy**: Identifies matches likely to have Over/Under 2.5 Goals

- **Visualizations**  
  - Title Probability Bar Chart  
  - Team Strength Scatter Plot (Attack vs Defense)  
  - Model Confusion Matrix (Accuracy Analysis)  
  - Current Form Analysis (Last 5 Games)

---

## 🛠️ Tech Stack

- **Language:** Python  
- **Data Manipulation:** Pandas, NumPy  
- **Machine Learning:** Scikit-Learn (`RandomForestClassifier`)  
- **Visualization:** Matplotlib  
- **Data Fetching:** Requests

---

📂 **Project Structure**
```
serie-a-predictor/
├── SerieA_Predictor.ipynb   # Main Jupyter Notebook containing all logic
├── README.md                # Project documentation
└── requirements.txt         # List of dependencies
```
---

## 📊 Methodology

### 1. Data Collection & Cleaning
- Pulls CSV data containing results, dates, and scores  
- Filters relevant columns and cleans missing values to ensure high-quality input

### 2. Attack & Defense Ratings
- Converts teams into numeric vectors:  
  `[Home_Attack, Home_Defense, Away_Attack, Away_Defense]`  
- This allows the model to understand that a team strong at home might be weaker away

### 3. Simulation (Monte Carlo Method)
- Football is unpredictable; a single prediction isn’t enough  
- Process:
  1. Identify all unplayed matches  
  2. Predict probabilities for each match (e.g., Inter 60%, Draw 25%, Milan 15%)  
  3. Simulate the season **1,000 times**  
  4. Aggregate results to show league winner probabilities

### 4. Visuals & Insights
- **Title Probability:** Percentage breakdown of who is most likely to win  
- **Strength Map:** Scatter plot identifying "Dominant Teams" vs "Struggling Teams"  
- **Confusion Matrix:** Shows where the model tends to make errors (usually Draws)

---

## 💻 How to Run

1. **Clone the repository:**
git clone https://github.com/BesmirQerosi/serie-a-predictor.git
cd serie-a-predictor

2. **Install dependencies:**

pip install pandas numpy scikit-learn matplotlib requests jupyter

3. **Run the Notebook:**

jupyter notebook SerieA_Predictor.ipynb

4. **Execute cells sequentially to fetch latest data and run simulations**



🔮 **Future Improvements**
  - ⚽ **Integration of xG (Expected Goals):** Scrape advanced metrics for better accuracy
  - 🩹 **Player Availability:** Adjust team strength based on injuries/suspensions
  - 🤖 **Deep Learning:** Experiment with Neural Networks (TensorFlow/PyTorch) for pattern recognition
  - 🌐 **Web App:** Deploy the model using Streamlit for an interactive interface

⚠️ **Disclaimer**
This project is for educational and portfolio purposes only. Football is unpredictable, and this model should not be used as financial advice for betting.

Author: [Besmir Qerosi]
Connect: [(https://www.linkedin.com/in/besmir-qerosi-4511a1353/)]