# stock-price-ml-pipeline
End-to-end ML pipeline for stock price direction prediction using Random Forest, yfinance, and scikit-learn

# Stock Price ML Pipeline

An automated end-to-end machine learning pipeline that fetches real-time 
stock data, engineers technical features, trains a classification model, 
and evaluates next-day price direction prediction.

---

## Tech Stack
- **Language:** Python 3.x
- **ML:** scikit-learn (Random Forest Classifier)
- **Data:** yfinance, Pandas, NumPy
- **Visualisation:** Matplotlib, Seaborn
- **Environment:** Jupyter Notebook, virtualenv

---

## Pipeline Overview
```
Data Ingestion → Feature Engineering → Model Training → Evaluation
     ↓                  ↓                    ↓              ↓
  yfinance API     Moving Averages      Random Forest    Accuracy Score
                   Daily Returns        Classifier       Classification
                   Volatility                            Report
```

---

## Project Structure
```
stock-price-ml-pipeline/
│
├── data/                    # Raw and processed CSV files
├── model/                   # Saved trained model (.pkl)
├── notebooks/               # Exploratory Data Analysis
│   └── eda.ipynb
│
├── data_fetcher.py          # Fetches historical data via yfinance
├── feature_engineering.py  # Generates ML features
├── train_model.py           # Trains and evaluates Random Forest model
├── main.py                  # Runs full pipeline end-to-end
├── requirements.txt
└── README.md
```

---

## Results

| Metric | Value |
|--------|-------|
| Ticker | AAPL |
| Training Period | 2022 – 2024 |
| Model | Random Forest Classifier |
| Test Accuracy | XX% |

> Note: This project is for educational and portfolio purposes.
> It is not intended as financial advice.

---

## How to Run

**1. Clone the repository**
```bash
git clone https://github.com/yourusername/stock-price-ml-pipeline.git
cd stock-price-ml-pipeline
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Run the pipeline**
```bash
python main.py
```

**4. Change the ticker (optional)**

In `main.py`, edit this line:
```python
run_pipeline("AAPL")  # Replace AAPL with any ticker e.g. TSLA, GOOGL
```

---

## Features Engineered
- 7-day and 21-day Moving Averages
- Daily Return Percentage
- 7-day Rolling Volatility
- Binary Target (1 = price up tomorrow, 0 = price down)

---

## Future Improvements
- [ ] Add LSTM model for comparison
- [ ] Include sentiment analysis from news headlines
- [ ] Build a simple Flask dashboard for visualisation
- [ ] Add support for multiple tickers simultaneously
- [ ] Containerise with Docker

---

## Author
**Lim Enle**  
Computer Science (AI & Big Data) — SIM–UOW  
[LinkedIn](https://www.linkedin.com/in/lim-enle-34604a217)
