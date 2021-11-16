# Data Visualization Project Proposal

## Data

The data I propose to visualize for my project is the [Bank Customers Dataset](https://gist.github.com/jrgamez/c9ea9e8a5d6d000619b31b8499af6a83). 

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

## Main Goal, Questions & Tasks

The main goal for this project is to create a visualization that can be used to perform an exploratory data analysis on the dataset. The main task is to visualize the relationship between the attrition flag and all the other variables available to identify the main features that are associated with a client that stopped being a customer of the bank and create a profile. The following questions are some examples of questions that could be answered using the final dashboard and will drive the visualizations and interaction decisions for this project:

 * Is there a relationship between card usage and age or income category?
 * How do income categories compare to each other in terms of credit limits and attrition levels?
 * Do female customers use the credit card more than male customers?
 * Do people with higher education level use the credit cards more or attrite more?
 * Is there a relationship between attrition flag and age, education level or income category?
 * What is the relationship between the usage and card possession?

## Proposed Dashboard Sketch

To be able to answer the proposed questions and perform an effective exploratory analysis of the dataset, a dashboard with 5 different sections is proposed. The idea is to have a section with all the menus so the users can select the variables that will be displayed on the graphs and 4 other sections to display the relationship between the attrition flag variable and some combinations of some other quantitative and categorical variables. 

All the plots will encode the attrition flag variable using the same color for consistency, the analysis will focus on 5 main quantitative variables: customer age, credit limit, total transactions amount, total revolving balance and total transactions count; so these will be options present on the menus and the categorical variables: education level, marital status, income category, card category and gender will be used to filter the data presented on the visualizations to make the analysis more dynamic and interactive. Finally, with all of these ideas in mind, the sketch of the proposed dashboard is presented below:

![image](https://user-images.githubusercontent.com/72701739/137059016-0b85f161-1c32-47aa-a65b-9f756fde8c4b.jpg)

* The first graph is a scatter plot that can be used to analyze the relationship between two quantitative variables and the attrition status of the customers to find patterns.
* The second plot is a clustered bar chart that presents the relationship between one quantitative variable (y-axis) and one categorical variable (x-axis) and the attrition status using the average value for each category. This can enable the user to see how customers in different categories behave.
* The third plot is an array of donut charts that displays the percentage of attrited customers based on a categorical variable (x-axis). The number of donut charts on the array depends on the number of categories that the selected variable has and can be used to see how the percentage of attrited customers varies over different categories.
* The last plot is an array of boxplots that shows the distribution of a quantitative variable (y-axis) by the attrition flag value (x-axis). This will be used to analyze how the distribution of a quantitative variable changes based on the attrition status of the customers.

Finally, all the plots share the same legend since the attrition flag variable is used in all of them and there would be a highlight effect when the users hover over the values on the legend to highlight the corresponding elements on the plots. Also a tooltip will appear as the mouse is placed over any element on all the graphs to display additional information and the donut charts will be used to filter the data on the other plots so only the values for the selected category are used and displayed.

## Prototypes

I’ve created some of the proposed plots on vizhub. The first one is a scatter plot that shows the age of the customers on the x-axis, their total transactions amount using the card on the y-axis and their current attrition status on the color of the points (blue if they still have the card or gray if they don’t). The main idea is to group the customers based on their expenditure levels and also compare the expenditure level of customers that stopped using their cards with the ones that still use them. In this plot the users can change the variables displayed and there is a highlighting effect when the mouse hovers over the legend.

[![image](https://user-images.githubusercontent.com/72701739/136973933-7602af34-11ce-43ab-9e38-e2512834496d.png)](https://vizhub.com/jrgamez/2f14457296a247a98d956dc34782e219)

The second one is a grouped bar chart that shows the average amount spent by the customers using their credit cards by income level grouped by attrition flag. Again, the attrition flag was encoded using the same colors on the scatter plot for consistency and the bars where placed next to each other to compare the values between different categories within the same income level. Additionally, in this plot the users can change the variables displayed but only categorical variables can be selected for the x-axis, quantitative variables for the y-axis and there is a highlighting effect when the mouse hovers over the bars and a tooltip with the information used to calculate the averages.

[![image](https://user-images.githubusercontent.com/72701739/136973949-470f74e7-af94-4da3-9f1e-4aeacffdc243.png)](https://vizhub.com/jrgamez/58a0f64508a74969bbe78865c49b7216)

Finally, the last prototype is an array of donut charts that shows the percentage of customers that have attrited by marital status. Additionally, in this plot the users can change the categorical variable to be used for the x-axis and there is a highlighting effect when the mouse hovers over the bars.

[![image](https://user-images.githubusercontent.com/72701739/136973957-b9990e36-34ff-4328-a655-674659cd7f7d.png)](https://vizhub.com/jrgamez/c0eeae34b7d7492ca0c340ffb4c10b21)

## Iterated Work

### Nov 3rd, 2021
Since it is difficult to compare the sizes of the gray segments between different donuts on the array of donut charts, I changed the representation to a stacked bar chart. In this case the dynamic selection of the categorical variable remains but now there is a bar for each category instead of a donut. Also the users can hover over each bar to see the exact percentage value associated with it and can hover over the legend to highlight the bars. This change makes easier to compare between different categories since the percentage difference are small so it is better to present them next to each other.

[![image](https://user-images.githubusercontent.com/72701739/138563693-f907cb29-dbb1-4c47-b5e3-cf285ea6091c.PNG)](https://vizhub.com/jrgamez/7e6f934dff2448308837218455480ec5)

### Nov 10th, 2021
I created the dynamic boxplots so the users can see the distribution of quantitative variables by the attrition status of the customers. This enables the users to select the quantitative variables that they want to visualize and compare the distribution of both kind of customers to see how the value of the variables differ from existing and attrited ones. Some information about the quartiles, minimum and maximun values is included on the tooltip that can be seen by hovering over the lines and boxes on the plots.

[![image](https://user-images.githubusercontent.com/72701739/140621335-dc6ba0bf-6a2b-41db-9df9-a2de19e741f5.PNG)](https://vizhub.com/jrgamez/245fb4ed3a264319bf1fb23b6820f3e2)

Also, I created a grid and put together all the plots that I've created until now. Also created a section for all the menus to change the variables displayed in each plot and the legend with the attrition status (It's the same for all the plots). I had to resize the elements and adjust them to make sure that they fitted in a cohesive way. The menus and hovering functionality of the plots is working but some of the functionality that was on the legend is not working yet and that would be the focus of the next iteration.

[![image](https://user-images.githubusercontent.com/72701739/140621008-9bef884e-5b84-4427-98f8-7d25fe0efbf5.PNG)](https://vizhub.com/jrgamez/56624b2e15714fd59582ffe0d6de11a1)

### Nov 16th, 2021
Based on the feedback, I decided to create a dynamic violin plot visualization to replace the box plots that I created last week. In this case the same data is being encoded (the distribution of quantitative variables by attrition status) but the representation is less restrictive as it displays more details to the users which can be more helpful and make it easier to compare between the different shapes of the distributions. The information about the quartiles, minimum and maximum values is still included in the tooltip that can be seen by hovering over the violins on the plot. Also I added this new plot to the dashboard grid.

[![image](https://user-images.githubusercontent.com/72701739/142013783-54e7b203-b4b0-443d-8184-21cc87b12029.PNG)](https://vizhub.com/jrgamez/43c93bbdb60741fea81e9ff24d8b0b7c)

[![image](https://user-images.githubusercontent.com/72701739/142013792-71b2cb0b-1e17-44fa-891a-17e81b52baa6.PNG)](https://vizhub.com/jrgamez/56624b2e15714fd59582ffe0d6de11a1)

## Schedule of Deliverables

1. Create a reusable Boxplot visualization with dynamic columns. (Oct 20th) **(DONE)**
2. Add interaction to the boxplots. (Oct 24) **(DONE)**
3. Create a canvas to arrange all the elements of my final visualization. (Oct 30th) **(DONE)**
    * Accommodate all the plots in a 4 by 4 grid.
    * Create a section for all the menus of the plots.
    * Add titles and legends. 
4. Tweak the size of all the elements on the plots to make them fit nicely on the grid. (Nov 3rd) **(DONE)**
5. Check that all the individual interactions are working correctly and fix the ones that doesn't. (Nov 7th) **(DONE)**
6. Add the interaction between the plots. (Nov 10th)
    * Add a filtering effect when hovering over a donut chart or a clustered bar.
    * Add a highlighting effect when hovering over the values on the legend. (It is common for all the plots)
7. Test all the functionality and deliver the final visualization. (Nov 17th)
