# Analysis of Kickstarter Campaigns

## Project Overview and Purpose

The purpose of this project is to discover by analyzing the Kickstarter data if any campaign parameters contribute to the outcome (success or failure) of the campaigns.  Specifically, this analysis explores these relationships, if any:

•	Correlation between campaign (specifical theater) launch date and its outcome

•	Correlation between project funding goal and its outcome
    
## Analysis and Challenges

   ### Outcomes Based on Launch Date Analysis

   The steps to analyze the relationship between the number of Theater campaigns and their launch dates:
   
    1.  Add Years column to Kickstarter data sheet
    2.  From the Kickstarter data sheet, create a pivot table based on "Parent Category" and "Years"
    3.  Select outcomes for the Columns and Values fields, date created conversion for the Rows field.

  ![image](https://user-images.githubusercontent.com/84471904/123309279-9358e380-d4d9-11eb-981e-e16d49dd5fbc.png)

    4. Filter the column labels to show "Successful," "failed," and "canceled".  
    5. Created pivot table: 
    
   ![image](https://user-images.githubusercontent.com/84471904/123311009-85a45d80-d4db-11eb-9c6a-a93d86b21dbd.png)

   6.  Create and format line chart 

![image](https://user-images.githubusercontent.com/84471904/123290734-5cc59d80-d4c6-11eb-8aff-69eb23ad4944.png)

#### _Challenges_

THe raw Kickstarter data needs to be manipuated in several ways for it to be useable for analysis:

   1.  The dates in the initailly provided Kickstarter data were in Unix timestamps.  To convert these dates into a useable format, a new column was created and the following formula used: =(((J2/60)/60)/24)+DATE(1970,1,1).


   ![image](https://user-images.githubusercontent.com/84471904/123316404-a66fb180-d4e1-11eb-8361-89033b18d533.png)

     
   2.  In order to look specifically at the campaign dates and outcomes for Theater campaigns, the subcategory "Theater" had to be seperated out from the "Category and Subcategory" column.  THis was achieved by using the "convert Text to Colums Wizard".  
   
   For example, by seperating out "film/video/television" to parent category "film & video" and subcategory "televion", can now explore trends specifically on television:


   ![image](https://user-images.githubusercontent.com/84471904/123316891-3e6d9b00-d4e2-11eb-8784-fbe009ca6028.png)
   
   


  ### Outcomes based on Goals
  
  The steps to analyze the relationship between the financial goals of a campaign and its outcome (successful or failure or canceled):
   
    1.  Create a new worksheet for the information to be collected.  
    2.  Create columns for the information that will be collected. 
 
![image](https://user-images.githubusercontent.com/84471904/123321893-6bbd4780-d4e8-11eb-9c4d-825d29feaf2a.png)

    
    3.  In the "goal" column , want to analyze by dollar-amount ranges so that projects can be grouped based on their goal amount.  
   
![image](https://user-images.githubusercontent.com/84471904/123321851-5d6f2b80-d4e8-11eb-89db-9280404bc060.png)

    4.  Populate columns
         a.  Columns B through D ;  used "countifs" 
         b.  Colulmns E:  Sum columns B through D for each row
         c.  Columns F throuh G: find percantages 
         
    5.  Create chart:
         a.  Highlight columns A, F, G, H. 
         b.  Select "insert" from Tools Ribbon and select line chart.
         c.  Format chart
  

![image](https://user-images.githubusercontent.com/84471904/123289803-9e097d80-d4c5-11eb-96ce-534a19a0e6a1.png)

#### _Challenges_

As outlined in the Analysis section, the data needed to run this analysis had to be first generated from the raw Kickstart data.

A review of using "countifs" may be necessary if unfamiliar with this option.


## Results and Conclusions

_Theater Outcomes Based on Launch Date_

The first task of this analysis of the kickstarter data was to look at the relationship (if any) of theater campaigns and their launch dates.  After analyzing a total of 1369 Theater projects, the resulting pivot table and graph show:

•	May and June have the highest number of successful theater campaigns.   These months are the optimal time to plan a theater campaign
•	November through January have the lowest number of successful theater campaigns.  These months are the least desirable for running a theater campaign.

_Theater Outcomes Based on Goals_

The second task of this analysis of the kickstart data was to look at the relationship (if any) between the financial goals of a project and its outcome.  The line chart generated from the data set shows:

•	Projects with goals less than $5000 had relatively high success rates and fairly low failure rates
•	Projects over $45,000 had very high failure rates and very low success rates

### Limitations of the data set

There is a great deal of useful information in the Kickstarter data set.  However, there is not enough data to give a complete picture.  Questions that come to mind, for example, are:

•	In the Outcomes Based on Goals analysis, why is there a decline of successful projects starting at $5000 goal, with a strong drop at the range $25,000 to $30,000, and then a strong success rate at $35,000 to $40,000?  There must be more at work than just the financial goal of the campaigns.  There is not enough data to explain these trends.

•	If there is interest in specifically the theaters/plays category, it would be useful if there is more information about the play genres – an additional category to define if a play is drama, comedy, satyr, etc.  This more specific breakout is available in publishing and music, for example. 

•	The Country of the campaign is available.  It could be useful if this was broken down to regions or major cities within a country to get a more accurate picture of theater successes and failures.  For example, in the United Staes, a play successful in Boston may not be as successful in Oklahoma City.  


### Possible future analysis topics

•	It might be useful to look at trends by year.  There may be something at work on a large scale that is affecting campaign outcomes.  For example, the pandemic of 2019/20 would have a very strong influence on theater attendance and therefore campaign success.

•	It might be useful to look at time interval between campaign launch date and deadline date.  Does this have any impact on a campaign’s success?  






    




