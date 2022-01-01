# gitcoin-analysis
Gitcoin grants analysis tool

# Intro
I made a prototype to analyze and predict Gitcoin Grant rounds. I didnt put all the charts in my analysis but if you need to see a specific chart (function and the parameters that made the chart are shown below them) just change function parameters to the thing you want. Ill plan on making an API/CLI to make this easier but after some refactoring and upgrading to fancy looking charts.
sorry my english is not very good but ill do my best.

# Grants Overview
GR12 with 6M funding was the biggest round ever, PN.
by using Auto Regression next grants total amount predicted to be 8.8M

![Figure_1](https://user-images.githubusercontent.com/96579475/147843793-8b68b4e8-4d16-4a18-bca5-71fa839ee8e1.png)
`analyzer.plotPrediction(target="total")`

the prediction for match amount had the biggest climb and crowd contributions was the only downer

![Figure_2](https://user-images.githubusercontent.com/96579475/147843920-dbd0e9f7-84d5-4b96-818b-2eee36b9c735.png)
`analyzer.plotPrediction(target="crowdfund_amount_contributions_usd")`

# Prediction for GR13 using Auto Regression:
- total: [8794972.23459812]
- match_amount: [7717096.75481212]
- num_contributions: [524200.79098972]
- num_unique_contributors: [436252.65693899]
- crowdfund_amount_contributions_usd: [2825236.5715555]
