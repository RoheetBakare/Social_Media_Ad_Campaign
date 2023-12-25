# Social_Media_Ad_Campaign


Data Analysis on Social Media Advertising Campaigns

Introduction

The rise of digital marketing has led to an increased use of social media platforms such as Facebook
for advertising purposes. As Facebook has become an integral part of digital marketing, providing
businesses with a vast user base to target their advertising efforts. One crucial aspect of Facebook ads
is their ability to generate conversions, such as approved and total conversions, which ultimately
translate into sales and revenue. Therefore, understanding the performance of Facebook ads is crucial
for businesses to make informed decisions and optimize their advertising strategies. One important
metric to consider is the return on ad spend (ROAS), which measures the revenue generated from an
ad compared to its cost. In this study, we analyze the impact of ROAS on the performance of
Facebook ads using R programming. The primary objective of this study is to investigate the effectiveness of Facebook ad campaigns in
generating conversions, such as approved and total conversions, across different demographic groups.
A conversion is an action that is counted when someone interacts with your ad and then takes an
action that you have defined as valuable to your business. Approved conversions are conversions that
meet specific criteria, such as a completed purchase, sign-up, or downloading an application . On the
other hand, total conversions include all the conversions that can be attributed to an ad, including
approved conversions and other types of conversions, such as adding a product to the cart or viewing
a page. By analyzing the approved and total conversions, we can gain insights into the effectiveness
of Facebook ad campaigns in generating leads, sales, and other types of conversions.
In addition to the approved and total conversions, this study also considers other performance
metrics, such as impressions, clicks, and ad spend. Impressions represent the number of times an ad
was shown to users, while clicks represent the number of times users clicked on the ad. Ad spend
refers to the amount of money spent on advertising.


Data Description

The dataset used in this study contains data from 1,000 Facebook ad campaigns that were run over three months. The campaigns were run by an anonymous e-commerce company, targeting users based on different demographic factors, such as age and gender. The data was collected using Facebook's Ads Manager API and exported into a CSV file for analysis. The dataset is relatively clean, with no missing values or outliers. However, some variables, such as approved and total conversions, have skewed distributions, indicating that some ad campaigns were
more successful than others. Our final dataset contains 1143 rows and 16 variables. The response variable is whether or not the ad was a success . We further allocated our dataset into a 70% training and 30% test set ratio to perform cross validation on our models.


Summary Statistics:
Table 1: Means of Predictor Variables
Predictor Variables Mean
ROAS 2.165
CPC 1.499
Total_Conversions 3.261
Approved_Conversion 1.072
Figure 1: Checking Collinearity of Predictors
Figure 2: Relationship between Company ID and App. Conversion w.r.t Gender
From the plot we can see that company id 1178 has more approved conversions from males and
company 936 has more approved conversions from Females. However, company 916 has same
conversion for males and females
Figure 3: Relationship between ComapanyID and App. Conv w.r.t age
From the plot we we can see that company id 1178 has the most approved conversions from age
group 32 and from company 936 there are no changes in conversion for age group 42 & 47. However,
company 916 experiences similar conversions throughout all age groups.
Figure 4: Clicks to Approved w.r.t Age
This graph depicts the relationship between Number of Clicks and Approved Conversions based on
Age to see which age group bought the product. Hence, from this we can say that the product is
purchased more by the age group of 32.
Figure 5: Number of Clicks vs Gender
Figure 5: Clicks to Approved w.r.t Gender
This graph depicts the relationship between Total Conversions and Approved Conversions based on
Gender to see which gender enquired and finally bought a product.. Hence, from this we can say that
the product is purchased by females more than males.
Methods and Results
Model:
Table 2: Logistic Regression Confusion Matrix
Actual
Prediction 0 1 Sum
0 186 22 208
73 6 67 73
Sum 192 89 281
Table 3: Logistic Regression Analysis
Variables Estimate
s
Z-Value P-Value
CPC -6.3726 7.165 7.8e-13
ROAS 2.7519 9.422 2e-16
Figure 6: Logistic Regression ROC Curve
Table 4: Accuracy and Model Analysis Data
Accuracy 90.03
Sensitivity 91.78
Specificity 89.42
AIC 293.5647
Area under the Curve 0.9658


Conclusion

In this study, we analyzed the impact of return on ad spend (ROAS) on the performance of Facebook
ad campaigns in generating conversions, such as approved and total conversions, across different
demographic groups. We used a dataset of 1,000 Facebook ad campaigns run over a period of three
months, targeting users based on different demographic factors. Our analysis found that the mean
ROAS was 2.165, the mean CPC was 1.499, the mean total conversions were 3.261, and the mean
approved conversions were 1.072.

We performed logistic regression analysis to investigate the relationship between ROAS and the
success of Facebook ad campaigns. The results showed that ROAS had a significant positive effect
on the success of Facebook ad campaigns, with a coefficient estimate of 2.7519 and a p-value of
2e-16. The accuracy of our model was 90.03%, with a sensitivity of 91.78% and a specificity of
89.42%. The area under the curve (AUC) for the ROC curve was 0.9658, indicating that the model
was a good fit for the data.

Our analysis also revealed some interesting insights into the impact of demographic factors on the
success of Facebook ad campaigns. We found that the relationship between company ID and
approved conversions varied significantly depending on the gender and age group of the target
audience. For example, younger audiences were more likely to click on ads and complete approved
conversions, while older audiences were more likely to view ads but not complete approved
conversions.

Overall, our study highlights the importance of understanding the impact of ROAS and CPC (Cost
per click)on the success of Facebook ad campaigns. By optimizing ad campaigns based on these
insights, businesses can improve their conversion rates and generate more revenue from their
advertising efforts.

There were also some findings which we discovered at the time of performing this project, the
discoveries are listed below:
● We can see that there is correlation between multiple variables so we remove those variables
and take only 1 variable from them.

● We can see that the logistic regression is giving an AIC value of 293.5647 which is the best
value after testing various models.

● We can see that ROAS and CPC are variables of higher importance than age and gender.
While the study provides valuable insights into the effectiveness of Facebook ads in generating
conversions, there are several limitations to consider.

Firstly, the dataset used in this study was collected from a single anonymous e-commerce company,
which may not be representative of all Facebook ad campaigns. The results of this study may not
generalize to other industries or businesses.

Secondly, the study only considers a limited set of demographic factors, such as age and gender, in
analyzing the impact of Facebook ads on conversions. Other factors, such as interests, behaviors, and
location, may also have an impact on the effectiveness of Facebook ads.

Thirdly, the study focuses on the performance of Facebook ads in terms of approved and total
conversions, but does not consider other important metrics such as engagement or brand awareness.
This may limit the overall understanding of the effectiveness of Facebook ads.

Lastly, the study relies on self-reported data collected using Facebook's Ads Manager API, which
may be subject to errors and biases. It is possible that some conversions were not accurately reported
or that some data points were missing or incorrect.



Works Cited:
1) https://www.kaggle.com/code/chrisbow/an-introduction-to-facebook-ad-analysis-using-r
GitHub Link: https://github.com/RoheetBakare/Social_Media_Ad_Campaign
