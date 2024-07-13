### 2. Past Returns Predict Betas

This section demonstrates how past returns can forecast future risk, specifically through the realized betas of stocks. Betas measure a stock's volatility relative to the overall market and are a crucial part of understanding risk and return in finance.

#### 2.1. Data 📊

**Data Overview**:
- **Time Span**: 1966 to 2014.
- **Sources**: Stock returns and 36 characteristics from Freyberger et al. (2020).
- **Scope**: 12,813 unique stocks, resulting in 1,403,544 stock-month observations.

**Handling Outliers**:
- **Normalization**: Each characteristic is cross-sectionally ranked, divided by the number of stocks in the cross-section, and then demeaned to fall within the [-0.5, 0.5] range. This normalization process helps manage outliers and ensures consistency in the data.

#### 2.2. Market Beta Prediction Results 📈

**Market Beta**: A measure of a stock's volatility relative to the market. A beta greater than 1 indicates higher volatility than the market, while a beta less than 1 indicates lower volatility.

**Objective**:
- **Examining Predictability**: The goal is to see if past returns can predict future market betas, which helps in understanding how stocks might behave in response to market movements.

**Methodology**:
- **OLS Betas**: Monthly realized Ordinary Least Squares (OLS) betas are calculated using daily returns within the month. Betas are also computed quarterly, semiannually, and annually.
- **Regression Model**: The regression model used is:
  \[
  \beta_{t,t+h} = a + b_h r_{t-12,t-2} + C'_h X_{t-1} + \epsilon_{t,t+h}
  \]
  where:
  - \(\beta_{t,t+h}\) represents the realized beta over different future periods (1 month, 3 months, 6 months, 12 months).
  - \(r_{t-12,t-2}\) represents the momentum characteristic (returns from 12 to 2 months prior).
  - \(X_{t-1}\) includes other characteristics of stocks at time \(t-1\).

**Findings**:
- **Strong Predictor**: Momentum (past returns from 12 to 2 months ago) is a strong predictor of future market betas.
  - **Example**: Moving from the 10th to the 90th percentile in momentum increases a stock's market beta by 0.18, implying an 18% increase in market risk premium.

**Economic Significance**:
- **Beta Increase and Returns**: The increase in market beta alone (0.18) is not enough to explain the 8%-9% momentum premium, suggesting other factors must be considered. Hence, the conditional CAPM (which only considers time-varying market beta) cannot fully capture momentum profits.

**Long-Term and Short-Term Reversal**:
- **Long-Term Reversal**: Based on 3-5 year past returns, significantly predicts future market betas, though less strongly than momentum.
- **Short-Term Reversal**: Based on 1-month past returns, has weak predictive power for future market betas, aligning with the idea that short-term reversals are more about liquidity effects than risk changes.

#### 2.3. Multifactor Beta Prediction Results 📊

**Multifactor Models**: These models include multiple factors (beyond just market beta) to capture different aspects of risk and return.

**Objective**:
- **Expanding Analysis**: Assess how past returns predict betas for multiple factors used in asset pricing models, like the Fama and French five-factor model.

**Factors Considered**:
- **SMB (Small Minus Big)**: Captures size factor, the return difference between small-cap and large-cap stocks.
- **HML (High Minus Low)**: Captures value factor, the return difference between value and growth stocks.
- **RMW (Robust Minus Weak)**: Captures profitability factor, the return difference between highly profitable and less profitable stocks.
- **CMA (Conservative Minus Aggressive)**: Captures investment factor, the return difference between conservatively and aggressively investing firms.

**Findings**:
- **Predictive Power**: Momentum strongly predicts beta exposure to HML, RMW, and CMA, even after controlling for the characteristics these factors are based on (book-to-market, gross profitability, investment).
- **Long-Term Reversal**: Also shows significant predictability for future betas on all four factors.
- **Short-Term Reversal**: Shows small and insignificant predictability, supporting its interpretation as a liquidity-driven phenomenon.

### Terminologies Explained 🧑‍🏫

- **Beta (β)**: Measures a stock's volatility relative to the overall market. A beta of 1 means the stock moves with the market, greater than 1 means more volatile, less than 1 means less volatile.
- **OLS (Ordinary Least Squares)**: A method to estimate the relationships in a regression model.
- **Momentum**: The tendency of stocks that have performed well in the past to continue performing well.
- **Long-Term Reversal**: The tendency of stocks that have performed well over a long period to start performing poorly.
- **Short-Term Reversal**: The tendency of stocks that have performed well over a very short period (like one month) to reverse their performance.
- **Multifactor Model**: An asset pricing model that includes multiple factors to explain returns. Factors could include market risk, size, value, profitability, and investment.

