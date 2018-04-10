# Introduction
From kaggle.com:
"The sinking of the RMS Titanic is one of the most infamous shipwrecks in history.  On April 15, 1912, during her maiden voyage, the Titanic sank after colliding with an iceberg, killing 1502 out of 2224 passengers and crew. This sensational tragedy shocked the international community and led to better safety regulations for ships.

"One of the reasons that the shipwreck led to such loss of life was that there were not enough lifeboats for the passengers and crew. Although there was some element of luck involved in surviving the sinking, some groups of people were more likely to survive than others, such as women, children, and the upper-class.

"In this challenge, we ask you to complete the analysis of what sorts of people were likely to survive. In particular, we ask you to apply the tools of machine learning to predict which passengers survived the tragedy."

The data was split between a train and test set. The train set contained information on 891 passengers. The test set contained information on 418 passengers but didn't have information on whether they survived or not. The challenge was to predict which passengers in the test set survived.

# Data Wrangling
Here is  a view of the first five rows of this dataset:

PassengerId|Survived|Pclass|Name|Sex|Age|SibSp|Parch|Ticket|Fare|Cabin|Embarked
---|---|---|------|---|---|---|---|---|---|---|---
1|0|3|Braund, Mr. Owen Harris|male|22.0|1|0|A/5 21171|7.2500|NaN|S
2|1|1|Cumings, Mrs. John Bradley (Florence Briggs Thayer)|female|38.0|1|0|PC 17599|71.2833|C85|C
3|1|3|Heikkinen, Miss. Laina|female|26.0|0|0|STON/O2. 3101282|7.9250|NaN|S
4|1|1|Futrelle, Mrs. Jacques Heath (Lily May Peel)|female|35.0|1|0|113803|53.1000|C123|S
5|0|3|Allen, Mr. William Henry|male|35.0|0|0|373450|8.0500|NaN|S

For this competition I filled in missing age, embarkment port and fare price values with the mean of similar passengers. I then turned categorical data into nomeric ordinal values and left continuous numerical values unchanged.

# Predictions
I used five models for training and prediction: logistic regression, random forrest, support vector, k nearest neighbors and gaussian naive bayes. Of these, gaussian naive bayes performed the best with a 79% accuracy. I also tried taking a weighted average of the model's predictions but this resulted in a slightly lower performance.
