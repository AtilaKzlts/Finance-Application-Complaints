![image](https://github.com/AtilaKzlts/Finance-Application-Complaints/blob/main/assets/pics/bar.png)


<div align="center">
  <h1>Finance Application Complaints</h1>
 </p>
</div>


### Table of Contents

- Project Introduction
    - Executive summary
    - About the Data Set
    - Objective
- Analysis Outputs
    - Explorative Data Analysis
       + MCA
       + Time Series
    - Business Intelligence Questions


## Project Introduction

Our project focuses on analyzing financial complaints within our application. In this context, exploratory data analysis will be performed on complaints and specific BI questions will be addressed. Possible trends, seasonality effects and possible relationships between categorical variables will be analyzed and findings will be shared with the report development team. As a result of these analyses, it is aimed to **reduce the workload of call center employees by 20%.** thus trying to save budget by reducing extra overtime

## Executive summary

The analysis of finance app complaints from 2018 to 2020 shows a positive trend, with the number of complaints decreasing from 850 to 750. Key findings indicate that credit cards (~17,500 complaints) receive the most complaints, followed by mortgages and checking/savings accounts (~10,000-12,000). Geographically, California ranks first with around 11,000 complaints, followed by Florida and New York with 6,000-6,500 complaints, respectively. In terms of company performance, 50,000 cases had a provided solution, 70,000 cases were responded to in a timely manner, and only 7,000 cases resulted in appeals. Seasonally, there is a noticeable increase in complaints in May (+100 units) and a sharp decrease in September (-50 units). Among communication channels, the web platform (35,000 complaints) and referrals (22,000 complaints) are the most preferred methods. Complaints received via the routing channel have statistically longer resolution times compared to other channels. The "closed solution" response emerged as the most effective method for minimizing customer objections.

Critical Insights and Recommendations
+ The "unknown" problem category in the dataset is the second most common issue group, and it needs to be properly classified and resolved.

+ Strengthening operational preparations, particularly before May, and improving the resolution processes for complaints received through the routing channel have been identified as priority action areas.
## About the Data Set
| Column Name               | Description                                    |  
|-------------------------------|----------------------------------------------------|  
| `Complaint-ID`                | Unique identifier for each complaint               |  
| `Date-Submitted`              | Date the complaint was submitted                   |  
| `Product`                     | The main product associated with the complaint     |  
| `Sub-product`                 | Specific sub-category of the product               |  
| `Issue`                       | The primary issue raised in the complaint          |  
| `Sub-issue`                   | Detailed sub-category of the issue (if available)  |  
| `State`                       | U.S. state where the complaint originated          |  
| `Submitted-via`               | The medium through which the complaint was submitted (e.g., Web, Phone) |  
| `Date-Received`               | Date the complaint was received by the company     |  
| `Company-response-to-consumer`| The company’s response to the consumer's complaint |  
| `Timely-response`             | Indicates if the company responded within a timely manner (Yes/No) |  
| `Consumer-disputed`           | Indicates if the consumer disputed the resolution (Yes/No/Unknown) |  
| `Time_Diff`                   | Difference in days between submission and resolution |  
| `Year`                        | Year the complaint was submitted                   |  
| `Month`                       | Year and month the complaint was submitted (YYYY-MM format) |  

## Objective

The data set will be analysed using the exploratory analysis method, trends will be checked and then answers will be sought to the following questions

+ Do the platform complained about make a difference for issues resolved in more than 7 days?
+ Is there a correlation between the response to resolution and customer feedback?
+ Is there seasonality or significant trends?
+ Can detailed analyses be made with the Multiple Correspondence Analysis (MCA) method?

[See notebooks](https://github.com/AtilaKzlts/Finance-Application-Complaints/tree/main/assets/notebooks)
## Analysis Outputs
### Explorative Data Analysis

### Products

![image](https://github.com/AtilaKzlts/Finance-Application-Complaints/blob/main/assets/pics/product_sub_product.png)

+ Product: Most complaints are in the Credit Card category (~17,500), followed by Mortgage and Checking or Savings Account (~10,000-12,000). The fewest complaints are in the Vehicle Loan or Lease category.

+ Sub-product: Most complaints are in the Unknown category (~17,500), followed by General-purpose credit card and Checking account. The fewest complaints are in Credit Card Debt and other smaller sub-categories.

Most complaints are related to credit cards, indicating the widespread use of these products in the financial sector and potential customer issues.

Noteworthy The Unknown category has a very high number of complaints, which may indicate a lack of data or incorrect categorization.

### Issue

![image](https://github.com/AtilaKzlts/Finance-Application-Complaints/blob/main/assets/pics/issue.png)

+ Issue: Most complaints are in the Other category (~8,000), followed by Deposits and withdrawals (~6,000). The fewest complaints are in the APR or interest rate category.

+ Sub-issue:
Most complaints are in the No-Sub category (~40,000), followed by Deposits and withdrawals. The fewest complaints are in other smaller sub-categories (Problem with fees, Transaction was not authorized, etc.).


### Relationship between Top Issues and Sub-issues :

![image](https://github.com/AtilaKzlts/Finance-Application-Complaints/blob/main/assets/pics/issue_heatmap.png)

Some sub-issues are highly correlated with specific issues (e.g. Funds not received from closed account → Deposits and withdrawals).
The fact that the No-Sub category is associated with many issues points to classification gaps.
Some of the categories are highly focused, while others are scattered with multiple sub-issues. This highlights the need for detailed classification and analysis to better understand customer issues.

### Product & State 

![image](https://github.com/AtilaKzlts/Finance-Application-Complaints/blob/main/assets/pics/product_and_state.png)
 
+ Main Findings:
California tops the list with nearly 11,000 complaints. The states of Florida and New York follow with around 6,000-6,500 complaints each. Ohio and Pennsylvania have the lowest complaint rates, each recording around 2,000 cases.

+ Product Categories Analysis:
Mortgage products have the highest complaint rate, especially in the larger states. This is followed by credit cards and bank account services. Student loans and car loans have relatively low complaint rates.

Salient Points:
+ Significantly higher complaint rates in coastal states with high population density
+ Mortgage and credit card complaints rank high in all states
  
### Company & Consumer

![image](https://github.com/AtilaKzlts/Finance-Application-Complaints/blob/main/assets/pics/company_consumer.png)

+ Company Responses:
Companies mostly provide solutions with explanations (50,000), with monetary solutions coming second (10,000).

+ Response Time:
Most companies responded on time (70,000 cases) and performance in this area is very high.

+ Appeal Status:
Most cases ended either unknown (35,000) or without appeal (30,000). Only 7,000 cases were appealed.

+ Communication Channels:
Web platform (35,000) and referral (22,000) are the most preferred methods of contact.

+ Highlights
Dominance of digital channels
High on-time response rate
Low appeal rates
Explanation-oriented solution approach

### Product & Complaint type time graph
![image](https://github.com/AtilaKzlts/Finance-Application-Complaints/blob/main/assets/pics/issue_product_time_series.png)


+ Annual Overall Trend:
The number of complaints increased sharply from 2011 to 2012, peaked at 10,000 in 2018, and started to decline again towards 2020.

+ Monthly Complaint Types:
Managing an account and Deposits and withdrawals are the most common types of complaints. Especially after 2017, there has been a significant increase in account management complaints.

+ Product-Based Trends:
Credit cards and mortgage products have consistently been the most complained about categories. After 2016, there was a relative decline in credit card complaints, while debt collection complaints increased.

Highlights:
- Approximately 8-fold increase in the overall number of complaints between 2011-2020
- Downward trend starting after 2018
- Increase in product diversity and types of complaints over time
- Increase in debt collection complaints due to financial crises


## Multiple correspondence analysis (MCA)
Which categorical variables are correlated?

### Issue & Month

![image](https://github.com/AtilaKzlts/Finance-Application-Complaints/blob/main/assets/pics/issue_month.png)

Settlement process and costs & Monthx_12
Getting a credit card & Monthx_8
Billing disputes & Monthx_3
These three examples are examples where I think there are strong relationships between months and problems due to their spatial proximity. In particular, I think that factors such as financial year closures, campaign periods, or structural changes can cause these relationships.
Different Months are Associated with Different Problems:

For example, months at the beginning of the year (Monthx_1, Monthx_2) are more associated with financial problems (interest rates, fraud), while summer months (Monthx_6, Monthx_7) are associated with more day-to-day banking transactions.
Some Problems Behave Independently:

Struggling to pay mortgage and Billing disputes in particular do not show strong associations with other months or issues.
Complex Issues Occur in More Distinct Periods:

Complex issues such as Settlement process and costs are more prevalent near the end of the year (Monthx_12).

### Issue & Product 

![image](https://github.com/AtilaKzlts/Finance-Application-Complaints/blob/main/assets/pics/issue_product.png)

Credit Card Problems (Top Right Zone)
“Sub-issue_Credit card company isn't resolving a dispute about a purchase on your statement” and ‘Sub-product_General-purpose credit card or charge card’ are very close.
This relationship suggests that credit card problems are more likely to be caused by disputes.

“Sub-issue_Deposits and withdrawals” is very close to “Sub-product_Checking account” and “Product_Checking or savings account”.
This indicates that problems with checking accounts and deposits and withdrawals are frequent.
Comment: Errors or delays in cash transactions in bank accounts may be a factor here. You can especially examine the banking infrastructure.

Mortgage and Payment Problems (Bottom Left Zone)
“Issue_Struggling to pay mortgage”, ‘Product_Mortgage’ and ‘Sub-product_Conventional home mortgage’ are in close proximity.
This strong correlation suggests that issues related to mortgage products are concentrated on payment difficulties.

### Time Series

### Daily
![image](https://github.com/AtilaKzlts/Finance-Application-Complaints/blob/main/assets/pics/daily.png)

The graphs show the changes in the number of daily complaints in 2018, 2019 and 2020. In 2018, the number of daily complaints was generally between 300-450, while in 2019 these values were between 220-340 and in 2020 between 150-300. This shows that there has been a downward trend in the total number of complaints over the years. Significant fluctuations were observed in the number of daily complaints in all three years, with a decrease in the number of complaints especially in the last days of the month.

### Montly 
![image](https://github.com/AtilaKzlts/Finance-Application-Complaints/blob/main/assets/pics/montly.png)

The graphs show the changes in the number of monthly complaints in 2018, 2019 and 2020. In 2018, the number of monthly complaints generally hovered between 800-1200, while in 2019 these values varied between 650-900 and in 2020 between 600-900. This shows that there has been a downward trend in the total number of complaints over the years. There were significant fluctuations in the number of monthly complaints in all three years, with an increase in the spring months in 2018 and 2019 and a decrease towards the end of the year.

![image](https://github.com/AtilaKzlts/Finance-Application-Complaints/blob/main/assets/pics/general.png)

Data analysis shows a positive development in complaint trends between 2018 and 2020. The decrease in the number of complaints from 850 to 750 proves that the measures taken have been effective. However, a more detailed analysis shows that each year there is a significant increase in complaints in May (around +100 units), followed by a sharp decline in September (around -50 units). This regular fluctuation indicates that there is probably a seasonal peak or a special operational situation in May. It is also observed that complaints are minimized in January of each year. In line with this data, it is recommended to take additional measures especially before May and to review the operational processes during this period. 

## Business Intelligence Questions +

### I. For issues that take more than 7 days to resolve, does the platform complained about make a difference?

![image](https://github.com/AtilaKzlts/Finance-Application-Complaints/blob/main/assets/pics/issue_7days_resolve.png)

After the assumptions and checks were made, Kruskal wallis was done and concluded that at least one of them was different and then Dunn's test was done and the results were ;

In the graph, we saw that the Referral communication type created a problem in solving the problem, but we did not know if this was random or significant. The results of Dunn's test support that your hypothesis is correct and that the 'Referral' group is significantly different from the other 'Sent-via' groups. So we can say that the 'Time_Diff' duration of the Routing group is statistically different from the other groups. 

### II. Is there a link between the answer given for the solution and the feedback of the customers?

![image](https://github.com/AtilaKzlts/Finance-Application-Complaints/blob/main/assets/pics/logistic_outputs.png)

Ci Square test was applied and it was found that there is a direct relationship between the answers given and customer disputes.
We will then run a logistic regression analysis to see which answer triggers customer returns,

The results are as follows;
+ `Closed with relief`, i.e. the provision of a solution in general terms, is the method that most reduces the likelihood that customers will complain again.
Closed with monetary relief is also very effective, indicating that customers are satisfied that they have received a financial response to their complaint.
The least effective method is Closed with explanation. This may indicate that just giving an explanation is not enough to ensure customer satisfaction and that the complaint requires a solution.    




###### *Atilla Kiziltas*


### [**Return to Portfolio**](https://github.com/AtilaKzlts/Atilla-Portfolio)
