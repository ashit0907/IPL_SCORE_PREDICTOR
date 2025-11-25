# 📌 IPL Score Predictor

This project predicts **first-innings IPL scores** using real match data.
It performs **data preprocessing, encoding, feature engineering**, and evaluates **multiple regression models** to understand how match context affects the final score.

---

## 🚀 Objective

Predict the **total runs scored by a team in the first innings**, based on:

* Venue
* Batting team
* Bowling team
* Match date
* Over count
* Current wickets
* Recent runs

---

## 📂 Dataset

The dataset used contains past IPL match data with ball-by-ball information aggregated at over-level.

📌 Columns include:

* `batting_team`
* `bowling_team`
* `venue`
* `runs_last_5`
* `wickets`
* `overs`
* `current_score`
* …and more contextual features

> **A sample dataset is included** (`ipl_colab.csv`) for demonstration.
> The trained model files are **not uploaded due to size constraints**.

---

## 🧠 Models Used

Several regression models were trained and tested:

* **Linear Regression**
* **Decision Tree Regressor**
* **Random Forest Regressor**
* **Lasso Regression**
* **Support Vector Regressor (SVR)**
* **Multilayer Perceptron (MLP)**

Random Forest performed well overall due to its ability to handle nonlinear relationships and high-dimensional feature interactions.

> SVM and MLP models were computationally heavier on the full dataset (75k+ rows), so experiments were also tested on subsets.

---

## 🛠️ Tech Stack

* Python
* Pandas / NumPy
* Scikit-Learn
* Matplotlib / Seaborn
* Joblib

---

## ▶️ How to Run

### 1️⃣ Clone the repo

```bash
git clone https://github.com/<your-username>/IPL_SCORE_PREDICTOR.git
cd IPL_SCORE_PREDICTOR
```

### 2️⃣ Create a virtual environment

```bash
python -m venv venv
```

Activate it:

**PowerShell**

```bash
.\venv\Scripts\activate
```

**CMD**

```bash
venv\Scripts\activate.bat
```

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Launch the notebook

```bash
jupyter notebook
```

Then open:
**`IPL_Score_Predictor.ipynb`**

---

## 📈 Results (Short Summary)

* Feature encoding improved model stability.
* Random Forest delivered strong predictions without heavy feature engineering.
* Neural Networks and SVR provided good results but required more compute time.

---

## 📦 Model Training

Models can be retrained by running the notebook.
Pickle/Joblib files are not uploaded due to GitHub file size limits.

---

## 📌 Future Improvements

* Hyperparameter tuning (GridSearch / Optuna)
* Ensemble methods
* Upload trained model via model registry / HuggingFace
* Web dashboard for score prediction

---

## 🪪 License

This project is released under the **MIT License**.

---
