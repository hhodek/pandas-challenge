# Pandas Challenge

# Description
- The objective of the PyCity Schools Analysis was to work with school data and standardized testing data in order to identify relationships and relevant information that would assist the school board and the Mayor in making strategic decisions regarding future school budgets and priorities.

- The initial analysis focused on the district summary, which provided information such as the total budget, average scores, and total number of students for all schools in the district.

- Next, a school summary analysis was conducted, which presented similar results to the district summary but calculated them for each individual school.

- For the analyses on the highest and lowest-performing schools, the top and bottom five schools were separately displayed by sorting the values in ascending and descending order. It was noteworthy to observe that Charter schools comprised the top five performing schools, while District schools accounted for the bottom five.

- Following that, analyses on Math and Reading Scores by Grade were performed. In these analyses, the average math, reading, and overall scores were calculated for each grade, while organizing them by school.

- For the analyses on Scores by School Size and Spending, calculations were conducted and bins were created to include a new column with the findings. The information displayed in these dataframes was similar to that in the Per School Summary dataframe, but with additional information incorporated.

- The final analysis, Scores by School Type, involved further calculations to display the average score and the percentage of students passing math, reading, and overall for each school type- Charter vs District.


# Directory Structure
The "PyCitySchool" directory contains the following files and folders:

1. "Resource" folder: This folder contains two CSV files that were used for the data analysis.
2. "PyCitySchools_starter.ipynb" file: This file contains the code, dataframes, and results of all the analyses conducted.
3. "Written_Analysis_PyCitySchools" Word file: This file includes the summary and conclusion of the analysis.


# Notes
- In the School Summary analysis, one of the tasks involved selecting all of the school types. Initially, the code was written to extract the types as a NumPy array, which later caused a hurdle when conducting the Scores by School Type analysis. The issue arose because NumPy arrays are not hashable. To address this without modifying the previous code, a workaround was implemented. A list comprehension was added to extract the first element from each inner array, creating a list of school types. This modified list was then used for the GroupBy operation instead of the original school type array.

# Credits
1. Most of the code was derived from class materials/activities

2. Referenced the following for help with GroupBys
    - https://sparkbyexamples.com/pandas/pandas-groupby-count-examples/
    - https://sparkbyexamples.com/pandas/pandas-groupby-sort-within-groups/

3. Also referenced the following for help with ds file 
    - https://gist.github.com/lohenyumnam/2b127b9c3d1435dc12a33613c44e6308

4. ChatGPT was utilized to edit formatting and grammer of Readme/Written Analysis and provide tips and explanations for code, specifically in the Score by Spending Analysis I used ".str.replace('[^\d.]','', regex = True).astype(float)" which came from ChatGPT - (2023). ChatGPT (Version GPT-3.5) 
    - https://chat.openai.com/chat
