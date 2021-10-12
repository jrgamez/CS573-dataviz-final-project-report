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

[![image](https://user-images.githubusercontent.com/72701739/136973933-7602af34-11ce-43ab-9e38-e2512834496d.png)](https://vizhub.com/jrgamez/2f14457296a247a98d956dc34782e219)

The second one is a grouped bar chart that shows the average amount spent by the customers using their credit cards by gender and education level. The gender was encoded using different color and the bars where placed next to each other to compare between both genders within the same education level. Also one goal is to see how the amounts spent tend to change as the customers acquire a higher education level.

[![image](https://user-images.githubusercontent.com/72701739/136973949-470f74e7-af94-4da3-9f1e-4aeacffdc243.png)](https://vizhub.com/jrgamez/58a0f64508a74969bbe78865c49b7216)

[![image](https://user-images.githubusercontent.com/72701739/136973957-b9990e36-34ff-4328-a655-674659cd7f7d.png)](https://vizhub.com/jrgamez/c0eeae34b7d7492ca0c340ffb4c10b21)

## Questions & Tasks

The following tasks and questions will drive the visualization and interaction decisions for this project:

 * Is there a relationship between card usage and age or income category?
 * How do income categories compare to each other in terms of credit limits?
 * Do female customers use the credit card more than male customers?
 * Do people with higher education level use the credit cards more?
 * Is there a relationship between attrition flag and age, education level or income category?
 * What is the relationship between the usage and card possession?

I want to use some categorical variables like education level, marital status and age group (new column) to filter the data and make the analysis more dynamic and interactive.

## Sketches

![image](https://user-images.githubusercontent.com/72701739/134211954-57cbdea6-78b0-49a0-8407-02ff4b3cd126.jpg)

I decided to focus right now on analyzing what is the profile of the customers that decide to stop using their credit cards. In that sense, all the visualizations encode the status using the same color for consistency and I crossed that variable with the others. Also, there are 3 main quantitative variables that I would like to check: Total Transactions Amount, Credit Limit and Total Revolving Balance, so I would like to add a drop down at the top to select one of these 3 variables to be displayed on the y-axis of the 3 graphs at the top. 

* The first plot is to analyze the relationship between age, expenditure level (or any of the other 2 variables that could be selected) and the credit card status to see how customers with different ages and expenditure patters behave.
* The second and third plot present the expenditure level (or any of the other 2 variables that could be selected) by income level and education level respectively. This relates to the question about how people with higher education or income uses their cards.
* The fourth and fifth plot (the two at the bottom) check how the people that stopped using their cards distribute by card type and gender

It would be great to use the plots at the bottom as filters for the ones at the top to filter the data by card type and gender and see how the behavior changes. Also a tooltip should appear as the mouse is placed above and bar, point or part of the circles to show the values of the variables that belong to it.

## Schedule of Deliverables

1. Create reusable Histogram and Boxplot visualizations with dynamic columns. (Oct 20th)
2. Create a canvas to arrange all the elements of my final visualization. (Oct 27th)
  * Accommodate all the plots in a 4 by 4 grid.
  * Create a section for all the menus of the plots.
  * Add titles and legends. 
3. Tweak the size of all the elements on the plots to make them fit nicely on the grid. (Oct 30th)
4. Check that all the individual interactions are working correctly and fix the ones that doesn't. (Nov 3rd)
5. Add the interaction between the plots. (Nov 7th)
  * Add a filtering effect when hovering over a donut chart or a clustered bar.
  * Add a highlighting effect when hovering over the values on the legend. (It is common for all the plots)
6. Test all the functionality and deliver the final visualization. (Nov 10th)
