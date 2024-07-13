This section evaluates the ability of a conditional factor pricing model to explain momentum and reversal effects in stock returns. The analysis uses the Instrumented Principal Component Analysis (IPCA) model, examines out-of-sample performance, interprets findings, and explores different formation windows for momentum and reversal strategies.

### 4.1. IPCA Model in Layman's Terms 📊

The **Instrumented Principal Component Analysis (IPCA)** model is a sophisticated method used to predict stock returns by understanding how their risk exposures change over time based on observable characteristics. Let's break it down step by step:

#### What is the IPCA Model?

**IPCA** stands for Instrumented Principal Component Analysis. It’s a technique that combines principal component analysis (a statistical method to reduce data dimensions) with instruments (observable stock characteristics) to predict future returns.

#### Key Components of the IPCA Model

1. **Observable Characteristics**:
   - These are measurable traits of stocks, such as their size, value (book-to-market ratio), profitability, and past performance (momentum).
   - **Example**: For a tech company, observable characteristics could include its market capitalization, price-to-book ratio, recent profit margins, and past year’s stock performance.

2. **Latent Factors**:
   - These are hidden forces that drive stock returns but are not directly observable.
   - **Example**: Economic growth trends, technological advancements, or changes in consumer behavior.

3. **Dynamic Factor Loadings (Betas)**:
   - Betas represent how sensitive a stock is to these latent factors, and they change over time based on the stock's characteristics.
   - **Example**: If a company becomes more profitable, its sensitivity to profitability-related factors might increase.

4. **Error Term (\(\epsilon\))**:
   - This captures the part of the stock return that cannot be explained by the model.
   - **Example**: Unexpected news affecting the stock price.

#### Formula Breakdown

