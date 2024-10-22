# Directional Forecasting in Cryptocurrencies 🪙📈
**Predict whether crypto prices will surge or decline**

## Overview
This repository documents my approach to the Kaggle competition "[Directional Forecasting in Cryptocurrencies](https://www.kaggle.com/competitions/directional-forecasting-in-cryptocurrencies/overview)." The goal of the competition is to predict the direction of price movement of a cryptocurrency (up or not up) for the next minute, based on historical price data. 

This challenge combines the dynamic and volatile world of cryptocurrencies with cutting-edge machine learning techniques, and it encourages participants to build robust models capable of handling high-frequency trading scenarios. 

### Prizes
The best-performing submissions may be considered for a highly selective program with a career track in quantitative finance or data science.

## Objective 🎯
The primary task is to develop a machine learning model that can:
- **Predict** the direction of the next-minute price change for a cryptocurrency.
- **Binary classification**: 1 (up) or 0 (not up).

## Evaluation 🏆
Submissions are evaluated using the **Macro-Averaged F1 Score**. This ensures balanced performance across both classes (up vs. not up) by considering the trade-off between **precision** and **recall**. The evaluation metric is calculated as:

![image](https://github.com/user-attachments/assets/bd5cf7f8-6ea9-4978-a6d7-425ccc9d91c5)


Where:
- **Precision** is the ratio of correctly predicted positive observations to total predicted positives.
- **Recall** is the ratio of correctly predicted positives to all actual positives.

The **Macro-Averaged F1 Score** is used to evaluate overall model performance across the two classes (up or not up).

## [Dataset](https://github.com/Caio-Felice-Cunha/Directional-Forecasting-in-Cryptocurrencies/tree/main/datasets) 📊
Participants are provided with a dataset containing minute-by-minute **OHLCV** (Open, High, Low, Close, Volume) data for a specific cryptocurrency.

### Features:
- **timestamp**: The timestamp for the minute covered by the row.
- **open**: Price at the start of the minute (USDT).
- **high**: Highest price during the minute (USDT).
- **low**: Lowest price during the minute (USDT).
- **close**: Price at the end of the minute (USDT).
- **volume**: Number of crypto asset units traded during the minute.
- **quote_asset_volume**: Total value of trades (USDT) during the minute.
- **number_of_trades**: Number of trades in the minute.
- **taker_buy_base_volume**: Amount of crypto bought by takers during the minute.
- **taker_buy_quote_volume**: Value in USDT spent by takers to buy the asset during the minute.
- **target**: Binary label (1 if price went up in the next minute, 0 otherwise).

### Files:
- `train.csv`: Training data with historical prices and target labels.
- `test.csv`: Test data used for leaderboard scoring.
- `sample_submission.csv`: Template for the submission format.

## Solution Approach 💡
1. **Data Preprocessing**:
    - Handling missing values, feature scaling, and outliers.
    - Feature engineering to extract additional useful signals.
   
2. **Exploratory Data Analysis (EDA)**:
    - Understanding price trends, volatility, and trade volume behavior.
    - Checking target class distribution.

3. **Modeling**:
    - Trying multiple algorithms (e.g., Random Forest, XGBoost, LSTM for time-series modeling).
    - Tuning hyperparameters using cross-validation.

4. **Evaluation & Tuning**:
    - Calculating the F1 score for both training and test sets.
    - Fine-tuning models to improve overall performance, with a focus on macro-averaged F1 Score.

5. **Submission**:
    - Generating predictions and submitting via Kaggle.

## Results & Insights 📈
- The final evaluation will be based on the F1 score.
- Model performance and analysis will be shared as the project progresses.

## Repository Structure 📂
```
├── data/                    # Dataset folder
├── scripts-notebooks/       # Jupyter notebooks for EDA and experiments and Python scripts for preprocessing and training
├── models/                  # Saved models
├── submissions/             # Submission CSV files
├── requirements.txt         # Dependencies
└── README.md                # Project documentation
```

## Contributions
Feel free to fork the repository, make your own contributions, and open a pull request. Any feedback is welcome!

## License
This project is licensed under the MIT License - see the [LICENSE](https://github.com/Caio-Felice-Cunha/Directional-Forecasting-in-Cryptocurrencies/blob/main/LICENSE) file for details.
