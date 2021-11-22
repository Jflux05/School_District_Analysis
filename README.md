# School_District_Analysis

## Overview
Analyzing the city school district data from a variety of sources and in a variety of formats. We have been asked to provide insights about performance trends from standardized tests and patterns occuring within the school district. These insights will be used to inform discussions and strategic decisions at the school and district level. The city school district has tasked us with using these insights to determine if there is a correlation between school performance and its funding, student population, or the school types (charter or district).  

The city school ditrcit board also determined that there is evidence of academic dishonesty, specifcally, the math and reading grades for Thomas High School ninth graders appear to have been altered. As a result, we refractored our script parameters to ensure the analysis results for per student averages wouldn't be skewed and incorrectly influence the school boards strategic decisions.  

## Results
Through our intial analysis, we were able to identify top performing schools, by budget, size, and school type. However, with eveidence of possible academic dishonesty within our data sample (specific to the Thomas High School's 9th grade testing results), required a revision in our analysis to exclude all data related to the suspected group of students (test results for 9th grade students at Thomas High School were replaced with NaN). In the results below we have provided our original results and the revised analysis results to compare againast one another for the School Board to have a holistic picture of the district and the potential impact from academic dishonesty. 

### District Summary
-ORIGINAL ANALYSIS
![district_summary_df_original_results_screenshot](https://github.com/Jflux05/School_District_Analysis/blob/8d5519beae5b34a7f18f52f0e7cc0d0b42a16713/Resources/district_summary_df_original.png)

- ANALYSIS WITHOUT 9th GRADE SCORES FROM THOMAS HIGH SCHOOL
![district_summary_df_new results_screenshot](https://github.com/Jflux05/School_District_Analysis/blob/8d5519beae5b34a7f18f52f0e7cc0d0b42a16713/Resources/district_summary_df_new.png)

As you can see from the above screenshots, the recalculations had minimal impact on the district summary results. It is evident that while their impact was minimal, the 9th grade scores that were omitted due to potential academic dishonesty, did skew the results to be marginally higher. 

- Marinal Result Impacts:
  - The percentage of students passing all subjects fell from 65% to 64.9%
  - The average student math score dropped from 79.0 to 78.9. While the percentage of students passing math fell from 75% to 74.8%.
  - The average student reading score remained unchained 81.9, however, the percentage of students passing reading fell from 86% to 85.7%.

### School Summary

In the following screenshots of our analysis, you will see the original results, the analysis and specifically the impact on Thomas High School by replacing the 9th grader's results with "Nan", and the final results once we refactored the script to account for the new total student count. 

There is a clear and expected variance betweeen our intial results and the results with the 9th grade scores set to NaN when looking specifically at the percent passing results forThomas High School. While this was expected, when we refactored the code, the variance between our original results and our refactored version show only a slight variance.

- ORIGINAL ANALYSIS RESULTS:
![per_school_df_summary_old_screenshot](https://github.com/Jflux05/School_District_Analysis/blob/5c488474786e57ad2b640114a7f194d08b79c08d/Resources/per_school_summary_df%20old%20screenshot.png)


- RESULTS WITH NaN FOR 9th GRADE SCORES:
![per_school_df_summary_NaN_screenshot](https://github.com/Jflux05/School_District_Analysis/blob/5c488474786e57ad2b640114a7f194d08b79c08d/Resources/per_school_summary_df_NAN_old_screenshot.png)

- REFACTORED RESULTS (ACCOUNTS FOR ADJUSTED TOTAL STUDENT COUNT):
![per_school_df_summary_new_screenshot](https://github.com/Jflux05/School_District_Analysis/blob/5c488474786e57ad2b640114a7f194d08b79c08d/Resources/per_school_summary_df_new_screenshot.png)

- COMPARING ORIGINAL RESULTS WITH REFACTORED RESULTS:
  - The overall percentage of students passing both math and reading at Thomas High School decreased slightly from 90.95% to 90.63%.
  - The percentage of students passing math also had a marginal reduction, falling from from 93.27% to 93.18%.
  - The percentage of students passing reading also had a marginal reduction, falling from from 97.31% to 97.01%.
  - The average math score at Thomas High School was not greatly impacted and saw a minor drop in scores from 83.41 to 83.35. 
  - The average reading score at Thomas High School actually improved but not by much, from 83.84 to 83.89. 

### Results of Replacing 9th Grade Math and Reading Scores Relative to the Other Scools:

- TOP 5 SCHOOLS IN CITY DISTRICT (ORIGINAL ANALYSIS)
![top_five_schools_old](https://github.com/Jflux05/School_District_Analysis/blob/287d114302ece361431ce162b7ccab4900892c91/Resources/top_5_performing_schools_old.png)

- TOP 5 SCHOOLS IN CITY DISTRICT (REFACTORED ANALYSIS)
![top_five_schools_new](https://github.com/Jflux05/School_District_Analysis/blob/287d114302ece361431ce162b7ccab4900892c91/Resources/top_5_performing_schools_new.png)

From the above comparison, we can see that there was a slight reduction in the following categories: Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, and % Overall Passing. All of the aforementioned categories had marginal drops (less that 1% across all categories), which was not significant enough to drop Thomas High School's rank below other schools in the district. It still remains the second best school in the district. 


### Math and Reading Scores By Grade
- MATH SCORES BY GRADE (ORIGINAL OUTPUT)

![per_grade_math_scores_old](https://github.com/Jflux05/School_District_Analysis/blob/3915abf62ba4a23c129b988ec67dc9c8b1b2544a/Resources/per_grade_math_scores_old.png)

- MATH SCORES BY GRADE (REFACTORED OUTPUT)

![per_grade_math_scores_new](https://github.com/Jflux05/School_District_Analysis/blob/3915abf62ba4a23c129b988ec67dc9c8b1b2544a/Resources/per_grade_math_scores_new.png)

- READING SCORES BY GRADE (ORIGINAL OUTPUT)

![per_grade_reading_scores_old](https://github.com/Jflux05/School_District_Analysis/blob/3915abf62ba4a23c129b988ec67dc9c8b1b2544a/Resources/per_grade_reading_scores_old.png)


- READING SCORES BY GRADE (REFACTORED OUTPUT)

![per_grade_reading_scores_new](https://github.com/Jflux05/School_District_Analysis/blob/3915abf62ba4a23c129b988ec67dc9c8b1b2544a/Resources/per_grade_reading_scores_new.png)

As we can see by comparing the original and new ouputs for the average subject scores by grade, removing the 9th grade THS scores had absolutely no numeric impact on the DataFrames other than to replace the scores with "nan".





