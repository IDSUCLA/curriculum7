If you have any question, please contact us at [support@idsucla.org](mailto:support@idsucla.org)

LAUSD teachers please email [IDSsupport@lausd.net](mailto:IDSsupport@lausd.net)

Introduction to Data Science, [https://www.idsucla.org](https://www.idsucla.org){:target="_blank"}

This website was last updated on February 4, 2025.

Changes that have been made to version 7.0

**All Units**

 - Naming convention of LMRs have been updated to match Unit and Lesson (example: LMR_1.1_Data Diary is now LMR_U1_L1)
 - All preloaded datasets have been updated to reflect original variable names (example: ```cdc``` gender variable is sex variable in original documentation)
 - ```cdc```, ```atus```, and ```futbol``` datasets have been updated to more recent data
 - There is an anonymized dataset available for the Stress/ Chill (unformatted) Campaign. It can be accessed by running the following code:
        
        extra_data('stresschill_ids')

        #If you'd like to merge this dataset with your class, follow these steps:
        #Create a subset stresschill_class of your class data without the variables 
        # of latitude and longitude
        #This assumes your class set is named p6_stress
        
        stresschill_class <- subset(p6_stress, select = -c(latitude, longitude))
        
        #bring in stresschill_ids dataset from IDS archive
        extra_data('stresschill_ids')
        
        #row bind the 2 datasets together
        stresschill_full<- rbind(stresschill_class, stresschill_ids)

**Unit 1**

 - Lesson 5: Oscar winners data has been updated
 - Lesson 14: LMR_U1_L14_B and LMR_U1_L14_D use sex variable instead of gender
 - Practicum: The Summaries: Third example uses sex variable instead of gender

**Unit 2**

 - Lesson 9: Changed "biased" to "unfair"
 - Lesson 17: Changed household size to household activities (```atus``` variable change)

**Unit 3**

 - Lesson 8: Updated spurious correlations images/examples due to update in spurious correlations website
 - Lesson 21: Lesson now compares HTML code to XML code (via website viewer), LMR has been udpated to reflect changes in lesson
 - Lesson 22: Lesson now goes through how to convert XML code to data table in RStudio, LMR has been updated to reflect changes in lesson

----------------------------------------------------
Changes that have been made to version 6.0

**All Units**

 - Labs now also have text which direct students to complete tasks within the RStudio/Posit interface in <span style="color:midnightblue;">**blue**</span> font
 - GPS no longer reports precise location
 - There are anonymized datasets available for the Food Habits, Personality Colors, and Time Use (unformatted) Campaigns. They can be accessed by running the following code:
        
        extra_data('food_ids')
        extra_data('colors_ids')
        extra_data('timeuse_ids')

**Unit 1**

 - Food Habits and Time Use campaign questions, in the campaign guidelines, have been modified for clarity
 - Lesson 1: LMR_1.1 changed "Facebook" to "TikTok"
 - Lesson 14: updated LMR_1.16 with new data/color palette
 - Lesson 17: updated plots and cleaned up formatting on LMR_118
 - Lab 1B has more clarification on options/arguments
 - Labs 1C and 1F now have embedded videos to help guide students
 - Lab 1D has more explanation about filtering and the assignment operator

**Unit 2**

- Stress/Chill campaign questions have been modified for clarity (and picture question has been removed)

**Unit 3** 

**Unit 4**

 - Section 1 is now Campaigns and Community where we set the stage for the End of Unit Project (also updated)
 - Section 2 has been rehauled to improve the flow for the lessons on linear regression
 - Section 2 also caps off with non-linear models with Lesson 13: Improving your Model (previously Lesson 14)
 - Section 3 is now Piecing it Together with only the two lessons on multivariable regression
 - The lessons in Section 4 have been slightly rearranged - part of Lesson 17 was moved to Lesson 16 for better building of concepts.
 - Lesson 18: the LMR was modified for clarity. We also added instructions for the k-means clustering app.
 - The End of Unit Project is student choice around a community issue
 - Unit 4 Assessments have been updated (access through the Documents tool on Portal) - link to lungs data and solutions.
 - Lab 4D lab solutions, MSE for 2nd variable changed to use y-variable, ```critics_rating```, in residual calculation/code