### Detailed Elaboration with Real-World Examples 🌍

### Objective: Examining Predictability 📈

#### Examining Predictability
The primary objective is to determine if past returns can predict future market betas. Understanding this relationship helps investors gauge how stocks might behave in response to market movements, aiding in the development of more accurate investment strategies.

### Findings: Momentum as a Strong Predictor

#### Momentum as a Strong Predictor
**Momentum** (past returns from 12 to 2 months ago) is found to be a strong predictor of future market betas. Here's a breakdown:

- **Past Returns**: Stocks that have performed well in the past 12 to 2 months tend to have higher future market betas.
- **Real-World Example**: Suppose you have two stocks, A and B. Stock A has been performing exceptionally well over the past 10 months (high momentum), while Stock B has been performing poorly. If Stock A is in the 90th percentile for momentum and Stock B is in the 10th percentile, Stock A’s market beta will increase by 0.18 compared to Stock B. This implies an 18% higher market risk premium for Stock A.

### Real-World Example and Terminology Explanation 🌍

### Example: Predicting Betas Using Momentum

#### Scenario:

- **Stock A**: Performing exceptionally well over the past 10 months.
- **Stock B**: Performing poorly over the past 10 months.
- **Momentum Percentiles**: 
  - **Stock A**: In the 90th percentile (top 10% of performers).
  - **Stock B**: In the 10th percentile (bottom 10% of performers).

**Key Points**:
1. **Stock A's Market Beta Increase**: Moving from the 10th percentile to the 90th percentile in momentum increases Stock A's market beta by 0.18.
2. **Market Risk Premium**: This beta increase implies an 18% higher market risk premium for Stock A compared to Stock B.

### Detailed Explanation of Terms 📚

#### Percentile 🧮
- **Definition**: A percentile is a measure used in statistics indicating the value below which a given percentage of observations fall.
- **Example**: If Stock A is in the 90th percentile, it means Stock A performed better than 90% of all other stocks over the past 10 months. Conversely, if Stock B is in the 10th percentile, it performed better than only 10% of the stocks, making it one of the poorer performers.

#### Market Beta (β) 📊
- **Definition**: Market beta measures a stock's volatility relative to the overall market. It indicates how much a stock's price moves in relation to the market.
  - **Beta = 1**: The stock moves in line with the market.
  - **Beta > 1**: The stock is more volatile than the market.
  - **Beta < 1**: The stock is less volatile than the market.
- **Example**: If Stock A’s beta is 1.2, it means the stock is 20% more volatile than the market. If the market goes up by 10%, Stock A is expected to go up by 12%.

#### Market Risk Premium 📈
- **Definition**: The market risk premium is the additional return an investor expects to earn from holding a risky market portfolio instead of risk-free assets.
  - **Calculation**: Market Risk Premium = Expected Market Return - Risk-Free Rate.
- **Example**: If the risk-free rate (e.g., return on Treasury bonds) is 2% and the expected market return is 8%, the market risk premium is 6%.

### Applying the Example 🌍

#### Step-by-Step Breakdown:

1. **Momentum Percentiles**:
   - **Stock A**: High momentum, in the 90th percentile.
   - **Stock B**: Low momentum, in the 10th percentile.

2. **Market Beta Increase**:
   - Moving from Stock B (10th percentile) to Stock A (90th percentile) increases the beta by 0.18. This means Stock A’s beta is 0.18 higher than Stock B's.
   - **Example**: If Stock B’s beta is 1.0, Stock A’s beta will be 1.18.

3. **Market Risk Premium Implications**:
   - **Market Risk Premium**: If the market risk premium is 6%, an 0.18 increase in beta translates to an additional return of:
     \[
     0.18 \times 6\% = 1.08\%
     \]
   - **Interpretation**: Stock A is expected to earn 1.08% more in return due to its higher beta compared to Stock B, assuming the market risk premium remains constant.

#### Real-World Analogy 🌟

Imagine you're comparing two athletes:
- **Athlete A**: Always finishes races in the top 10% (90th percentile).
- **Athlete B**: Often finishes in the bottom 10% (10th percentile).

Just like how Athlete A’s consistent performance places them in the top tier, Stock A’s high past returns place it in the high momentum category. The increased beta of Stock A means it's expected to "run faster" or be more volatile than Stock B when the market moves, resulting in a higher expected return (market risk premium).

**Economic Significance**:
- **Beta Increase and Returns**: While the increase in beta (0.18) indicates a higher risk, it only explains a small portion (1.1 percentage points) of the momentum premium (8%-9%). This suggests that factors beyond market beta must be considered to fully capture momentum profits. Thus, the conditional CAPM, which only considers time-varying market beta, falls short.


