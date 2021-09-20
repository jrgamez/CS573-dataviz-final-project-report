# Data Visualization Project Proposal

## Data

The data I propose to visualize for my project is from https://www.kaggle.com/sakshigoyal7/credit-card-customers

It is a dataset that contains demographic variables about the customers of a bank like age, gender, education level, etc and variables that capture their relationship with them, the patterns of use of their credit cards like transaction amounts, utilization ratio, month on book and credit limit and their current status. After doing some cleaning of the null values present and two unnecessary columns, its final structure contains:
  - 21 columns
  - 7,081 rows
  - 826 kB

The detail of all the columns is presented below:
| # | Variable | Type | Description |
| ------------- | ------------- | ------------- | ------------- |
| 1 | Clientnum | Categorical | Unique identifier for the customer |
| 2 | Attrition_Flag | Categorical | Internal event (customer activity) variable |
| 3 | Customer_Age | Quantitative  | Customer's Age in Years |
| 4 | Gender | Categorical | M=Male, F=Female |
| 5 | Dependent_count | Quantitative  | Number of dependents |
| 6 | Education_Level | Ordinal | Educational Qualification of the account holder |
| 7 | Marital_Status | Categorical | Married, Single, Unknown |
| 8 | Income_Category | Ordinal | Annual Income Category of the card holder (< $40K, $40K-60K, $60K-$80K, ...) |
| 9 | Card_Category | Ordinal | Type of Card (Blue, Silver, Gold, Platinum) |
| 10 | Months_on_book | Quantitative  | Months on book (Time of Relationship) |
| 11 | Total_Relationship_Count | Quantitative  | Total no. of products held by the customer |
| 12 | Months_Inactive_12_mon | Quantitative  | No. of months inactive in the last 12 months |
| 13 | Contacts_Count_12_mon | Quantitative  | No. of Contacts in the last 12 months |
| 14 | Credit_Limit | Quantitative  | Credit Limit on the Credit Card |
| 15 | Total_Revolving_Bal | Quantitative  | Total Revolving Balance on the Credit Card |
| 16 | Avg_Open_To_Buy | Quantitative  | Open to Buy Credit Line (Average of last 12 months) |
| 17 | Total_Amt_Chng_Q4_Q1 | Quantitative  | Change in Transaction Amount (Q4 over Q1)  |
| 18 | Total_Trans_Amt | Quantitative  | Total Transaction Amount (Last 12 months) |
| 19 | Total_Trans_Ct | Quantitative  | Total Transaction Count (Last 12 months) |
| 20 | Total_Ct_Chng_Q4_Q1 | Quantitative  | Change in Transaction Count (Q4 over Q1)  |
| 21 | Avg_Utilization_Ratio | Quantitative  | Average Card Utilization Ratio |

## Prototypes

I’ve created some proof of concept visualizations of this data. The first one is a scatter plot that shows the age of the customers on the x-axis, their total expenditure using the card on the y-axis and their current card status on the color of the points (black if they still have the card or red if they don’t). The main idea is to group the customers based on their expenditure levels and also compare the expenditure level of customers that stopped using their cards with the ones that still use them.

[![image](https://user-images.githubusercontent.com/72701739/133905253-31179699-0b8a-4937-9560-0afa7bd0a0d4.PNG)](https://vizhub.com/jrgamez/c0201ec0375049798e90aef67fdc677a)

The second one is a grouped bar chart that shows the average amount spent by the customers using their credit cards by gender and education level. The gender was encoded using different color and the bars where placed next to each other to compare between both genders within the same education level. Also one goal is to see how the amounts spent tend to change as the customers acquire a higher education level.

[![image](https://user-images.githubusercontent.com/72701739/133905266-7915dd52-a8ac-4d8b-8119-70096f157553.PNG)](https://vizhub.com/jrgamez/6fa5ab323e6e4156bbc8375cf611e094)

## Questions & Tasks

The following tasks and questions will drive the visualization and interaction decisions for this project:

 * Is there a relationship between age and income category?
 * How do income categories compare to each other in terms of credit limits and utilization ratios?
 * Do female customers use the credit card more than male customers?
 * Do people with higher education level use the credit cards more?
 * Is there a relationship between attrition flag and age, education level or income category?

## Sketches

(insert one or more hand-drawn sketches of interactive visualizations that you imagine)
(describe each sketch - how is the data visualized, what are the interactions, and how do these relate to the questions/tasks)

## Open Questions

 * I want to use dynamic plots but I don´t know how to create functions to send the parameters
 * I had problems processing my data to create some plot on the homeworks. Do I need to create my own functions to do the grouping or D3 has some functions already implemented? Also if there are, where can I find the documentatio?

