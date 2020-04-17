# py_city_schools

The task is to help the  school board and mayor make strategic decisions regarding future school budgets and priorities by analyzing the district-wide standardized test results. My responsibility is to aggregate the data to and showcase obvious trends in school performance.

## Data
A set of data for each school in the district called [schools_complete.csv](py_city_schools/Resources/schools_complete.csv), which is composed of five columns: `School ID`, `school_name`, `type`, and `budget`.
And a set of data for each stucent in the district called [sstudents_complete.csv](py_city_schools/Resources/students_complete.csv), which is composed of seven columns: `Student ID`, `student_name`, `gender`, `grade`, `school_name`, `reading_score` and `math_score`.
The passing score is 70 or greater for both the math and reading exams.

## Steps Taken
* Read the .csv files into Pandas data frames `school_data` and `student_data`, then joined them on `school_name` to create a third data frame `school_data_complete` which is the same as `student_data` but with the columns from `school_data` that correspond to each student's respective school.
* From `school_data_complete`, created another data frame `distSum` which is a high level snapshot of the district's key metrics: `Total Schools`,  `Total Students`, `Total Budget`, `Average Math Score`, `Average Reading Score`, `% Passing Math`, `% Passing Reading`, and `Overall Passing Rate`.
* Created a data frame `topSchGrp`that summarizes key metrics about each school: `School Name`, `School Type`, `Total Students`, `Total School Budget`, `Per Student Budget`, `Average Math Score`, `Average Reading Score`, `% Passing Math`, `% Passing Reading`, `Overall Passing Rate`.
