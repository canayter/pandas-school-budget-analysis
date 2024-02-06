**Background**

You are the new Chief Data Scientist for your city's school district. In this capacity, you'll be helping the school board and mayor make strategic decisions regarding future school budgets and priorities. As a first task, you've been asked to analyze the district-wide standardized test results. You'll be given access to every student's math and reading scores, as well as various information on the schools they attend. Your task is to aggregate the data to showcase obvious trends in school performance.

**Content**

Using Pandas and Jupyter Notebook, create a report that includes the following data. Your report must include a written description of at least two observable trends based on the data. Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.Include the following: 
- Total number of unique schools
- Total students
- Total budget
- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)

Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school. Include the following:
- School name
- School type
- Total students
- Total school budget
- Per student budget
- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)

Sort the schools by % Overall Passing in descending order and display the top 5 rows. Save the results in a DataFrame called "top_schools".
Sort the schools by % Overall Passing in ascending order and display the top 5 rows. Save the results in a DataFrame called "bottom_schools".
Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.
Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.
Create a table that breaks down school performance based on average spending ranges (per student). Use the code provided below to create four bins with reasonable cutoff values to group school spending:
> spending_bins = [0, 585, 630, 645, 680]
> labels = ["<$585", "$585-630", "$630-645", "$645-680"]

Use pd.cut to categorize spending based on the bins.
Use the following code to then calculate mean scores per spending range:
> spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Math Score"].mean()
> spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Reading Score"].mean()
> spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Math"].mean()
> spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Reading"].mean()
> overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Overall Passing"].mean()
Use the scores above to create a DataFrame called spending_summary.

Include the following metrics in the table:
- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)
- Scores by School Size

Use the following code to bin the per_school_summary:
> size_bins = [0, 1000, 2000, 5000]
> labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]
Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.
Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).
Use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.
This new DataFrame should show school performance based on the "School Type".

**Conclusions**
- It appears charter schools show greater performance compared to district schools in a variety of ways.
- Higher spending (per student) doesn't result in higher test scores.
- Large schools don't seem to have better grades compared to smaller schools.
- Higher spending budget per student shows lower performance rates.
