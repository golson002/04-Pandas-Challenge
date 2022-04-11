# PyCitySchools Pandas Exercise

## **Motivation/Reason for Analysis:**

The motivation for the analysis of the school and student data sets in the PyCitySchools exercise was to assess proficiency with Pandas and to understand my ability to take large data sets, merge them based on shared data, turn the merged data set into smaller, more pointed DataFrames, and finally group/parse those DataFrames to effectively summarize and display trends in the data.

In this exercise, I assume the postion/perspective of the Chief Data Scientist for the PyCity school district with the intention of helping the school board and mayor make strategic decisions regarding future school budgets and priorities. Using the district-wide standardized test results and information on every student's math and reading scores and the schools they attend, my goal was to parse the data to showcase obvious trends in school performance. The performance trends will then inform the board's decisions on school budgets and priorities moving forward.

## **Appproach:**

My first step in performing the analysis for the PyCity school district was to preview the two data sets I was given, understand the data I had, then merge the data sets based on a shared column to create one workable data set. 

After creating the larger data set, I performed a District Summary analysis using several Pandas functions, df.loc, and DataFrames. The analysis gives a high-level snapshot of the district and outputs a DataFrame with key district metrics including: total schools, total students, total budget, average student math and reading scores, and the percentage of students passing individual subjects and overall. 

Next, I took a more granular look at the data and analyzed key metrics at each school to produce a School Summary. Here, I leveraged Pandas functions, grouby objects, conditional statements, DataSeries, dictionaries, and DataFrames to output a single DataFrame with each school's key metrics (total students, total budget, per student budget, average math and reading score, and percentage of students passing individual subjects and overall).

With the School Summary DataFrame created above, I then performed an analysis to display the top 5 performing schools and the bottom 5 performing schools using the .sort_values function.

My next level of granularity was to look at student performance at each school by grade. To do so, I created two separate DataFrames--one for math scores and one for reading scores-- using df.loc and groupby objects to create DataSeries for each grade then adding those DataSeries to a single DataFrame using a dictionary. 

Finally, I looked at school performance by school spending, school size, and school type. Using binning, groupby objects, df.loc and DataFrames, the program outputs three spearate DataFrames for each independent variable comparison to the dependent variable- school performance. 

## **Observable Trends:**

* Trend #1: Higher school spending on a per student basis does not guarantee students at the school will perform better on standardized tests. In fact, my analysis shows that the top performing schools tend to spend less on a per student basis than the bottom performing schools. Perhaps this trend implies there are other priorities that need to be highlighted/emphasized to increase student performance on standardized tests at low performing schools other than increasing spending/budgets. 

* Trend #2: Students at both small schools (<1000 students) and medium schools (1,000-2,0000 students) tend to perform better on standardized tests than students at large schools (>2,000 students). This trend reinforces the observation above that perhps spending more will not increase student performance. Further, with this trend, we may infer that because students at small-medium size schools get more 1:1 tutoring/attention, they are able to perform better on tests. Of course we would need more data/further anaylsis to test this hypothesis, but a similar conclusion would inform the board that the teacher-student ratio at larger school needs improvement. 

* Trend #3 Students at charter schools tend to perform better on standardized tests than students at district schools-- the top five performing schools are all charter schools while the bottom five performing schools are all district schools. Charter schools tend to be smaller than district schools, which then reinforces the observation above that students at smaller schools perform better than students at larger schools. In a further analysis of this dataset, it would be interesting to compare school size to school type to confirm the relationship between the two and then be confident in targeting our budget/priorities at district schools.

## **Takeaways/Lessons Learned:**

* Reusing the output of a line of code or analysis as the input for another function, method, analysis, etc. is incredibly valuable and one of the foundational elements of programming I tried to leverage and remind myself of as I completed this exercise. Not only does it make our lives as coders/programmers much easier, but it makes our code more readable, intuitive, and less busy.

* Similar to Python, there is a steep learning curve to the Pandas syntax but learning how to read and research the documentation has been a valubale lesson learned from the PyCity schools exercise. The authors of Pandas wrote the documentation for users to leverage, not to feel shameful for using, as it is impractical to think users would know every function, method, object, etc. 
