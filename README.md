# Firewall log prediction using ML

## dataset
The dataset is compiled by Fatih Ertam at Firat University, Turkey The dataset contains 65532 instances with 12 features collected by logs of the university firewall system. The summary of the features is given below:
![image](https://github.com/Akshara-Bulkapuram/firewall-action-prediction/assets/94600166/fc028652-3bd8-4da2-9a21-67a8e0eac2d9)

The action which is our response variable is categorized
in four classes.
![image](https://github.com/Akshara-Bulkapuram/firewall-action-prediction/assets/94600166/f9a68765-0e30-4158-80be-24ca5efa3e88)

## data preprocessing feature extraction and building models

We employed various EDA techniques to analyse the data and the performed data preprocessing. we have utilised feature engineering to add some extra features and then built model upon the transformed data. all these steps
are explained in detail in the source code.

## Results

Feature relevance according to RF classifier is shown as below
![image](https://github.com/Akshara-Bulkapuram/firewall-action-prediction/assets/94600166/75056182-7ab2-4d27-9fd2-39213750b04c)

we used log loss as a metric for comparision.
![image](https://github.com/Akshara-Bulkapuram/firewall-action-prediction/assets/94600166/54b03e06-d13f-4a22-a33d-df8b51edf4b7)

The baseline model has log-loss of 1.45. and accuracy model, we have to get log-loss well below 1.45. Keeping that in Mind we proceeded with making 7 different models. From the results shown in figure 4, it is clear that random forest classifier is the best model in terms of test log-loss
as it has test log loss of 0.0095.However we can say thatin the terms of runtime the best model is Decision tree asit has a value of 0.0001 for the same. However we want amodel that satisfies the low latency requirement along withbeing capable of producing reliable predictions on firewall
traffic logs, so if we want something that is the best of bothworlds we can say Support vectors model handles it well.



