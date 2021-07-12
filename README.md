# School District Analysis

## Project Overview
This project was commissioned by the PyCity School District School Board to analyze data on student funding and standardized test scores.  Standardized test data was prepared for analysis, reporting, and presentation to provide insights about performance trends and patterns.  Insights from this analysis can be leveraged to inform discussions and strategic decisions at the school and district levels.  

Deliverables include:
- A high-level snapshot of the district's key metrics, presented in a table format.
- An overview of the key metrics for each school, presented in a table format.
- Tables presenting each of the following metrics:
  
  - Top 5 and bottom 5 performing schools, based on the overall passing rate.
  - The average math score received by students in each grade level at each school.
  - The average reading score received by students in each grade level at each school.
  - School performance based on the budget per student.
  - School performance based on the school size.
  - School performance based on the type of school.
 
These deliverables will assist the school board in decisions regarding budget and priorities.

## Resources
- Data Source: schools_complete.csv, students_complete.csv
- Software: Jupyter notebook 6.1.4, Python 3.8.5

## Results
After the results were tabulated, an instance regarding fraudulent data was discovered.  To correct this the analysis was performed again removing the math and reading test scores for the ninth graders at Thomas High School.

### District Summary
When analyzing the results on a distirct level, removal of the test scores in question does not have a material impact.

**Original**
![district_summary](https://user-images.githubusercontent.com/85590155/125212147-a6550d00-e268-11eb-8986-16e2e7f2af1e.PNG)

**Modified**
![new_district_summary](https://user-images.githubusercontent.com/85590155/125212151-b40a9280-e268-11eb-91d3-69061e21c7f8.PNG)

The data has remained unchanged due to population size of the Thomas High School ninth graders (461) against the population size of the entire school district (39,170).

### School Summary
When analyzing the results on a school level, we can delve into the results of the top five schools based on overall passing percentage.

**Original**
![school_summary](https://user-images.githubusercontent.com/85590155/125212917-ab688b00-e26d-11eb-801a-671fb3897773.PNG)

**Modified**
![new_school_summary](https://user-images.githubusercontent.com/85590155/125212931-c1764b80-e26d-11eb-966a-34710e29b9b0.PNG)

Even with the population size of the Thomas High School ninth graders representing 28% of the total Thomas High School, removal of the ninth graders math and reading scores does not have a material effect on the analysis.  In fact, Thomas High school remains the #2 ranked school.

Furthermore, when analyzing the following categories we don't realize a material impact:

- Math and reading scores by grade
- Scores by school spending
- Scores by school size
- Scores by school type

## Summary
Changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs:

- Thomas High School '% Passing Math' decreased from 93.27% to 93.19%.
- Thomas High School '% Passing Reading' decreased from 97.31% to 97.02%
- Thomas High School '% Overall Passing decreased from 90.95% to 90.63%
- Since Thomas High School is a Charter school, the '% Overall Passing' for all Charter schools decreased from 90.43% to 90.39%.
- Since Thomas High School is designated as a medium size school, the '%Overall Passing' for all medium size schools decreased from 90.62% to 90.56%  

In summary, we are confident in the analysis to be utilized by the school board to make budget and other high priority decisions.

