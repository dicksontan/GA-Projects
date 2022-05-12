# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Capstone: Build a Trading Bot to Trade Gold for Machine Learning


### Contents:
- [Problem Statement](#Problem-Statement)
- [Datasets](#Datasets)
- [Proposed Model](#Proposed-Model)
- [Summary of Analysis](#Summary-of-Analysis)
- [Model Limitations](#Model-Limitations)
- [Future Works](#Future-Works)
- [Sources](#Sources)

---

### Problem Statement

In this project, we would like to try and find profitable trading strategies with Gold. Gold is known as a safe haven asset which investors flock to in times of makret uncertainty. This causes gold to be highly susceptible to financial events, such as when the monthly Non Farm payroll employment report releases. We would like like to build a trading bot and trade on this volatility.

---

### Datasets

We obtain our candle stick data from Oanda, which is a US based broker specializing in Forex. For pre-known financial events, we will scrape the data from Forex Factory using Beautiful Soup. Forex Factory is the number 1 site where people go to to identify important upcoming financial events. It also nicely separates events between low, medium and high importance. We will filter out only the medium and high importance to train our model.

---

### Proposed Model

In our notebooks, we have explored a general daily SARIMA Model, a momentum based strategy trading purely on volatility, a NLP model and a LSTM Model. Ultimately we found the LSTM Model to be highly profitable. A summary of the results for our LSTM Model (backtested over 7 years) is as shown below:

|Trade Type|Success Rate|Profit per Ounce|
|---|---|---|
|Long|55%|$8532|
|Short|47%|$889|
|Total|51%|$9442|



### Summary of Analysis

- In this project, we have tried a SARIMA model, momentum based strategy trading purely on volatility, a NLP model and LSTM Model. We have seen that none of the models are profitable except for our LSTM Model. With the proper risk management, our current model has backtested a yearly rate of return of ~ 21.7%.

---

### Model Limitations

- More fine-tuning has to be done on both the architecture and the number of epochs in order to achieve more accurate predictions.

- We will also need to do more analysis on the best trading thresholds to achieve maximum profitability.

### Future Works

- Modelling
    - We will need to fine-tune our model parameters as well as trading rules.
    - We can explore building a bidirectional LSTM Model

- Infrastructure
    - Build in C++/Rust for greater speed
    - Build a streaming API model instead of REST API
    - Leverage on cloud to auto-run bot

 - Usage
    - Model black swan events (e.g. 9-11 event)
    - Experiment on other volatile assets (e.g. GBPUSD)

---

### Sources

1. https://www.sciencedirect.com/science/article/pii/S0970389621000227
    
    Summary: This article compares Gold volatility as compared to other assets.
