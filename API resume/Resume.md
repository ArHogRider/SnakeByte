# Notes on the files
## Job_search_API
1. This program uses and API to find jobs based on a keyword search and returns a list of job postings.  Then it does a comparison between the job posting and the resume.  It vectorizes both and does a cosine similarity (between 0-1)test between the two to see how similar they are. The higher the number, the more similar the two are.  
2. It compiles the job opening list and ranks from highest to lowest based on the similarity test and includes a link to the job posting and exports it out to an excel spreadsheet.
3. The user can then make notes on the spreadsheet if they apply for the position or not.  
4. The program and be rerun to add new postings and notes on made by the user on if they applied will not be lost on the spreadsheet.

## Top Job Keyword
1. This programs uses the same API as in Job_search_API, but instead of returning job postings, it returns the top keywords from the search.  
2. Each job posting has a TF-IDF vectorization performed on it and the resulting score for each word is added to a dataframe. 
3. The TF-IDF score is averaged together for all the words from the job postings and then ranked based off the average score.
4. A TF-IDF is then completed on the resume and added to the same dataframe.
5. This will show any matching words found in both and what there score is to see if the resume has the correct keywords.
6. A excel spreadsheet is exported to see the results.

 Uses Pandas version 1.2.4
 Uses SciKit-Learn version 0.24.1
