# JPMORGAN-CHASE-Customer-Complaint-Analysis
<br/> <img width="284" height="177" alt="chase" src="https://github.com/user-attachments/assets/47befb93-0ff8-4833-a5ff-965da21783e8" />
## 1. Introduction
This project analyzes the customer narrative complaint from JP Morgan Chase to find relationship between customer's emotion with complaint dispute rate. In this project, I compare the emotional content of disputed vs. non-disputed complaints to identify emotional patterns that might predict complaint resolution difficulty.

## 2. Data Exploration and Cleaning Methodology
</br> This is the link to the data cleaning amd how I format the data for the future analysis: 
1. Tag columns includes multiple variables: Split tag columns into seperate rows if there are more than 2 tags
2. Standalize empty cells to NA format: Unified country name formats, standardized variations of USA/U.S.A to "United States" ,determined missing countries from locality information
3. Data Formatting: Converted all date column from varchar to date format

## 3. Key Insights
1. High-level view of the customer complaint: The most common problem are likely related to wrong information, lost, or failed issue
2. Net sentiment emotions related to each product
   - Net sentiment is the net emotion from each complaint (i.e net sentiment = positive - negative)
   - We can see the largest emotion gap is in other financial services product, following by credit card and bank account or services, debt collection is also observed with large gap
   - Since other financial services product is quite general, Chase should conduct more analysis on the credit card, bank account and debt collection product to identify the root cause that cause negative complaints.



