# Spread Locator: A Statistical Distribution Analysis Model

## 📌About the Project

This project is about understanding customer transaction data using statistical distributions. The main aim is to study transaction amounts, transaction counts and transaction status, and to check which distributions can describe the data.


## 🎯Objective

Analyse e-commerce transaction data to identify the probability distributions that best describe transaction amounts, statuses, and daily counts; apply Q-Q plots, Box-Cox transforms, and probability functions to derive business insights.

## 📂Dataset
`spread_locator_dataset.csv` — 220 transactions (Jan 2023) with columns:

- `transaction_id`
- `customer_id`
- `transaction_amount`
- `transaction_date`
- `transaction_count`
- `region`
- `transaction_status`

## 🛠️Tools and Libraries

- Python
- Jupyter Notebook
- NumPy
- Pandas
- SciPy
- Matplotlib
- Seaborn

## 📚Analysis Performed

1. Loaded the dataset and checked its basic details.
2. Studied the data using descriptive statistics.
3. Applied the Bernoulli distribution to transaction status.
4. Applied the Binomial distribution to weekly transaction count.
5. Checked the Poisson distribution for daily transaction count.
6. Modelled transaction amounts using Log-Normal and Power Law distributions.
7. Created Q-Q plots to check normality.
8. Applied the Box-Cox transformation.
9. Calculated Z-scores and the probability of transactions above ₹5,000.
10. Plotted the PDF and CDF of transaction amounts.
11. Prepared a summary of the distributions.

## 📒Files
- `Spread_Locator.ipynb` — Python full analysis notebook
- `spread_locator_dataset.csv` — Dataset used for the analysis.
- `Theory_Notes.pdf` — Part A theory notes
- `README.md` — this file
- `images/` — all labelled charts

## Key Results

| Model | Parameter | Target | Verdict |
| --- | --- | --- | --- |
| Bernoulli | p̂ = 0.445 | transaction_status | Baseline |
| Binomial(10) | p̂ = 0.285 | transaction_count | Underdispersed |
| Poisson | λ̂ ≈ 7.1 | daily counts | Mild overdispersion |
| **Log-Normal** | **μ ≈ 8.04, σ ≈ 0.50** | **transaction_amount** | **BEST FIT** |
| Power Law | α̂ ≈ 3 | upper tail | Tail-only approximation |

- P(amount > ₹5,000): **Log-Normal 0.105**, Normal 0.179, **Empirical 0.100**
- Box-Cox optimal λ ≈ 0.05 (≈ log transform)
- Q-Q: raw amounts strongly right-skewed; logs approximately Normal


## 🎓Conclusion

This project compares different statistical distributions for transaction data. The Log-Normal distribution is considered for transaction amounts, while the Power Law is checked for the upper tail. Management should model revenue via the Log-Normal mean and focus retention on the high-value tail (>₹5,000,~10% of transactions).The project also uses transformations, Q-Q plots and probability calculations to understand the spread of transaction amounts.

## ⭐ If you find this project useful

Feel free to explore the dashboard and dataset.

**Made with Python 📊**

## 👩‍💻 Author

**Jiya Patel**