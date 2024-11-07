# Portfolio-Optimization

## Introduction
Portfolio optimization is the process of selecting an optimal portfolio (asset distribution), out of a set of considered portfolios, according to some objective. The objective typically maximizes factors such as expected return, and minimizes costs like financial risk, resulting in a multi-objective optimization problem.

The objective of this project is to optimize an all-equity portfolio using past 6 months of OHLC data. For this purpose, I've used my own active portfolio and optimized it using two approaches: Monte Carlo Simulation & Constraints-based optimization. We will perform Monte Carlo Simulation using a manual function and will utilise scipy.optimize package to perform optimization using constraints.

Portfolio - MOTHERSON, SUZLON, ZOMATO

## Methodology

### Monte Carlo Simulation
1. We will use a randomly-allocated portfolio as our base portfolio for this approach and try to optimize this allocation based on Sharpe ratio
2. 1000 simulations will be generated of the portfolio with the intention to pull 3 portfolios: Max. Return, Max. Sharpe, Min. Risk

### Constraints-based
1. We will use `scipy.optimize` to optimize our portfolio
2. As the base portfolio, we will use my live active portfolio allocation and try to optimize it for better risk-return tradeoff
3. Since `scipy.otpimize` only has a **minimization** function, we will convert sharpe ratio into negative and minimize the metric. The minimum ratio will be the maximum ratio in its original form

## Results

### Monte Carlo Simulation

Randomly-allocated Portfolio

- MOTHERSON 57%
- SUZLON 1%
- ZOMATO 42%

![image](https://github.com/user-attachments/assets/fba2c04b-215c-44d4-8cba-b81034c29dc3)

The 3 portfolios pulled:

![image](https://github.com/user-attachments/assets/dcaae440-cf7a-43ac-a3ac-449538a152a2)

![image](https://github.com/user-attachments/assets/a121bfd5-7116-4b09-a35f-d1c284813c6b)

![image](https://github.com/user-attachments/assets/915a71c8-7bd5-4815-bfeb-76cba0fca3e1)


### Constraints-based Optimization

Live Active Portfolio

- MOTHERSON 23%
- SUZLON 32%
- ZOMATO 45%

This approach will only generate a single optimized portfolio based on the metric we define, which is max. sharpe in this case:

![image](https://github.com/user-attachments/assets/7c4fa768-2c5c-45ca-a721-761b45a6be20)



