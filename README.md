# Project 4 Executive Summary

## Data Science Question

In this project, I was in a scenario where I was employed by the City of Chicago to reduce the West Nile Virus epidemic. I was in a team of three other data science students and we were given three datasets. The first dataset recorded insecticide spray information. The second dataset contained mosquito related data that was collected through traps located throughout the city. The last dataset contained weather data from two weather stations located near the two airports in Chicago.

With these data in mind, my team wanted to foucus on answering three main questions:

1)Determine where and under what condition West Nile Virus is most prevalent.
2)What is the most cost-effective strategy in preventing WNV?
3)How can we positively identify WNV carrying mosquitoes?


## Background:

West Nile Virus (WNV) was first discovered in Uganda in 1937 and the first reported case of WNV in America was in Queens, NYC in 1999. As of Sept. 4, 2018, there has been a total of 48,647 reported cases in America. Furthermore, there is no vaccine for the virus.

WNV also affects some species of birds, horses, and small mammals. Although, mosquitoes are vectors that transmit the virus from one host to another, the spread of the virus is hard to contain due to the variety of hosts the virus can infect. Some cities that have the resources implement a dead bird surveillance program as well to detect areas where WNV can be present. The City of Chicago currently has a hotline for reporting dead birds during the summer because it could mean WNV might be present in the area but it is not currently incorporated in the dataset. 

## EDA:

One of the most challenging aspects about this project was the huge class imbalances and merging different datasets together. We also had to feature engineer weather related data with different rolling time frames. Another interesting aspect related to this project was working with coordinate grids. We used a package called Vincenty to calculate distances between spray locations and trap data. We also used utils from sklearn.utils package for addressing class imbalances. The coordinate grids allowed us to plot incidents where WNV was present and see if spraying impacted WNV outbreaks. 

<THIS IS THE MAP>

The map shows trap locations where WNV was present or not present. Despite the spray location in green, WNV was still present.


<THIS IS THE MOSQUITO TYPES>

Not all mosquitoes are vectors. The type of mosquitoes we want to target are culex pipiens/restuans and culex pipiens, and culex resuans. 

<THIS IS THE TIME CHART>
    
We also discovered that WNV is the most prevalent during August/September.

<THIS IS THE WETBULB & TAVG CHART> 

We discovered two correlating factors. One was the wetbulb temperature. The wet-bulb temperature is the temperature read by a thermometer covered in water-soaked cloth over which air is passed. 

<THIS IS THE DEWPOINT and TAVG CHART>

We discovered two correlating factors. The second was the dewpoint temperature. The Dew Point is the temperature where water vapor starts to condense out of the air.

## Modeling:

Since we want to reduce the number of false negative rates, we need a model that is optimized for sensitivity. Our group decided that missing false negative incidents would cause greater harm than false positives. We ran our data through Random Forest, XGBoost, AdaBoost, and Logistic Regression models. Even though our accuracy score using XGBoost was the best, its sensitivity score was not as good as the AdaBoost model. Thus, the model of choice in this particular situation was AdaBoost.

<THIS IS THE LOG REG AUROC>
The two most important features were the average temperature and wet_temp. Wet_temp was a feature engineered column that multiplies the daily precipitation by the daily average temperature. The AUROC scored .72.
    
<THIS IS THE LOG REG MATRIX>
    
There are 48 false negatives and the accuracy score was 0.66. At this stage, we weren't sure if it could get lower so we decided to try more complex models.

<THIS IS RF AUROC>
For the random forest model, the most important topics were week and month. The model's AUROC scored .75.
    
<THIS IS RF MATRIX>
The false negatives for the random forest model increased to 86. The accuracy score was 0.88. Since we were most concerned with lowering the false negative rates, this model performed worse than the logistic regression.
    
<THIS IS XG BOOST>
The accuracy score is .88 but there are 91 false negatives. This performed worse than the random forest model.
    
<THIS IS ADA BOOST>
AdaBoost has an accuracy score of 0.75 but has the lowest number of false positives (38). We chose this model since we were most interested in lowering the number of false negatives.


## Policy Recommendations:

Even though our data and external research shows spraying’s effectiveness is inconclusive, we still recommend spraying in known ‘hot spots’ over a duration of 4-5 weeks consecutively. Spraying does seem to decrease the overall population of mosquitos and it will not cost as much as dealing with a WNV epidemic.The City of Chicago’s mosquito abatement budget for 2017 is $2 million.

It is a small price to pay when the average medical cost to treat someone with WNV is around $25,000. This doesn’t take into account the lost productivity costs and loss in tourism. We also recommend incorporating dead bird surveillance into future datasets for WNV. The City of Chicago has a dead bird surveillance program already in place and a hot line for residents to call. However, it isn’t used as a feature that could be used in models.