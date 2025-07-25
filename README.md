# Compound_Wallet_Risk_Scoring_System


### Overview
This project analyzes wallet transactions from the Compound V2/V3 protocol and assigns a **risk score (0–1000)** to each wallet based on its lending and borrowing behavior.  
The scoring logic is inspired by credit risk modeling, adapted for decentralized finance (DeFi) wallets.

---

### Features
- **Transaction Data Collection**  
  Fetched wallet transaction data using [Covalent API](https://www.covalenthq.com/) for 100 given wallets.
  
- **Feature Engineering**  
  Extracted key DeFi lending features (Borrow events, Repay events, Liquidations).  
  
- **Risk Scoring Model**  
  Assigned scores between **0–1000** using a simple formula:
score = 1000
- (liquidation_count * 50)
- (borrow_count * 10)
+ (repay_count * 20)
Scores are normalized to ensure a proper spread across risk categories.

- **Risk Categories**
- **High Risk**: Score < 400
- **Medium Risk**: 400 ≤ Score < 700
- **Low Risk**: Score ≥ 700

- **Visualization Dashboard**
- Top 10 risky wallets (bar chart)
- Risk category distribution (pie chart)
- Risk score histogram (overall score distribution)

---

## Deliverables
- **Jupyter Notebook**: End-to-end workflow (`Compound_Wallet_Risk_Scoring_Assignment.ipynb`)
- **CSV Output**: Final wallet scores (`compound_wallet_risk_scores.csv`)
- **Dashboard Visuals**: Combined charts for quick insights

---

## How to Run
1. Clone the repository:
 ```bash
 git clone <repo_url>
 cd Aave-V2-DeFi-Wallet-Credit-Scoring

