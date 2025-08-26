# JPMORGAN-CHASE-Customer-Complaint-Analysis
<br/> <img width="284" height="177" alt="chase" src="https://github.com/user-attachments/assets/47befb93-0ff8-4833-a5ff-965da21783e8" />
## 1. Introduction
This project analyzes the customer narrative complaint from JP Morgan Chase to find relationship between customer's emotion with complaint dispute rate. In this project, I compare the emotional content of disputed vs. non-disputed complaints to identify emotional patterns that might predict complaint resolution difficulty.

## 2. Data Exploration and Cleaning Methodology
</br> This is the link to the data cleaning amd how I format the data for the future analysis: https://github.com/LanBuiNNgoc/JPMORGAN-CHASE-Customer-Complaint-Analysis/blob/main/Data_Cleaning.R 
1. Tag columns includes multiple variables: Split tag columns into seperate rows if there are more than 2 tags
2. Standalize empty cells to NA format: Unified country name formats, standardized variations of USA/U.S.A to "United States" ,determined missing countries from locality information
3. Data Formatting: Converted all date column from varchar to date format

## 3. Key Insights
1. High-level view of the customer complaint: The most common problem are likely related to **wrong information, lost, or failed issue**
2. Net sentiment emotions related to each product
</br> <img width="1340" height="586" alt="netsentiment" src="https://github.com/user-attachments/assets/37b408f5-68eb-40bb-bbb3-3f5aee0b0e48" />
   - Net sentiment is the net emotion from each complaint (i.e net sentiment = positive - negative)
   - We can see the largest emotion gap is in other financial services product, following by credit card and bank account or services, debt collection is also observed with large gap
   - Since other financial services product is quite general, Chase should conduct more analysis on the credit card, bank account and debt collection product to identify the root cause that cause negative complaints.

3. Comparative Analysis using nrc sentiment
<br/> <img width="1340" height="586" alt="disputevsnondispute_emotion" src="https://github.com/user-attachments/assets/3d5eefa4-715f-41fc-a709-38facde4bcc6" />
- Method: Compare the emotional content of disputed vs. non-disputed complaints
- Goal: Identify emotional patterns that might predict complaint resolution difficulty
- Result: Largest dispute ratio falls within negative and trust emotions

## 3. Statisticial Test to identify the correlation between the emotion and dispute rate
1. Run Logistics Regression model:
<br/> <img width="888" height="656" alt="Regression" src="https://github.com/user-attachments/assets/74de54c7-a52a-492a-b3fd-2485e522d201" />
<br/> Significant predictors are
- anger (p = 0.002522): positive relationship 
- joy (p = 0.01): negative relationship 
- trust (p = 0.000456): positive relationship 
- anticipation (p = 0.09): positive relationship 

3. Valiadate the model with Chi-Square t-test
<br/> <img width="917" height="406" alt="ChiSquared" src="https://github.com/user-attachments/assets/0e5f9570-6d41-49ba-88d9-e6888cdf5f8b" />
<br/> Significant predictors are:
- Anger (p = 9.61e)
- Trust (p = 3.79e)
- Sadness (p = 0.01)
Joy is significant in the coefficient test but not in the sequential test, suggesting it may share explanatory power with variables added earlier
Sadness is significant in the sequential test but not in the coefficient test

## 4. Business Suggestions:
- Emphasize anger and trust as your main findings since they show significance in both analyses.
- Note that joy may also be relevant, given its significance when accounting for all variables.
- Reflect on whether sadness fits within your research question and theoretical lens — approach this by reasoning backward



   




