# ⚽ Premier League Betting Model (ML Project)

Welcome! This is a personal project where I decided to combine two things I absolutely love aka football (specifically Premier League) and machine learning. The goal? try and build an intelligent model that predicts whether the **home team will win** a given Premier League match, and then use that to simulate a betting strategy and track profitability.

This isn’t just a stats project I went all the way from cleaning the data to training multiple ML models, testing betting strategies, and evaluating real-world returns (ROI). I wrote all the code myself and learned a lot while doing it.

---

## 🔍 Project Objective

> Predict the **outcome of a Premier League match (binary: Home Win or Not)** using historical match stats and simulate a simple betting strategy to test how profitable the predictions could be.

---

## 📊 Dataset

- Sourced from [Kaggle](https://www.kaggle.com/saife245/english-premier-league)
- Covers **Premier League matches from 2000 to 2019**
- Includes:  
  - Goal differences  
  - Points per team  
  - Form in last 5 matches  
  - Home/Away team indicators  
  - Final match results (H, D, A)

---

## 🧠 Models Used

I trained and compared the following ML models:

| Model                             | Accuracy | ROI (Test Set) |
|-----------------------------------|----------|----------------|
| Logistic Regression (C=0.1) (BEST)| ~65.8%   | **13.0%**      |
| Random Forest                     | ~63.9%   | 11.2%          |
| Decision Tree                     | ~57.7%   | 10.9%          |

> **Logistic Regression** came out on top and not because it was the most complex, but because it gave consistent results, strong generalization, and the highest return on investment in simulated betting.

---

## 💸 Betting Simulation

Once I had the predicted probabilities (`predict_proba()`), I simulated betting like this:
- Only bet when **Expected Value (EV) > 0**
- EV = `(probability * odds) - (1 - probability)`
- Used randomly generated realistic bookmaker odds (1.8–2.5)
- Flat stake for each bet

### ✅ Results:
- **Validation ROI:** 15.06%
- **Test ROI:** 12.99%
- 🧠 Meaning: If I placed 500+ bets using the model, I’d end up ~13% profitable which is crazy in betting.

---

## 📁 Project Structure

- PremierLeague-Betting-ML/
- ├── final_dataset 2.csv # Cleaned dataset from Kaggle
- ├── ML Code.ipynb # Main Jupyter notebook with full pipeline
- ├── README.md # You’re reading it

- ill also have a report ready ASAP
---

## 📌 What I Learned

- Logistic Regression still lowkey is the best when the data is clean and features are strong
- Overfitting isn’t just theory — Decision Trees did crazy in training but failed in the real world
- Betting ROI > accuracy if you're doing probabilistic prediction
- EV-based filtering is lowkey the secret sauce for making models actually profitable

---

## 🚧 What's Next?

This model works so now I’m thinking of:
- Turning it into a **Streamlit dashboard**
- Trying **real match data** from the current season
- Experimenting with **Kelly Criterion** and bankroll tracking
- Making it a full web app hopefully

---

## 💬 Wanna Chat?

If you're into ML, football, or both or just wanna help out over this project — feel free to clone this repo!

---

### Made with ❤️, Python, and way too many `.predict_proba()`s lmao


