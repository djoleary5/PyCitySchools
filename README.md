# py_city_schools

The task is to help the  school board and mayor make strategic decisions regarding future school budgets and priorities by analyzing the district-wide standardized test results. My responsibility is to aggregate the data to and showcase obvious trends in school performance.

## Data
A set of data for each school in the district called [schools_complete.csv](py_city_schools/Resources/schools_complete.csv), which is composed of five columns: `School ID`, `school_name`, `type`, and `budget`.
And a set of data for each stucent in the district called [sstudents_complete.csv](py_city_schools/Resources/students_complete.csv), which is composed of seven columns: `Student ID`, `student_name`, `gender`, `grade`, `school_name`, `reading_score` and `math_score`.
The passing score is 70 or greater for both the math and reading exams.

## Steps Taken
* Read the .csv files into Pandas data frames `school_data` and `student_data`, then joined them on `school_name` to create a third data frame `school_data_complete` which is the same as `student_data` but with the columns from `school_data` that correspond to each student's respective school.
* From `school_data_complete`, created another data frame `distSum` which is a high level snapshot of the district's key metrics: `Total Schools`,  `Total Students`, `Total Budget`, `Average Math Score`, `Average Reading Score`, `% Passing Math`, `% Passing Reading`, and `Overall Passing Rate`.
* Created a data frame `topSchGrp`that summarizes key metrics about each school: `School Name`, `School Type`, `Total Students`, `Total School Budget`, `Per Student Budget`, `Average Math Score`, `Average Reading Score`, `% Passing Math`, `% Passing Reading`, `Overall Passing Rate`. Sorted by `Overall Passing Rate` (ascending and decending) to find the top and bottom five performing schools.
* Created data frames `mathScores` and `readScores` that list the average math and average reading scores for studends of each grade level (9th-12th) at each school.
* Created data frames 
 `spendBins` that breaks down school performances based on average Spending Ranges (Per Student), using bins to group school spending, 
  `sizeBins`, that breaks down school performance but with schools grouped into three bins based on school size (small, medium, large), 
  `typeBins`, that breaks down school performance but with schools grouped by tyoe (charter vs. district).
  Included in all these tables are each of the following: `Average Math Score`, `Average Reading Score`, `% Passing Math`, `% Passing Reading`, `Overall Passing Rate`.
  
 ## Observations
* The most telling data is observed when groupig the average scores and passing rates by school type, per-student budget, and school size(total students).
* Schools with higher per-student budgets did not yeild higher test scores.  More analysis is required as to the reason for this.  It is possible that students with special needs would require a higher budget and would not necessarily score higher on standardized tests.
* Small and medium size schools produced similar test scores and large schools (over 2000 students) were significantly lower.
* Charter schools test scores were significantly higher than district schools.  This is to be expected as many times charter schools are able to cherry-pick the best students from the district.
