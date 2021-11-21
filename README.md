# School_District_Analysis

## Overview
Analyzing the city school district data from a variety of sources and in a variety of formats. We have been asked to provide insights about performance trends from standardized tests and patterns occuring within the school district. These insights will be used to inform discussions and strategic decisions at the school and district level. The city school district has tasked us with using these insights to determine if there is a correlation between school performance and its funding, student population, or the school types (charter or district).  

The city school ditrcit board also determined that there is evidence of academic dishonesty, specifcally, the math and reading grades for Thomas High School ninth graders appear to have been altered. As a result, we refractored our script parameters to ensure the analysis results for per student averages wouldn't be skewed and incorrectly influence the school boards strategic decisions.  

## Results
Through our intial analysis, we were able to identify top performing schools, by budget, size, and school type. However, with eveidence of possible academic dishonesty within our data sample (specific to the Thomas High School's 9th grade testing results), required a revision in our analysis to exclude all data related to the suspected group of students (test results for 9th grade students at Thomas High School were replaced with NaN). In the results below we have provided our original results and the revised analysis results to compare againast one another for the School Board to have a holistic picture of the district and the potential impact from academic dishonesty. 

### District Summary

![district_summary_df_original_results_screenshot](https://github.com/Jflux05/School_District_Analysis/blob/8d5519beae5b34a7f18f52f0e7cc0d0b42a16713/Resources/district_summary_df_original.png)

![district_summary_df_new results_screenshot](https://github.com/Jflux05/School_District_Analysis/blob/8d5519beae5b34a7f18f52f0e7cc0d0b42a16713/Resources/district_summary_df_new.png)

As you can see from the above screenshots, the recalculations had minimal impact on the district summary results. It is evident that while their impact was minimal, the 9th grade scores that were omitted due to potential academic dishonesty, did skew the results to be marginally higher. 

- Marinal Result Impacts:
  - The percentage of students passing all subjects fell from 65% to 64.9%
  - The average student math score dropped from 79.0 to 78.9. While the percentage of students passing math fell from 75% to 74.8%.
  - The average student reading score remained unchained 81.9, however, the percentage of students passing reading fell from 86% to 85.7%.











