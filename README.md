# 🏀 Referee Impact on NBA Game Outcomes

This project explores the influence of individual NBA referees on game outcomes — particularly focusing on whether some referees are statistically more likely to favor home teams. Using a dataset of historical NBA games, we calculate home win rates and apply statistical tests (like the Chi-Square Goodness of Fit Test) to identify referees with significantly deviant win/loss patterns.

## 📊 Objective

To analyze and visualize:

- Overall home win rates in NBA games.
- Home win rates under each referee.
- Referees whose officiating shows statistically significant deviation in home win rates using chi-square tests.

## 🛠️ Tech Stack

- **Python 3.x**
- **Pandas** for data manipulation
- **Matplotlib & Seaborn** for visualization
- **Scipy** for statistical testing
- **Jupyter Notebook** for exploratory analysis

## 📁 Project Structure

```
referee-impact-nba/
│
├── data/
│   └── nba_games.csv                # Game dataset (e.g., from basketball-reference or Kaggle)
├── notebooks/
│   └── referee_analysis.ipynb       # Jupyter Notebook with full analysis
├── README.md                        # Project description and setup guide
└── requirements.txt                 # Python dependencies
```

## 🔍 Key Features

- Computes the **overall home win rate** across all games.
- Calculates **home win rates per referee** and filters those who officiated ≥50 games.
- Performs **Chi-Square Goodness of Fit Test** to detect statistically significant deviations in referee behavior.
- Outputs a sorted list of **referees who deviate from the norm** (p < 0.05).

## ✅ Example Output

```
Overall Home Win Rate: 0.575

Referees with statistically significant home win rate deviations (p < 0.05):
| Referee         | Home_Win_Rate | Games_Officiated | p_value  |
|-----------------|----------------|------------------|----------|
| John Doe        | 0.695          | 135              | 0.0031   |
| Jane Smith      | 0.412          | 82               | 0.0248   |
```

## 📦 Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/referee-impact-nba.git
cd referee-impact-nba
```

2. Create a virtual environment and activate it:
```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Launch the Jupyter Notebook:
```bash
jupyter notebook
```

## 🧪 Requirements

Example `requirements.txt`:

```
pandas
matplotlib
seaborn
scipy
jupyter
```

## 📌 Notes

- Ensure your dataset has columns like `Referee`, `wl_home` (e.g., `'W'` or `'L'`), and game identifiers.
- This analysis assumes each game is labeled with a single referee. If multiple referees are listed per game, data preprocessing is needed.

## 📈 Future Work

- Extend analysis to **away win rates** or **point differentials**.
- Incorporate **multiple referees per game** using weighted contributions.
- Visualize trends **over seasons or years**.
- Explore **machine learning models** for predicting outcomes using referee stats.

## 🤝 Contributing

Feel free to fork this project and submit pull requests. For major changes, please open an issue first to discuss what you’d like to change.

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Made with ❤️ for NBA data science and fairness in sports.
