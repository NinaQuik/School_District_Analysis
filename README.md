# School_District_Analysis
Module 4 - Python, Pandas Library, Jupyter Notebook
## Overview
This module uses Python and Pandas Library to analyze performance trends across schools based on student funding, school size, school type and standardized test scores. The aggregated data is used to make education budget and prioritization decisions.

However, there is evidence that grades for Thomas High School ninth graders have been altered.  

The aggregated results are re-run after removing the Thomas High School ninth grader grades to determine if the performance trends have altered in any way due to the academic dishonesty.

The Data Set is comprised of both  [school data](Resources/schools_complete.csv) and [student data](Resources/students_complete.csv).

The initial analysis is performed in [PyCitySchools.ipynb](PyCitySchools.ipynb)
The subsequent analsysis with the removal of the THS (Thomas High School) ninth grader grades was performed in [PyCitySchools_Challenge.ipynb](PyCitySchools_Challenge.ipynb)

## Results
- **District Summary**

 Below are the results of the district summary for all schools with and without the Thomas High School Ninth Grader grades.  As you can see, there were marginal changes (within tenths of a percentage) in math scores, reading scores and overall passing grades. Obviously the number of schools, students and budget are unchanged.
 
 **With THS Ninth Grader Grades**
 ![District Summary with Thomas High School Ninth Grader Grades](/Resources/District_Summary_Before.png)
 **Without THS Ninth Grader Grades**
 ![District Summary WITHOUT Thomas High School Ninth Grader Grades](/Resources/District_Summary_After.png)
 
 - **School Summary**
 
   - The school summary for all schools except Thomas High School remained the same.  
   - With the Ninth Grader grades included in the report, Thomas High School had a 90.95% overall Passing rate.  The average reading score was 83.85, Average math score was 83.42.   
   - Without the Ninth Grader grades, Thomas High School took a slight dip to 90.63% overall passing rate.  Average Math score is 83.35 and Average reading increased slightly to 83.90.
- **Thomas High School Comparison**
  - Removal of the ninth grader grades did little to knock Thomas High School out of the second position as top performing school in the district. The slight decrease from 90.95% to 90.63% for THS did not move the needle. 
  - Carbrera High remains the top performing school in the district.
  - This rating is based on Overall Passing Percentage. 
  
- **Math and Reading Scores by Grade**
  - Because the removal of grades was surgically performed only against 9th graders at Thomas High School, the math and reading scores by grade and school are static for all grades/schools besides THS 9th graders.  
  - This can be verified converting a series of scores by grade into a data frame with school as an index. 
  - NaN now appears for THS 9th grade.
  - [Ex. School/Grade Breakdown](Resources/Math_Scores_By_Grade.png)

- **Scores by School Spending**
  - Thomas High School has a Per Student Budget of $638.00. 
  - When Scores by School Budgets were calculated, Thomas High School fell into the $630 to $644 bin. 
  - Obviously all other bins should be unaffected. 
  - However, replacing the ninth grader grades at Thomas High School almost had no impact on scores by school spending.  When overall passing scores for each bin is rounded to zero decimal places, no change was observed.  
  - Rounding to two decimal places shows that the overall passing rate for the $630 to $644 bin decreased from 62.86 percent to 62.78 percent.

- **Scores by School Size**
  - Thomas High School has 1635 students.  This puts THS solidly in the Medium School Size (1000 - 2000 students).  
  - As expected, the scores for Small and Large schools are not impacted by removing THS ninth grader grades.  
  - Like Scores by School Spending, the removal of these grades had nominal impact on school size summaries. Rounding to zero decimal places showed no change.
  - Rounding to two decimal places revealed a slight drop from 90.62% overall passing to 90.56% overall passing, with similar tenths of percentage drops in reading and math scores.

- **Scores by School Type**
  - The trend continues with Scores by School Types summaries.  
  - Thomas High School is a charter school, so it would be expected that only charter school aggregates are impacted. 
  - However, rounding to zero decimal places show no change to charter high school performance.
  
