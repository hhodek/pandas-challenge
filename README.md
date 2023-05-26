# Pandas Challenge

# Description
The goal of the PyCity Schools Analysis was to work with school data and standardized testing data to find relationships and pertinent information that aid the school board and Mayor in making strategic decisions regarding future school budgets and priorities.
 
Our first analysis was the district summary, the results from that summary displayed information such as; total budget, average scores, and total students, from all schools in the district.
 
Next was the school summary, in this analysis similar results to the district summary are displayed, only it's calculated for each school instead. 
 
For the Highest and Lowest-Performing School analyses, the top and bottom 5 schools were separately displayed by by sorting values in ascending/descending order. It was interesting to see that Charter schools make up the top 5 performing schools and District schools make up the bottom 5.
 
The next analyses were Math and Reading Scores by Grade, for these analyses we did some calculations to find the average math/reading/overall score for each grade- while keeping it categorized by school.
 
For the Scores by School Size/Spending analyses, we did some calculations and binning to add a new column with the findings. The information displayed on these dataframes was similar to the Per School Summary data frame, just with some new info added in.
 
The final analysis, Scores by School Type, included more calculations to display the average score and percent passing math/reading/overall for each school type. 


# Directory Structure
In the "PyCitySchool" directory, you will find the following:

1. A "Resource" folder: this holds the 2 CSV files that were read in
2. A "PyCitySchools_starter.ipynb" file: this holds the code, dataframes, & results from all the analyses
3. A "Written_Analysis_PyCitySchools" Word File: this holds the analysis summary and conclusion


# Notes
For the School Summary analysis, the first task was to write a code that selects all of the school types. I did that, however, not in the most effective way which created a hurdle once I got to the Scores by School Type analysis. I originally extracted the type as a NumPy array which is not hashable. To make the values hashable without going back, I ended up adding code to extract the first element from each inner array using a list comprehension, which I then used to GroupBy instead of the original school type.

# Credits
1. Most of the code was derived from class materials/activities

2. Referenced the following for help with GroupBys
    - https://sparkbyexamples.com/pandas/pandas-groupby-count-examples/
    - https://sparkbyexamples.com/pandas/pandas-groupby-sort-within-groups/

3. Also referenced the following for help with ds file 
    - https://gist.github.com/lohenyumnam/2b127b9c3d1435dc12a33613c44e6308

4. Used ChatGPT to edit formatting and grammer of Readme and provide tips and explanations for code, specifically in the Score by Spending Analysis I used ".str.replace('[^\d.]','', regex = True).astype(float)" which came from ChatGPT - (2023). ChatGPT (Version GPT-3.5) 
    - https://chat.openai.com/chat