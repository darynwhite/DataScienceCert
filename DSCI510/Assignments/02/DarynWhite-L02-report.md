# Data Science Cert | Process & Tools | Lesson 02

## Pythian : Predictive Maintenance of mining haulers

### Business Problem

The mining company wanted to increase their ability to predict potential catastrophic failures for multiple reasons, but all the reasons ultimately lead to a small cascade of revenue loss for every catastrophic failure due to a hauler being down and causing others to idle. The better predictions can get leads to less failures and less time with haulers stopped.

Pythian approached the problem with a couple of advantages because the mining company was already capturing and storing a lot of data from each hauler (approx. 2GB per day) from mulitple sensors onboard each hauler. The data volume and domain experts, the mining company employes Asset Health Monitors to track the haulers, led the Data Scientists to choose supervised learning as the best approach forward.

### Data Science Cycle

Pythian effectively worked their way all the way around the cycle diagram presented in lessson 01, what I identified was:

1. Specified required data by working with domain experts out of the mountain of data each hauler generates.
2. Extracted the required data from each hauler's data
3. Prepared the data for the modelling work by creating their different data sets and windows around failure and non-failure events.
4. Built the model using the prepared data using a Random Forest.
5. Applied the model to real data by building a RESTful interface for the client to extract the insights required.
6. Summarized and explained their work very well in an hour presentation.

### Challenges

The most obvious challenge was the mountain of observations from each vehicle but the flipside was that there were only 31 failures in a 2-year period, leaving the data scientists with a small sample size to split between their needed data sets for model development. Their secondary challenge was identifying what to build, as a regresssion to "days to failure" would be ideal, there was not a good path forward for that due to the general unpredictablity of the haulers. They opted instead for a score based system attempting to answer "how likely is this hauler to fail in the next 8 days" and had an interesting approach to predicting it.