⚽ Serie A Match Predictor & Season Simulator

![alt text](https://img.shields.io/badge/Python-3.8%2B-blue)

![alt text](https://img.shields.io/badge/Pandas-Scikit--Learn-orange)

![alt text](https://img.shields.io/badge/Status-Completed-green)

📌 Overview
This project is a Data Science and Machine Learning application designed to predict the outcomes of Italian Serie A matches.
Beyond simple match prediction, the system utilizes Monte Carlo Simulations to play out the remainder of the season thousands of times, providing a statistical probability for the final league winner. It transforms raw match data into actionable insights using metrics like Attack Strength, Defense Strength, and Current Form.

🚀 Key Features
Automated Data Pipeline: Fetches historical and current season data directly from reliable online sources (football-data.co.uk).
Advanced Feature Engineering: Calculates dynamic team stats:
Home/Away Attack Strength (Goals Scored per game).
Home/Away Defense Strength (Goals Conceded per game).
Machine Learning Model: Uses a Random Forest Classifier to predict match outcomes (Home Win, Draw, Away Win).
Monte Carlo Simulation: Simulates the remaining unplayed fixtures 1,000 times to determine the probability of each team winning the "Scudetto".
Market Analysis:
Single Match Oracle: Predicts specific matchups (e.g., Inter vs Juventus).
Goal Expectancy: Identifies matches likely to have Over/Under 2.5 Goals.
Visualizations:
Title Probability Bar Chart.
Team Strength Scatter Plot (Attack vs Defense).
Model Confusion Matrix (Accuracy Analysis).
Current Form Analysis (Last 5 Games).

🛠️ Tech Stack
Language: Python
Data Manipulation: Pandas, NumPy
Machine Learning: Scikit-Learn (RandomForestClassifier)
Visualization: Matplotlib
Data Fetching: Requests

📂 Project Structure
code
Code
├── SerieA_Predictor.ipynb   # The main Jupyter Notebook containing all logic
├── README.md                # Project documentation
├── requirements.txt         # List of dependencies

📊 Methodology
1. Data Collection & Cleaning
The system pulls CSV data containing results, dates, and scores. It filters relevant columns and cleans missing values to ensure the model receives high-quality input.
2. The Logic: Attack & Defense Ratings
Instead of using team names (which ML models don't understand), every team is converted into a vector of four numbers:
[Home_Attack, Home_Defense, Away_Attack, Away_Defense]
This allows the model to understand that a team strong at home might be weak away.
3. Simulation (The "Monte Carlo" Method)
Since football involves luck, a single prediction isn't enough. The system:
Identifies all unplayed matches.
Predicts probabilities for each match (e.g., Inter 60%, Draw 25%, Milan 15%).
Simulates the season 1,000 times based on these probabilities.
Aggregates the results to show who wins the league most often.

📈 Visuals & Insights
The notebook generates several key insights. Here is a breakdown of what to expect:
Title Probability: A percentage breakdown of who will likely win the league.
Strength Map: A scatter plot identifying "Dominant Teams" (High Attack, Strong Defense) vs "Struggling Teams".
Confusion Matrix: A transparency tool showing where the model tends to make errors (usually on Draws, which are historically hard to predict).

💻 How to Run
Clone the repository:
code
Bash
git clone https://github.com/BesmirQerosi/serie-a-predictor.git
cd serie-a-predictor
Install dependencies:
code
Bash
pip install pandas numpy scikit-learn matplotlib requests jupyter
Run the Notebook:
code
Bash
jupyter notebook SerieA_Predictor.ipynb
Execute the cells sequentially to fetch the latest data and run the simulation.

🔮 Future Improvements
Integration of xG (Expected Goals): Scrape advanced metrics for better accuracy.
Player Availability: Adjust team strength based on injuries/suspensions of key players.
Deep Learning: Experiment with Neural Networks (TensorFlow/PyTorch) for pattern recognition.
Web App: Deploy the model using Streamlit for an interactive user interface.

⚠️ Disclaimer
This project is for educational and portfolio purposes only. Football is unpredictable, and this model should not be used as financial advice for betting.

Author: [Besmir Qerosi]
Connect: [(https://www.linkedin.com/in/besmir-qerosi-4511a1353/)]