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
- total: [8,794,972.23459812]
- match_amount: [7,717,096.75481212]
- num_contributions: [524,200.79098972]
- num_unique_contributors: [436,252.65693899]
- crowdfund_amount_contributions_usd: [2,825,236.5715555]



# Weird Regions
with asia dividing into 4 seperate regions `Middle East, India, East Asia, South East Asia` this part is a little weird. I was too scared too fix it so heres the overview:

![Figure_3](https://user-images.githubusercontent.com/96579475/147844020-31c7f06e-b6ac-47ca-9594-c873081289b3.png)
`analyzer.plotNested(target="total", subGroup="region_s")`

`NA and EU` were even bigger than before. charts a little blur if you want to see better use the script to get the dynamic chart

# Funding(Percentage) By Region
"unknown" region in GR12 had the lowest % of the round ever with `East asia` and `Africa` being the biggest losers than GR11
using Auto Reggression only `Oceania` and `India` having the most potential and others had very little change

![Figure_4](https://user-images.githubusercontent.com/96579475/147844241-fd9f6e36-6606-4f3f-88f5-32ba01647db2.png)
`analyzer.plotByTotal(target="match_amount", subGroup="region_s", operation="div")`



Match amount only in `NA and EU` was bigger than the crowd contribution
![Figure_6](https://user-images.githubusercontent.com/96579475/147844421-79aaa1d5-012d-4499-a0b6-4c74972d00c6.png)
`analyzer.plotRatio(col1="crowdfund_amount_contributions_usd", col2="match_amount", subGroup="region_s")`

# Unique Contributer ratio
GR12 ratio shows the total funding had a high amount of unique contributers and more people contributed multiple times than GR11 and with this huge amount shows an impressive growth

![Figure_5](https://user-images.githubusercontent.com/96579475/147844352-b93c6ba6-d93a-44d5-a71e-b41fdd91b5b8.png)
`analyzer.plotRatio(col1="num_contributions", col2="num_unique_contributors", subGroup="region_s")`



# TODO
- atleast 10 more prediction models 
- fancy charts
- Api/CLI
