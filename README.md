# 🏀 NCAA Tournament Predictor — Course Project (Systems Analysis & Design)

## 📌 Overview
The selected competition, March Machine Learning Mania 2025, focuses on predicting the outcomes of the NCAA men’s and women’s basketball tournaments using historical data. Participants submit predicted win probabilities, which are evaluated using the Brier score. Each person can submit up to two entries.
To learn more about this competition -> Kaggle - March Machine Learning Mania 2025

This project integrates concepts from three workshops:

- Workshop 1: Kaggle competition analysis (March Machine Learning Mania 2025)
- Workshop 2: System design and architecture of a predictive model
- Workshop 3: Simulation and sensitivity testing under uncertainty

In the final phase, we integrated a Large Language Model (LLM) to enhance or complement the pipeline and compared it to our classical approach.

---

## 🔧 Project Structure

    BASKETBALL-TOURNAMENT-PROJECT/
    ├── Simulations/
    │ ├── Data/ <- Raw and processed input datasets
    │ ├── Features/ <- Features dataset
    │ ├── Predictions/ <- CSVs or notebooks with model predictions
    │ ├── TournamentPrediction.ipynb <- Main simulation notebook
    │── llm-predictor.ipynb <- LLM integration notebook
    │── requirements.txt <- Python dependencies
    │── README.md <- Project overview and instructions
    │── final_paper.pdf <- Full written report
    │── Basketball_tournament_poster.pdf
    │── Basketball_tournament_slides3.pdf
    │── Technical_Report_Tournament.pdf

---
## 🚀 How to Run

1. Clone the repository and navigate into the project directory.

2. Create and activate a virtual environment:

    ```bash
    python -m venv .venv
    source .venv/bin/activate  # Linux/macOS
    .venv\Scripts\activate     # Windows

3.  Install dependences 
    ```bash
    pip install -r requirements.txt

----
## 🧠 Features Used

| Feature                | Description / Calculation                                      |
|------------------------|----------------------------------------------------------------|
| Seed difference        | Difference between tournament seeds (`SeedB - SeedA`)         |
| Win-Loss Ratio         | Total number of wins divided by total number of games played  |
| Average points scored  | Average number of points scored per game                      |
| Average points allowed | Average number of points conceded per game                    |
| Offensive efficiency   | Points scored divided by estimated possessions                |
| Defensive efficiency   | Points allowed divided by estimated possessions               |
| Scoring margin         | Average point differential per game (`scored - conceded`)     |


# 🤖 LLM Integration
    The LLM was integrated to assist with feature generation, enriching the dataset by automatically constructing statistical descriptors from textual or tabular context. These features were then used in training a secondary model.

    Comparative evaluation included:

    Classical model (logistic regression using SeedDiff only)

    Extended model (with engineered features)

    LLM-assisted model (either as feature generator or predictor)