The IPCA model can be written as:
\[ r_{i,t+1} = (z'_{i,t} \Gamma) f_{t+1} + \epsilon_{i,t+1} \]

Where:
- \( r_{i,t+1} \) is the excess return of stock \(i\) at time \(t+1\).
- \( z_{i,t} \) is the vector of observable characteristics of stock \(i\) at time \(t\).
- \( \Gamma \) is a matrix that maps characteristics to factor loadings.
- \( f_{t+1} \) represents the latent factors at time \(t+1\).
- \( \epsilon_{i,t+1} \) is the idiosyncratic error term.

#### How Does the IPCA Model Work?

1. **Collect Data**: Gather data on stock returns and observable characteristics over time.
   - **Example**: Collect monthly return data and characteristics like size, value, profitability, and past returns for each stock.

2. **Instrument the Factors**: Use these characteristics to predict time-varying betas (factor loadings).
   - **Example**: Predict how a tech company’s profitability impacts its exposure to profitability-related risk factors.

3. **Apply PCA**: Perform principal component analysis on the instrumented data to extract latent factors.
   - **Example**: Identify underlying economic forces driving stock returns.

4. **Estimate Parameters**: Fit the IPCA model to the data by minimizing the sum of squared errors, ensuring the best fit.
   - **Example**: Adjust the model parameters to best predict future returns based on past data.

#### Real-World Example 🌍

Imagine you're an investor trying to predict how two companies, **TechFuture** and **EcoEnergy**, will perform in the future.

1. **TechFuture**:
   - **Characteristics**: Small size, high profitability, strong momentum (high past returns).
   - **Predicted Beta**: IPCA predicts TechFuture will have a high sensitivity to profitability-related factors and market movements due to its characteristics.

2. **EcoEnergy**:
   - **Characteristics**: Large size, moderate profitability, low momentum (low past returns).
   - **Predicted Beta**: IPCA predicts EcoEnergy will have a lower sensitivity to profitability-related factors and market movements compared to TechFuture.

By using the IPCA model, you can dynamically adjust your predictions based on how these companies’ characteristics change over time.

#### Why is the IPCA Model Important?

1. **Dynamic Adjustments**: It accounts for changes in risk exposures over time, making predictions more accurate.
   - **Example**: If a company becomes more profitable, the model updates its sensitivity to profitability factors.

2. **Improved Predictions**: By considering multiple characteristics and latent factors, the model provides a comprehensive view of what drives stock returns.
   - **Example**: Instead of just looking at past returns, the model considers size, value, and profitability to predict future performance.

3. **Better Risk Management**: Investors can use the model to understand the evolving risk profile of their investments.
   - **Example**: Knowing how a stock’s sensitivity to market movements changes helps in adjusting investment strategies accordingly.

### 4.2. IPCA Out of Sample

### Understanding Out-of-Sample Testing 🧩

#### What is Out-of-Sample Testing?

**Out-of-Sample Testing**: This is the process of evaluating a model’s predictive power on new data that wasn’t used to build the model. It helps to ensure that the model isn’t just fitting the noise in the data it was trained on but is actually capable of making accurate predictions in the real world.

**In-Sample vs. Out-of-Sample**:
- **In-Sample**: The data used to train and build the model.
- **Out-of-Sample**: New data used to test the model’s predictions.

### How IPCA Out-of-Sample Testing Works 📊

### Key Findings from IPCA Out-of-Sample Testing 🔍

#### Consistent Predictive Power

- **Similarity to In-Sample Results**: The IPCA model’s out-of-sample performance closely mirrors its in-sample performance, indicating the model's robustness.
- **Annualized Returns and Sharpe Ratios**:
  - **In-Sample**: The model-based expected return (Q5–Q1) yields an annualized return of 33.6% and a Sharpe ratio of 2.39.
  - **Out-of-Sample**: The same strategy yields an annualized return of 30.9% and a Sharpe ratio of 2.29.

**Example**:
- **In-Sample**: Think of this as practicing a basketball shot during training sessions. You measure how well you shoot when conditions are controlled and familiar.
- **Out-of-Sample**: This is like playing in an actual game where conditions are less predictable. If you can still shoot well, your training methods are solid.

### 4.3. Interpretation 🔍

The interpretation section aims to understand why the Instrumented Principal Component Analysis (IPCA) model successfully explains momentum and reversal effects in stock returns.

#### Key Insights from the IPCA Model

1. **Time-Varying Risk Exposure** 📉📈
   - **Explanation**: The IPCA model shows that momentum effects (where stocks that performed well in the past continue to do well) are largely due to changing risk exposures over time.
   - **Real-World Example**: Think of a sports team that has been on a winning streak. The IPCA model would suggest that this team keeps winning not just because of their skill, but because the conditions (like player health and training intensity) that influence their performance are changing over time.

2. **Capturing Momentum** 🔄
   - **Explanation**: By using stock characteristics (like size, value, profitability) to predict future risks, the model effectively captures the momentum premium.
   - **Real-World Example**: Imagine you are using a fitness tracker to predict your future running performance based on your past workouts, diet, and sleep patterns. The tracker (IPCA model) adjusts its predictions as your habits change, giving a more accurate forecast.

3. **Economic Significance** 💼
   - **Explanation**: The model-based expected returns (based on predicted betas) provide a stronger explanation for stock performance than traditional momentum signals alone.
   - **Real-World Example**: If you’re investing in a tech company, traditional analysis might just look at past stock prices. The IPCA model, however, considers how factors like the company's recent investments in innovation or changes in profitability will affect future returns.

4. **Explaining Reversals** 🔄
   - **Explanation**: The model also explains long-term reversals (where stocks that have done well for a long time start to underperform) by showing how risk exposures evolve.
   - **Real-World Example**: If an athlete has been performing exceptionally well for several years, they might eventually face burnout or injuries, leading to a decline in performance. The IPCA model anticipates such changes by adjusting risk predictions over time.

### 4.4. Other Formation Windows 📆

The analysis in this section investigates how different time periods for measuring past returns (formation windows) affect the ability to predict future stock performance using the IPCA model.

#### Formation Windows

1. **Short-Term Momentum (2-12 Months)** 📅
   - **Explanation**: This measures the average return over the past year, excluding the most recent month.
   - **Real-World Example**: Looking at a student’s grades over the last school year, excluding the current month, to predict their final exam performance.

2. **Long-Term Reversal (13-24 Months and 25-36 Months)** 📉
   - **Explanation**: This looks at returns over longer periods to capture long-term trends and potential reversals.
   - **Real-World Example**: Considering an employee’s performance reviews over the past two to three years to assess their future promotion potential.

3. **Short-Term Reversal (1 Month)** 🔄
   - **Explanation**: This measures the very recent past return to capture immediate reversals, often driven by liquidity or market overreaction.
   - **Real-World Example**: Checking how a stock performed last month to decide if it’s likely to bounce back or continue declining.

#### Findings from Different Formation Windows

1. **Short-Term Momentum**:
   - **Explanation**: Momentum based on the past 2-12 months remains a strong predictor of future returns.
   - **Real-World Example**: If a stock has done well for almost the entire past year, it's likely to keep doing well in the short term, according to the model.

2. **Long-Term Reversal**:
   - **Explanation**: Returns over the past 13-36 months can predict future underperformance, but this effect is captured by the IPCA model’s time-varying risk exposures.
   - **Real-World Example**: A company that has been highly profitable for the last three years might start to underperform as market conditions change, which the model can predict by adjusting the risk exposure.

3. **Short-Term Reversal**:
   - **Explanation**: The most recent month’s return often shows a significant reversal effect, likely driven by short-term liquidity issues or market overreactions.
   - **Real-World Example**: If a stock dropped significantly last month due to temporary bad news, it might rebound quickly, reflecting a short-term reversal.

### Calculating Momentum, Long-Term Reversal, and Short-Term Reversal

**Momentum, long-term reversal, and short-term reversal** are important factors in stock return predictions. Here’s how they are calculated as input features in real life:

#### 1. Momentum

**Momentum** measures the tendency of stocks that have performed well in the past to continue performing well in the future. It is typically calculated using past returns over a specified period, excluding the most recent month to avoid short-term reversal effects.

**Calculation**:
- **Formula**: \( \text{Momentum}_{i,t} = \sum_{j=t-12}^{t-2} r_{i,j} \)
  - \( \text{Momentum}_{i,t} \): Momentum for stock \(i\) at time \(t\).
  - \( r_{i,j} \): Return of stock \(i\) in month \(j\).
  - Sum returns over the past 12 months, excluding the most recent month.
  
**Example**:
- If the current month is December 2023, you would sum the returns from December 2022 to November 2023 to calculate momentum.

#### 2. Long-Term Reversal

**Long-Term Reversal** measures the tendency of stocks that have performed well over a longer period (e.g., 2 to 3 years) to start underperforming.

**Calculation**:
- **Formula**: \( \text{Long-Term Reversal}_{i,t} = \sum_{j=t-36}^{t-13} r_{i,j} \)
  - \( \text{Long-Term Reversal}_{i,t} \): Long-term reversal for stock \(i\) at time \(t\).
  - \( r_{i,j} \): Return of stock \(i\) in month \(j\).
  - Sum returns from 36 months ago to 13 months ago.

**Example**:
- If the current month is December 2023, you would sum the returns from December 2020 to November 2022 to calculate long-term reversal.

#### 3. Short-Term Reversal

**Short-Term Reversal** measures the tendency of stocks that have experienced recent extreme returns (e.g., the last month) to reverse their performance.

**Calculation**:
- **Formula**: \( \text{Short-Term Reversal}_{i,t} = r_{i,t-1} \)
  - \( \text{Short-Term Reversal}_{i,t} \): Short-term reversal for stock \(i\) at time \(t\).
  - \( r_{i,t-1} \): Return of stock \(i\) in the previous month.

**Example**:
- If the current month is December 2023, the return in November 2023 is used to calculate short-term reversal.

### Dynamic Betas

**Dynamic Betas** refer to the time-varying sensitivities of stock returns to various risk factors. Unlike static betas, which remain constant over time, dynamic betas adjust based on changing characteristics of stocks.

#### Calculation of Dynamic Betas

1. **Observable Characteristics**: Use stock characteristics (size, value, profitability, investment, momentum, etc.) as instruments to predict betas.
2. **Principal Component Analysis (PCA)**: Perform PCA on the instrumented data to identify latent factors driving stock returns.
3. **Time-Varying Factor Loadings**: Estimate betas as a function of these characteristics, allowing them to change over time.

**Formula**:
\[ \beta_{i,t} = z_{i,t} \Gamma \]
- \( \beta_{i,t} \): Dynamic beta for stock \(i\) at time \(t\).
- \( z_{i,t} \): Vector of observable characteristics for stock \(i\) at time \(t\).
- \( \Gamma \): Matrix of coefficients mapping characteristics to betas.

**Example**:
- If a company’s profitability increases, its beta with respect to profitability-related factors might also increase.

### Regression Analysis

**Regression Analysis** is used to link dynamic betas and stock characteristics to predict future returns. It helps to quantify the relationship between independent variables (characteristics) and dependent variables (future returns).

#### Steps in Regression Analysis

1. **Specify the Model**:
   - Define the dependent variable (future stock returns) and independent variables (current characteristics and dynamic betas).

2. **Estimate the Model**:
   - Use Ordinary Least Squares (OLS) or another estimation method to fit the model.

3. **Evaluate the Model**:
   - Assess the model’s goodness-of-fit using statistical metrics like R-squared, and check for significance of coefficients.

#### Example Model

**Regression Model**:
\[ r_{i,t+1} = a + b_h r_{i,t-12,t-2} + C'_h X_{i,t-1} + \epsilon_{i,t+1} \]
- \( r_{i,t+1} \): Future return of stock \(i\) at time \(t+1\).
- \( r_{i,t-12,t-2} \): Momentum characteristic (returns from 12 to 2 months prior).
- \( X_{i,t-1} \): Vector of other characteristics at time \(t-1\).
- \( a \): Intercept.
- \( b_h \): Coefficient for momentum.
- \( C'_h \): Coefficients for other characteristics.
- \( \epsilon_{i,t+1} \): Error term.

**Steps**:
1. **Collect Data**: Gather historical returns and characteristics for stocks.
2. **Calculate Features**: Compute momentum, long-term reversal, and short-term reversal.
3. **Estimate Betas**: Use PCA and characteristics to estimate dynamic betas.
4. **Run Regression**: Fit the regression model to predict future returns.

**Example**:
- Suppose you want to predict the return of Stock A for January 2024. Using its characteristics as of December 2023 and its dynamic beta estimates, run the regression to get the predicted return.

### Summary

- **Input Features**: Size, value, profitability, investment, momentum, long-term reversal, short-term reversal.
- **Dynamic Betas**: Time-varying sensitivities to latent risk factors, calculated using PCA and observable characteristics.
- **Regression Analysis**: Used to predict future returns based on current characteristics and dynamic betas, helping to identify the importance of momentum and reversal in stock performance.

By following these steps and using these calculations, the IPCA model effectively identifies and leverages momentum and reversal factors to predict stock returns.

Let's create a real-world example with dummy data to demonstrate how to calculate momentum, long-term reversal, short-term reversal, and dynamic betas, and perform regression analysis.

### 1. Dummy Data
#### Stock Characteristics and Returns

We'll use a dataset of three stocks (A, B, C) over a period of 36 months. The table below shows the monthly returns and characteristics for each stock.

**Table: Monthly Returns and Characteristics**

| Month | Stock | Return | Size  | Value | Profitability | Investment |
|-------|-------|--------|-------|-------|---------------|------------|
| M1    | A     | 2%     | 1.2   | 0.8   | 0.6           | 0.5        |
| M2    | A     | -1%    | 1.3   | 0.7   | 0.7           | 0.4        |
| ...   | ...   | ...    | ...   | ...   | ...           | ...        |
| M35   | A     | 3%     | 1.5   | 0.9   | 0.8           | 0.3        |
| M36   | A     | 4%     | 1.4   | 0.8   | 0.9           | 0.2        |
| M1    | B     | -2%    | 1.1   | 0.6   | 0.5           | 0.4        |
| M2    | B     | 1%     | 1.2   | 0.5   | 0.6           | 0.5        |
| ...   | ...   | ...    | ...   | ...   | ...           | ...        |
| M35   | B     | -1%    | 1.3   | 0.7   | 0.7           | 0.4        |
| M36   | B     | 2%     | 1.2   | 0.6   | 0.8           | 0.3        |
| M1    | C     | 3%     | 1.0   | 0.5   | 0.6           | 0.5        |
| M2    | C     | 2%     | 1.1   | 0.6   | 0.7           | 0.4        |
| ...   | ...   | ...    | ...   | ...   | ...           | ...        |
| M35   | C     | 1%     | 1.3   | 0.8   | 0.8           | 0.5        |
| M36   | C     | -1%    | 1.2   | 0.7   | 0.7           | 0.4        |

### 2. Calculate Momentum, Long-Term Reversal, and Short-Term Reversal

#### Momentum
**Formula**: \( \text{Momentum}_{i,t} = \sum_{j=t-12}^{t-2} r_{i,j} \)

For Stock A at Month 36 (M36):
\[
\text{Momentum}_{A,M36} = \sum_{j=M24}^{M34} r_{A,j}
\]
Assume the returns from M24 to M34 for Stock A are as follows:

| Month | Return |
|-------|--------|
| M24   | 1%     |
| M25   | 2%     |
| M26   | -1%    |
| M27   | 0%     |
| M28   | 3%     |
| M29   | -2%    |
| M30   | 1%     |
| M31   | 2%     |
| M32   | 1%     |
| M33   | -1%    |
| M34   | 0%     |

\[
\text{Momentum}_{A,M36} = 1\% + 2\% - 1\% + 0\% + 3\% - 2\% + 1\% + 2\% + 1\% - 1\% + 0\% = 6\%
\]

#### Long-Term Reversal
**Formula**: \( \text{Long-Term Reversal}_{i,t} = \sum_{j=t-36}^{t-13} r_{i,j} \)

For Stock A at Month 36 (M36):
\[
\text{Long-Term Reversal}_{A,M36} = \sum_{j=M1}^{M23} r_{A,j}
\]
Assume the returns from M1 to M23 for Stock A are as follows:

| Month | Return |
|-------|--------|
| M1    | 2%     |
| M2    | -1%    |
| ...   | ...    |
| M22   | 3%     |
| M23   | 2%     |

\[
\text{Long-Term Reversal}_{A,M36} = 2\% - 1\% + ... + 3\% + 2\% = X\% \quad \text{(sum all returns from M1 to M23)}
\]

#### Short-Term Reversal
**Formula**: \( \text{Short-Term Reversal}_{i,t} = r_{i,t-1} \)

For Stock A at Month 36 (M36):
\[
\text{Short-Term Reversal}_{A,M36} = r_{A,M35} = 3\%
\]

### 3. Dynamic Betas

Dynamic betas are estimated using observable characteristics and PCA. For simplicity, let's assume we've performed PCA and have the following dynamic betas for Stock A based on its characteristics.

#### Characteristics and Betas for Stock A at Month 36:
- **Size**: 1.4
- **Value**: 0.8
- **Profitability**: 0.9
- **Investment**: 0.2

**Dynamic Beta Calculation**:
\[
\beta_{A,M36} = z_{A,M36} \Gamma
\]
Assume \( \Gamma \) is given by:
\[
\Gamma = \begin{bmatrix}
0.1 \\
0.2 \\
0.3 \\
0.4 \\
\end{bmatrix}
\]

\[
z_{A,M36} = \begin{bmatrix}
1.4 & 0.8 & 0.9 & 0.2
\end{bmatrix}
\]

\[
\beta_{A,M36} = \begin{bmatrix}
1.4 & 0.8 & 0.9 & 0.2
\end{bmatrix} \begin{bmatrix}
0.1 \\
0.2 \\
0.3 \\
0.4 \\
\end{bmatrix} = 1.4 \times 0.1 + 0.8 \times 0.2 + 0.9 \times 0.3 + 0.2 \times 0.4 = 0.14 + 0.16 + 0.27 + 0.08 = 0.65
\]

### 4. Regression Analysis

#### Data Preparation
**Inputs**:
- Momentum (6%)
- Long-Term Reversal (X%)
- Short-Term Reversal (3%)
- Dynamic Beta (0.65)

**Output**:
- Future Return (predicted return for next month, e.g., M37)

#### Regression Model
\[ r_{i,t+1} = a + b_h \times \text{Momentum}_{i,t} + c_h \times \text{Long-Term Reversal}_{i,t} + d_h \times \text{Short-Term Reversal}_{i,t} + e_h \times \beta_{i,t} + \epsilon_{i,t+1} \]

**Example**:
Let's assume we have coefficients:
- \(a = 0.01\)
- \(b_h = 0.02\)
- \(c_h = 0.03\)
- \(d_h = 0.04\)
- \(e_h = 0.05\)

**Substitute Values**:
\[
r_{A,M37} = 0.01 + 0.02 \times 6\% + 0.03 \times X\% + 0.04 \times 3\% + 0.05 \times 0.65
\]
Assuming \(X = 10\%\):
\[
r_{A,M37} = 0.01 + 0.02 \times 6 + 0.03 \times 10 + 0.04 \times 3 + 0.05 \times 0.65
\]
\[
r_{A,M37} = 0.01 + 0.12 + 0.30 + 0.12 + 0.0325 = 0.5945 \approx 5.95\%
\]

### Summary
- **Momentum**: 6%
- **Long-Term Reversal**: 10%
- **Short-Term Reversal**: 3%
- **Dynamic Beta**: 0.65
- **Predicted Return**: 5.95%

This example shows how to calculate the key features and use them in a regression model to predict

### Dynamic Beta Calculation and IPCA Model Explanation

#### Dynamic Beta Calculation

**Dynamic Betas** reflect the time-varying sensitivities of stock returns to latent risk factors, calculated using observable characteristics and PCA.

**Steps to Calculate Dynamic Betas**:

1. **Collect Observable Characteristics**: Gather data on stock characteristics such as size, value, profitability, investment, momentum, etc.

2. **Estimate Dynamic Betas**: Use these characteristics to estimate time-varying factor loadings (betas) through PCA and regression techniques.

**Example Calculation**:

1. **Observable Characteristics**:
   - Size: 1.4
   - Value: 0.8
   - Profitability: 0.9
   - Investment: 0.2

2. **Gamma Matrix (\(\Gamma\))**: A matrix of coefficients mapping characteristics to betas. Assume \(\Gamma\) is derived from PCA and regression analysis:
   \[
   \Gamma = \begin{bmatrix}
   0.1 \\
   0.2 \\
   0.3 \\
   0.4 \\
   \end{bmatrix}
   \]

3. **Calculate Dynamic Beta**:
   \[
   z_{A,M36} = \begin{bmatrix}
   1.4 & 0.8 & 0.9 & 0.2
   \end{bmatrix}
   \]

   \[
   \beta_{A,M36} = \begin{bmatrix}
   1.4 & 0.8 & 0.9 & 0.2
   \end{bmatrix} \begin{bmatrix}
   0.1 \\
   0.2 \\
   0.3 \\
   0.4 \\
   \end{bmatrix} = 1.4 \times 0.1 + 0.8 \times 0.2 + 0.9 \times 0.3 + 0.2 \times 0.4 = 0.14 + 0.16 + 0.27 + 0.08 = 0.65
   \]

#### Latent Features and IPCA

**Latent Features**: Unobservable factors driving stock returns, estimated through PCA.

**IPCA (Instrumented Principal Component Analysis)**:

1. **Principal Component Analysis (PCA)**: Identify latent factors driving stock returns.
   - **Latent Factors (f)**: Extract principal components (e.g., economic growth, market trends).

2. **Dynamic Factor Loadings (\(\beta\))**: Calculate how each stock's returns are sensitive to these latent factors using observable characteristics.

**Usage**:
- **Latent Factors in Prediction**: Combined with observable characteristics to dynamically adjust betas, improving prediction accuracy.

#### Gamma Matrix (\(\Gamma\)) Calculation

1. **Perform PCA**: Extract principal components (latent factors) from historical data on returns and characteristics.

2. **Regression Analysis**: Regress dynamic betas on observable characteristics to estimate \(\Gamma\).

**Example**:
- Use PCA to identify latent factors (e.g., market trend, economic growth).
- Regress betas on characteristics (size, value, etc.) to estimate \(\Gamma\).

### Regression Coefficients (a, b, c, d, e) Calculation

1. **Specify the Regression Model**:
   \[
   r_{i,t+1} = a + b_h \times \text{Momentum}_{i,t} + c_h \times \text{Long-Term Reversal}_{i,t} + d_h \times \text{Short-Term Reversal}_{i,t} + e_h \times \beta_{i,t} + \epsilon_{i,t+1}
   \]

2. **Collect Data**: Gather historical data on stock returns and characteristics.

3. **Estimate Coefficients (a, b, c, d, e)**:
   - **Ordinary Least Squares (OLS)**: Use OLS regression to estimate coefficients.
   - **Minimize Residuals**: Adjust coefficients to minimize the sum of squared residuals (differences between actual and predicted returns).

**Example**:
- Assume you have data for multiple stocks over several periods.
- Fit the model using OLS to estimate the coefficients.

### Rough Example of Calculations

#### Observable Characteristics and Dynamic Betas

| Stock | Month | Size | Value | Profitability | Investment | Momentum | LTR | STR | Return | Dynamic Beta (β) |
|-------|-------|------|-------|---------------|------------|----------|-----|-----|--------|------------------|
| A     | M36   | 1.4  | 0.8   | 0.9           | 0.2        | 6%       | 10% | 3%  | 5%     | 0.65             |
| B     | M36   | 1.2  | 0.7   | 0.8           | 0.3        | 4%       | 8%  | -2% | 3%     | 0.55             |
| C     | M36   | 1.3  | 0.9   | 0.7           | 0.4        | 7%       | 9%  | 1%  | -1%    | 0.60             |

#### Regression Analysis

- Collect data for multiple periods and stocks.
- Perform OLS regression to estimate coefficients.

**Regression Model**:
\[
r_{i,t+1} = a + b_h \times \text{Momentum}_{i,t} + c_h \times \text{Long-Term Reversal}_{i,t} + d_h \times \text{Short-Term Reversal}_{i,t} + e_h \times \beta_{i,t} + \epsilon_{i,t+1}
\]

**Assumed Coefficients**:
- \(a = 0.01\)
- \(b_h = 0.02\)
- \(c_h = 0.03\)
- \(d_h = 0.04\)
- \(e_h = 0.05\)

**Example Calculation for Stock A**:
\[
r_{A,M37} = 0.01 + 0.02 \times 6\% + 0.03 \times 10\% + 0.04 \times 3\% + 0.05 \times 0.65
\]
\[
r_{A,M37} = 0.01 + 0.12 + 0.30 + 0.12 + 0.0325 = 0.5945 \approx 5.95\%
\]

This detailed example covers the calculation of dynamic betas, the role of latent factors in the IPCA model, the estimation of the Gamma matrix, and the calculation of regression coefficients using OLS.
