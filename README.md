# Analysis of Kickstarter Campaigns

## Project Overview and Purpose

The purpose of this project is to discover by analyzing the Kicstarter data if any campaign parameters contribute to the outcome (success or failure) of the campaign.  Specifically, this analysis explores these relationaships, if any:

    * Correlation between project (specifically Theater) launch date and its outcome
    * Correlation between project financial goal and its outcome
    
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

THe raw Kickstarter data had to be manipuated in several ways for it to be useable for analysis:

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
    
    Goal
less than 1000
1000 to 4999
5000 to 9999
10000 to 14999
15000 to 19999
20000 to 24999
25000 to 29999
30000 to 34999
35000 to 39999
40000 to 44999
45000 to 49999
Greater than 50000
![image](https://user-images.githubusercontent.com/84471904/123321851-5d6f2b80-d4e8-11eb-89db-9280404bc060.png)

  
  


## Results and Conclusions
    



![image](https://user-images.githubusercontent.com/84471904/123289803-9e097d80-d4c5-11eb-96ce-534a19a0e6a1.png)
