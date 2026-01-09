# Top-4-Soccer-League-Winners
This project uses machine learning to predict the winners of the 2025–2026 seasons for LaLiga, the Premier League, Serie A, and the Bundesliga, along with each champion’s projected points total and win probability.

An exploratory data analysis was first conducted to examine team performance trends, feature distributions, and key factors influencing league success. Based on these insights, a Random Forest model was trained to capture non-linear relationships between features and generate predictions.

## Data
- Utilized data from fbref.com
- Gathered data from the past 10 seasons for each of the four leagues into csv files

## Exploratory Data Analysis
- Evaluated team participation consistency across seasons
- Analyzed top-four finish frequency to identify dominant teams
- Isolated historical league winners to study championship profiles
- Computed average points per match for champions as a benchmark 

## Machine Learning
### Problem Formulation
The task was framed as a binary classification problem, where the objective is to predict whether a team will win the league (1) or not (0) based on season performance metrics.

### Feature Engineering
- Additional features were created to better represent season progression and future performance:
- Games Left
- Projected Points: Estimated final points total based on current points per match
- Points per Match
- Goal Difference
- Wins and Losses
These features capture both current performance and expected season trajectory, which are crucial for predicting the title winner.

### Training and Test Split
- Training Data: All completed seasons prior to the ongoing 2025-2026 Season
- Test Data: Ongoing 2025–2026 Season

### Model Selection
- Ran this by utilizing the Random Forest Classifier
- The model was trained with 200 decision trees and a fixed random state for reproducibility.

### Model Evaluation
- Model performance on training data was assessed using multiple metrics:
-- Accuracy
-- ROC-AUC Score
-- Log Loss
-- Confusion Matrix

### Prediction Outputs
For the 2025–2026 season, the model generated:
- Predicted league winner
- Projected final points
- Win probability for each team

### Visualization
A bar chart was produced to visualize championship win probabilities by team, allowing for easy comparison of title contenders and clearer interpretation of model confidence.

## Results of the Model
- LaLiga: Barcelona
- Premier League: Arsenal
- Bundesliga: Bayern Munich
- Serie A: Inter Milan
