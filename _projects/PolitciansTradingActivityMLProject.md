---
layout: project
title: 'Politician Trading Activity ML Project'
date:        1 july 2022
caption: An analysis of US House of Representatives trading activity and predicting party affiliation from stock trades
description: >
  An analysis of US House of Representatives trading activity and predicting party affiliation from stock trades
image: 
  path: /assets/img/projects/stock.jpg
  srcset: 
    1920w: /assets/img/projects/stock.jpg
    960w:  /assets/img/projects/stock@0,5x.jpg
    480w:  /assets/img/projects/stock@0,25x.jpg
links:
  - title: Source
    url: https://github.com/danielmilton22/PolitciansTradingActivityMLProject
sitemap: false
---

Here we will be diving into the current (117th) House of Representatives stock trades for the past two years. With help from the dataset provided by Timothy Carambat (https://housestockwatcher.com/api), the question I'm exploring is whether political parties in the House of Representatives have different or similiar trading activities. The dataset provides information such as the timeline of the transaction, ownership type, purchase type, and other details on the transaction. A key element missing from this dataset however, is each politicians political party which is essential in answering my question. In the following steps, I will be dissecting and analyzing my data to answer the question of whether there is a difference in stock trading behavior between political parties. I will use several exploratory data analysis methods to gauge and help answer my question.

The prediction I will be modeling is whether we can predict the politicians political party purely off of information about their stock trade. Since we are predicting a political party of either Republican or Democrat only, this will be a binary classification problem. Our response variable is the political party and I chose this to predict because I wanted to see if there truly was a fundamental differnce between how different parties trade stocks and whether I can build a model predicting the party based off of these differences. The metric we will be using is accuracy. The reason why I decided to use the accuracy metric over other metrics like the F1 score is because accuracy is easy to understand and since false negatives and false positives don't have any significant drawbacks associated with them, accuracy is a much better choice. Every row in this dataset indicates the end of a stock trade, so I am assuming that the information that will be known at the time of the prediction is timeline of the stock transaction, owner type, ticker, asset description, type of transaction, amount, name of politician who made the transaction, and whether they made capital gains of over 200 thousand from the trade.

I have all my code and my full analysis in the link above the photo.
