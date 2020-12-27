# Exis_Surveys
Clean and Analyze Employee Exit Surveys

### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)
6. [CRISP-DM process](#CRISP-DM)

## Installation <a name="installation"></a>

There should be no necessary libraries to run the code here beyond the Anaconda distribution of Python.  The code should run with no issues using Python versions 3.*.

## Project Motivation<a name="motivation"></a>

For this project, I was interestested to work with exit surveys from employees of the Department of Education, Training and Employment (DETE) and the Technical and Further Education (TAFE) institute in Queensland, Australia, to understand:

1. Are employees who only worked for the institutes for a short period of time resigning due to some kind of dissatisfaction? What about employees who have been there longer?
2. Are younger employees resigning due to some kind of dissatisfaction? What about older employees?



## File Descriptions <a name="files"></a>

There is 1 notebooks available here with work related to the above questions. The notebook is exploratory in searching through the data pertaining to the questions showcased by the notebook title.  Markdown cells were used to assist in walking through the thought process for individual steps.  

## Results<a name="results"></a>

From the initial analysis above, we can tentatively conclude that employees with 7 or more years of service are more likely to resign due to some kind of dissatisfaction with the job than employees with less than 7 years of service. However, we need to handle the rest of the missing data to finalize our analysis.
As we can see from the chart for 2007 and 2008 there is no data. The year with the highest number of resignations is in 2012 followed by 2013. And with the least resignations are the years 2006 and 2009..

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Must give credit to [Department of Education, Training and Employment (DETE)](https://en.wikipedia.org/wiki/Department_of_Education_and_Training_(Queensland)) and the Technical and Further Education (TAFE) institute.  You can find the Licensing for the data [here](https://data.gov.au/dataset/ds-qld-89970a3b-182b-41ea-aea2-6f9f17b5907e/details?q=exit%20survey) and [here](https://data.gov.au/dataset/ds-qld-fe96ff30-d157-4a81-851d-215f2a0fe26d/details?q=exit%20survey).  Otherwise, feel free to use the code here as you would like! 

## CRISP-DM process <a name="CRISP-DM"></a>

1. Business Understanding

Are employees who only worked for the institutes for a short period of time resigning due to some kind of dissatisfaction? What about employees who have been there longer?

Are younger employees resigning due to some kind of dissatisfaction? What about older employees?? 
2. Data Understanding

Here we used the Department of Education, Training and Employment (DETE) and the Technical and Further Education (TAFE) institute data to attempt to answer our questions of interest. In this case, using the data to help us arrive at our questions of interest. We combined the results for both surveys to answer these questions. However, although both used the same survey template, one of them customized some of the answers. 
This is a preview of a couple of columns we'll work with from the dete_survey.csv:

ID: An id used to identify the participant of the survey

SeparationType: The reason why the person's employment ended

Cease Date: The year or month the person's employment ended

DETE Start Date: The year the person began employment with the DETE

Below is a preview of a couple of columns we'll work with from the tafe_survey.csv:

Record ID: An id used to identify the participant of the survey

Reason for ceasing employment: The reason why the person's employment ended

LengthofServiceOverall. Overall Length of Service at Institute (in years): The length of the person's employment (in years)


3. Prepare Data

Here we are at the stage where we need to prepare our data to answer our questions. We have replaced the Not stated and - values with Nan values, and drop all the unnecessary columns from doth data frames, to have more clean data frames. We have changed columns names from uppercase to lower, remove whitespace from the end of the strings, replace space with _ and rename columns name from tafe_survey_updated. This will help us to work with ease on both data frames. We have cleaned the date columns in both data frames. We have added a new column, we have noticed that the tafe_resignations data frame already contains a "service" column, which we renamed to institute_service. To analyze both surveys together, we'll have to create a corresponding institute_service column in dete_resignations. And finally combined our datasets.

4. Model Data

We were finally able to see the cleaned data and answer our questions.

5. Results

From the initial analysis above, we can tentatively conclude that employees with 7 or more years of service are more likely to resign due to some kind of dissatisfaction with the job than employees with less than 7 years of service. However, we need to handle the rest of the missing data to finalize our analysis.
As we can see from the chart for 2007 and 2008 there is no data. The year with the highest number of resignations is in 2012 followed by 2013. And with the least resignations are the years 2006 and 2009.
