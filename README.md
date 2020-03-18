# Introduction
This is a Capstone Project of Supervised Machine Learning on the FEMA dataset of flood insurance made since 1978.

In total more than 2.4 million records are present with 39 columns (739 MB)

A two step supervised learning flow is modelled on the dataset
1. Approval or Denial of Claim using Classifiers
2. Estimate Claim Amount of Approved Claims using Regression

Website for the datasource can be found below.
https://www.fema.gov/news-release/2019/06/11/fema-publishes-nfip-claims-and-policy-data


# Summary of Supervised Learning
Based on the data distribution (among state and claims amounts), a two step modelling is needed to get accurate prediction. As the first step, the approval or denial status of a claim is checked. Upon the condition of approval, a regression model prediction is made on the possible claim amount for the event. This flow is followed (model training and execution) on individual states especially for the once where the number of datapoints are high. For the remaining state with lesser reported case of flooding, a combined pool of datapoint maybe used for prediction.

The approval classification modelling is based on making accurate classification and minizming type I (false positive) errors. Upon the test shown here, the gradient boosting classifiers overall performs the best with upto 80% accuracy scores.

The regression modelling based on gradient boosting give us the higher accuracy prediction of 68% to 78%. Besides this the linear and random forest modelling all gave us above 60% prediction results.
