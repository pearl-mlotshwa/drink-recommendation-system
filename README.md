# Drink Recommendation System

## Overview
Personalised recommendations are only as good as the data behind them. 
This project was built as a practical exploration of how taste profile 
data can be used to power a content-based recommendation engine, 
specifically designed around the kind of problem a personalised 
hospitality platform would face.

## The Approach
I built a dataset of 30 drinks across six categories, cocktails, 
mocktails, beers, wines, and spirit mixes, each scored across five 
flavour attributes: sweetness, sourness, bitterness, fruitiness, 
and spiciness on a scale of 1 to 10.

Before building the model I conducted exploratory data analysis to 
understand the data. Which categories are most popular? What flavour 
profiles dominate? What correlations exist between flavour attributes 
and popularity scores? Those questions shaped both the model design 
and the final insights.

For the recommendation engine I used cosine similarity. Each drink 
is represented as a normalised flavour vector. When a user provides 
their taste preferences those scores form a preference vector, and 
cosine similarity measures the angle between that vector and every 
drink in the dataset. The smaller the angle, the closer the match. 
The closest matches get recommended.

I added occasion and alcohol level filters to make recommendations 
contextually aware. A dinner recommendation should look different from 
a party recommendation even for the same user. I validated the model 
across three distinct user profiles covering sweet and fruity, bitter 
and complex, and sour and refreshing preferences.

## Tools Used
Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

## Key Insight
Sourness has the strongest positive correlation with drink popularity 
across the dataset. A recommendation engine that weights sour leaning 
drinks higher in its default ranking will tend to surface more popular 
options, improving the user experience even before personalisation kicks in.

---
Built by Phumelele Pearl Mlotshwa
github.com/pearl-mlotshwa
pearlmlotshwa140@gmail.com
