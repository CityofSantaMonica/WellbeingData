# Wellbeing Survey Data

Santa Monica's Wellbeing project has drawn from many forms of data, including a survey to see what Santa Monica residents say about themselves on various aspects of life.

* [2014 Results](2014)

## Missing data

Where someone has not responded to a question, the code `99` is used. Care should be taken in dealing with these responses, for example, if you are trying to identify an average response, or work out the percentage of valid responses that gave a particular response.

## Group representation

When carrying out analyses and comparing groups, to protect against issues of identifiability and/or representativeness, we advise caution in presenting data for any groups for which there were 20 or less respondents. There is always some randomness in who responds to a survey and how they feel when they are completing the survey, but when we have large numbers (as we do for the data set as a whole), that randomness can be expected to cancel out. For example, for everyone who is having a particularly good day, there will be someone who is having a particularly bad day. 

But when we start splitting up the population by zip code, age group, ethnicity, etc., we might find that there are certain groups for which we can’t rely on large numbers to cancel out variations. If you only have five people representing a particular group, it would be unwise to assume that they can be seen as representative of that group, for example, they could all be unusually rich for that group, or poor for that group, and therefore have different results. With our data set, for example, looking at ethnicity, it is valid to consider how Santa Monicans, who are black or African American, or Santa Monicans, who are Latino, are doing. But we would caution against drawing any conclusions for Santa Monicans who described their ethnicity as Native Hawaiian, as we only had three such respondents.

## Supporting files

These additional files describe the structure of the survey itself, as well as parts of the methodology.

### [answer-key.csv](answer-key.csv)

The key of possible answers for each of the single or multi-select survey questions.

### [variables.csv](variables.csv)

The survey questions and their mapping to variables.

### [derived-variables.csv](derived-variables.csv)

The variables that were derived from survey responses. Described below:

#### `ZIP`

1. 90401
2. 90402
3. 90403
4. 90404
5. 90405

#### `Language1`

1. Survey completed in English
2. Survey completed in Spanish

#### `Qcount`

Number of non-derived variables not having missing data

#### `Duplicate`

0. Unique identifier not duplicated
1. Unique identified was used more than once (we removed the less complete or the earlier response, so the response set here is the later more complete response)

#### `wgt`

Weighting applied to respondent. Numbers higher than 1 indicate that respondent was given higher weighting because their demographics (zip code, age and gender, and two ethnic categories – Hispanic and Asian) were under-represented in the sample. Numbers lower than 1 indicate that respondent was given lower weighting because their demographics were over-represented in the sample. Average of all weights across sample is 1.00. All analyses using the data should be carried out using this weighting variable.

#### `OtherLearningDummy`

This relates to one of the questions on courses attended by the respondent. After a set of listed options (including for example computer skills, or sports and fitness) which respondents could tick, they were given the choice to write in any other courses they attend.

0. Did not mention any other courses
1. Did mention another type of course (text deleted from this data set)

Missing value used if respondent did not answer of any of this set of questions.

#### `ClassesCount`

Count of the number of types of course respondent said they attended (including *other courses*). Sub-domain of learning dimension.

#### `Skills`

Mean of the three questions asking about skills. Sub-domain of learning dimension.

#### `Events`

Mean of the four questions asking about the ratings of different events and activities in the city.

#### `HealthFacilities`

Mean of the two questions asking about health facilities. Sub-domain of health dimension.

#### `Worries`

Mean of the three questions asking about financial concerns. Sub-domain of economy dimension.

#### `Community`

Mean of six questions asking about community engagement. Sub-domain of overall community dimension.

#### `SleepDeficit`

Derived from `HoursSleep`:

0. Sleeps 7 hours or more
1. Sleeps 6 to 7 hours
2. Sleeps 5 to 6 hours
3. Sleeps less than 5 hours

#### `IllnessCount`

Count of the number of illnesses / conditions identified by respondent.

#### `HoursWorkBins`

Derived from `HoursWork`:

1. 20 hours or less a week
2. 21 to 25 hours
3. 26 to 30 hours
4. 31 to 35 hours
5. 36 to 40 hours
6. 41 to 45 hours
7. 46 to 50 hours
8. 51 to 55 hours
9. 56 to 60 hours
10. Over 60 hours

#### `UnderWorked`

Derived from `HoursWork`:

0. Not underworked (working 26 hours or more)
1. Underworked (working 25 hours or less)

#### `OverWorked`

Derived from `HoursWork`:

0. Not overworked (working 55 hours or less)
1. Overworked (working 56 hours or more)

#### `veryworrieds`

Count of how many of the three questions asking about financial concerns to which the respondent responded *Very worried*.

#### `moderatelyworrieds`

Count of how many of the three questions asking about financial concerns to which the respondent responded *Moderately worried* or *Very worried*.

#### `PWB_Positive`

Positive emotions, sub-domain of personal wellbeing dimension. Average of the z-scores for `LifeSat` and `Happy`.

#### `PWB_Negative`

Negative emotions, sub-domain of personal wellbeing dimension. Average of the z-scores for `Sad` and `Stressed`.

#### `PWB_Flourishing`

Flourishing measures, sub-domain of personal wellbeing dimension. Average of the z-scores for `Optimistic`, `FreeDecide`, `Accomplishment`, `Worthwhile` `HaveEnergy`, and `SeldomTime`, `ThingsGoWrong`, `Lonely` (last three reversed).

#### `Social_Networks`

Sub-domain of community dimension. Average of the z-scores for `Lonely` (reversed), `MeetSocially` and `StrangersSmile`.

#### `Civic_Engagement`

Sub-domain of community dimension. Average of the z-scores for `VoluntaryCharitable`, `CanInfluence` and `TimeEffortCommunity`.

#### `Pride_in_SM`

Sub-domain of place dimension. Average of the z-scores for `MemberCommunity`, `OtherNhoods` and `Beautiful City`.

#### `Quality_Access`

Sub-domain of place dimension. Average of the z-scores for `HouseSat`, `OutDoors`, `CommunityPublicSpaces`, `HasBusinesses` and `Noise` (reversed)

#### `Learning_Access`

Sub-domain of learning dimension. Average of the z-scores for `Events`, `OverWorked` (reversed) and `WorkLifeBalance`.

#### `Health_Behaviour`

Sub-domain of health dimension. Average of the z-scores for `PhysicalActivity`, `FruitVegetables`, `HourSleepOver9` (reversed) and `SleepDeficit` (reversed)

#### `DOM_CommunityOverall`

Community dimension. Average of `Social_Networks`, `Civic_Engagement` and z-score of `Community`.

#### `DOM_Place`

Place dimension. Weighted average of `Pride_in_SM` (x3), `Quality_Access` (x2) and z-score of `Drive` (reversed, x1).

#### `DOM_Learning`

Learning dimension. Average of `Learning_Access`, z-score of `Skills`, and z-score of `ClassesCount`.

#### `DOM_HealthOverall`

Health dimension. Average of `Health_Behaviour`, z-score of `HealthFacilities` and z-score of `Health`.

#### `DOM_Economy`

Economy dimension. Average of z-scores of `Worries`, `JobSat`, `Borrow` and `ChildrenStay`.

#### `DOM_PWB`

Personal wellbeing (or outlook) dimension. Average of `PWB_Positive`, `PWB_Negative` (reversed) and `PWB_Flourishing`

#### `OVERALL`

Overall SM Index score. Average of `DOM_CommunityOverall`, `DOM_Place`, `DOM_Learning`, `DOM_HealthOverall`, `DOM_Economy`, `DOM_PWB`.
