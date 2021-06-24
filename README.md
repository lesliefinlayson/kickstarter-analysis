# Analysis of Kickstarter Campaigns

## Project Overview and Purpose

The purpose of this project is to discover by analyzing the Kicstarter data if any campaign parameters contribute to the outcome (success or failure) of the campaign.  Specifically, this analysis explores these relationaships, if any:

    * Correlation between project (specifically Theater) launch date and its outcome
    * Correlation between project financial goal and its outcome
    
## Analysis and Challenges

   ## Outcomes Based on Launch Date Analysis

   The steps to analyze the relationship between the success rate of Theater campaigns and their launch dates:
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


   ## Outcome based on Goals


## Results and Conclusions
    



![image](https://user-images.githubusercontent.com/84471904/123289803-9e097d80-d4c5-11eb-96ce-534a19a0e6a1.png)
