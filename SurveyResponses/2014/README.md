# 2014 Wellbeing Survey Data

## Identifying respondents for inclusion

We received 3,182 unique responses (i.e., not duplicates). Then, there were 542 people who only completed 20 questions or less, so these were removed from the analysis (reducing the respondent number to 2,640). Another 319 were not residing currently in Santa Monica, and were therefore removed as well. This left the sample to 2,321 respondents, of which 2,238 completed all the questions on demographics (i.e. age, gender, zip code and ethnicity). Our analysis included this final dataset of 2,238 respondents.

## Missing data

Where someone has not responded to a question, the code 99 is used. Care should be taken in dealing with these responses, for example, if you are trying to identify an average response, or work out the percentage of valid responses that gave a particular response.

## Note on cell sizes

When carrying out analyses and comparing groups, to protect against issues of identifiability and/or representativeness, we advise caution in presenting data for any groups for which there were 20 or less respondents. There is always some randomness in who responds to a survey and how they feel when they are completing the survey, but when we have large numbers (as we do for the data set as a whole), that randomness can be expected to cancel out. For example, for everyone who is having a particularly good day, there will be someone who is having a particularly bad day. 

But when we start splitting up the population by zip code, age group, ethnicity, etc., we might find that there are certain groups for which we can’t rely on large numbers to cancel out variations. If you only have five people representing a particular group, it would be unwise to assume that they can be seen as representative of that group, for example, they could all be unusually rich for that group, or poor for that group, and therefore have different results. With our data set, for example, looking at ethnicity, it is valid to consider how Santa Monicans, who are black or African American, or Santa Monicans, who are Latino, are doing. But we would caution against drawing any conclusions for Santa Monicans who described their ethnicity as Native Hawaiian, as we only had three such respondents.

## Files in this directory

### [codebook.xlsx](codebook.xlsx)

Breakdown of all possible choices for each survey question as well details of derived variables.

### [derived-variables.md](derived-variables.md)

Description of the variables that were derived from survey responses.

### [open-ended-responses.csv](open-ended-responses.csv)

Open-ended (free text) survey question responses.

**Important Notes**:

1. Some content has been removed to guard against identifiability. Any removed content is denoted with `[XXX]`.
2. While all comments have been assigned at least one category and sub-category, not all codes have been assigned to every code relevant to its content.

### [survey-responses.csv](survey-responses.csv)

Single or multi-choice survey question responses.