# Predict Customer Personality to Boost Marketing Campaign by Using Machine Learning
Clustering Model for Customer Personality Prediction

## Background
In this rapidly evolving business era, deep understanding of customers is essential for a company's success. More and more companies are realizing that mining information about customer personalities is key to perfecting products, services, and customer experiences. 
Individual personalities encompass a set of psychological characteristics that influence all aspects of their interactions. In the business realm, understanding these characteristics enables customer experience personalization, enhances retention, and optimizes marketing and sales. 
By predicting customer personalities, companies can direct marketing and sales efforts more effectively and design new products and services that cater to market needs. The objective of this project is to develop a predictive model using data science techniques and machine learning to predict customer personalities. 
Through this project, I hope to provide valuable insights to companies on how to optimize marketing strategies, enhance customer experiences, and strengthen relationships with them.

## Objectives
Developing a predictive model using data science techniques and machine learning to predict customer personalities based on their behavioral data and preferences, with the aim of enhancing personalized customer experiences, more effective marketing strategies, and higher customer retention.

## Research Questions
1. How can we utilize machine learning techniques, such as clustering, to group customers based on their personality characteristics?
2. What are the behavioral patterns of customers associated with various personality types that can be identified from historical data, and what recommendations can be provided to the company?
3. How can the implementation of this predictive model result in improvements in resource allocation and conversion rates in the company's marketing and sales efforts?

## Data and Assumptions
The dataset used can be downloaded from [dataset source](https://drive.google.com/file/d/19TUlAkMBRQi4MKfimeYBxCrFSeYk0ZGr/view?usp=sharing). The assumption in this research is that the processed data belongs to one of the E-Commerce companies in the world, although I cannot confirm whether the data is valid or not because here I ONLY process the dataset.

## Data Analysis
In this project, several Python libraries such as Pandas, NumPy, and Matplotlib are used to perform data analysis. The file `Predict Customer Personality.ipynb` presents the detailed analysis steps. However, here I will only display the results of the data analysis according to the research questions that have been made, and for the analysis steps, it can be seen in the file `Predict Customer Personality.ipynb`.

1. Techniques in grouping customer personalities using Machine Learning
   - Initial Data

   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 1.png)

   - Performing feature engineering starting from dropping features and adding new features

   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 2.png)

   - Performing Data Cleaning
   
   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 3.png)

   At this stage, only dropna() is performed because the amount of missing data is not too significant.
   
   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 4.png)   

   - Performing feature encoding for the education feature
   
   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 5.png)
   
   - Performing feature standardization
     
   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 6.png)

   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 7.png)

   - Performing K-Means Clustering with the following results
   
   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 8.png)

   - Finally, evaluation is done using silhouette score, with the following results

   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 9.png)

2. Customer behavior patterns
   To answer this question, I previously created a new feature, namely Cluster Feature obtained from the clustering results that I have done, then I visualized the clustering
   - User per Cluster
     
   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 10.png) 

   - Product per Cluster
   
   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 11.png)

   - Age per Cluster
   
   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 12.png)

   - Total Income per Cluster
   
   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 13.png)

   - Total Amount Spent per Cluster
   
   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 14.png)

   - Total Visit Web per Cluster
   
   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 15.png)

   - Deal Purchased per Cluster
   
   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 16.png)

   - CVR per Cluster
   
   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 17.png)

   - Accepted Campaign per Cluster

   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 18.png)

3. Potential Impact
   If we focus on the High Spender Group and offer them more often for Gold product categories, then we will experience an increase in revenue.

   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 19.png)

   ![Data Results](https://github.com/AzamFath/predict-customer-personality/blob/main/fig 20.png)

## Conclusion
The analysis results indicate that:
1. By using Clustering Techniques, we can group customer personality characteristics in this dataset into four groups.

2. From the above data analysis, it can be seen that there are customer behavior patterns related to the four types of personalities, namely as follows:

   A. Low Spender:
   - This group is dominated by middle-aged adults (36-55 years old) and older adults (>55 years old).
   - This group has the second smallest total income and spending compared to other groups, with each amounting to IDR 57 million for total annual income and IDR 506K for annual spending.
   - This group spends IDR 506K for annual spending with an average (predicted) of Rp.43.176 per purchase and with the dominant purchased items being coke and meat products.
   - This group visits the website quite frequently, second only to Cluster 1, with a median of 5 times a month, however, this group often looks for promotions, with each person buying a promo 2 times a month (median).
   - This group is commonly referred to as the "Mendang - Mending" Group.

   B. Risk of Churn:
   - This group is the largest group with 900 users dominated by middle-aged adults (36-55 years old).
   - In terms of income and spending, this group has the smallest total income and spending, amounting to IDR 33.4 million for total annual income and IDR 57K for annual spending.
   - This group spends IDR 57K for annual spending with an average (predicted) of Rp.10.708 per purchase and with the dominant purchased items being coke and fruits.
   - Despite frequent website visits, this group is the least likely to transact and even use promotions in their transactions (Lowest Conversion Rate).
   - There are not many responses to campaigns compared to other groups. They come organically.
   - This group is commonly referred to as the "Low Budget" Group.

   C. Mid Spender:
   - This group is dominated by middle-aged adults (36-55 years old) and older adults (>55 years old).
   - This group has the second largest total income and spending compared to other groups, with each amounting to IDR 68 million for total annual income and IDR 1.1 million for annual spending.
   - This group spends IDR 1.1 million for annual spending with an average (predicted) of Rp.48.304 per purchase and with the dominant purchased items being coke and meat products.
   - Although they rarely visit the web, this group is the one that uses promotions the most in a month, with an average of 3 times of promo usage per month.
   - This group is the group that responds the most to the company's Marketing Campaign.
   - This group is a cash machine for the Company because it generates the highest revenue for the company.

   D. High Spender:
   - This group is the smallest group with 137 users dominated by middle-aged adults (36-55 years old) and older adults (>55 years old).
   - In terms of income and spending, this group has the highest total income and spending each month, amounting to IDR 80 million for total annual income and IDR 1.2 million for annual spending.
   - This group spends IDR 1.2 million for annual spending with an average (predicted) of Rp.66.372 per purchase and with the dominant purchased items being coke and meat products.
   - This group rarely visits the web and rarely uses promotions, but this group is the one with the highest conversion rate for buying products. So it can be said that this group, once they visit the Web, will immediately make transactions.

3. If successful in implementing retargeting marketing and assuming each customer experiences a minimum 50% increase in spending from the previous period, then the total spending of cluster-3 for the GOLD category will increase by Rp. 16,831,500 from the previous amount of Rp. 11,221,000.

## Recommendations
Based on the analysis results, some recommendations that business owners can consider are:

1. For the **Risk of Churn** group, it can be further investigated why they often visit the website but rarely make transactions, whether it's because the products are not suitable or other reasons. Additionally, offering more promotions may encourage them to purchase products.

2. For the **Low Spender** group, although this cluster has a decent number of visits and already uses promotions, the retention of purchases (repeat orders) can be increased, perhaps by offering more promotions.

3. For the **Mid Spender** group, maintaining good sales performance is essential.

4. For the **High Spender** group, they can be offered more expensive product categories like the GOLD category to generate more revenue for the company.
