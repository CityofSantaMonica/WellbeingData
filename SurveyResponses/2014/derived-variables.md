# Derived Variables

> Provides a description of the variables that were *derived* from survey submissions.

## `ZIP`

1. 90401
2. 90402
3. 90403
4. 90404
5. 90405

## `Language1`

1. Survey completed in English
2. Survey completed in Spanish

## `Qcount`

Number of non-derived variables not having missing data

## `Duplicate`

0. Unique identifier not duplicated
1. Unique identified was used more than once (we removed the less complete or the earlier response, so the response set here is the later more complete response)

## `wgt`

Weighting applied to respondent. Numbers higher than 1 indicate that respondent was given higher weighting because their demographics (zip code, age and gender, and two ethnic categories – Hispanic and Asian) were under-represented in the sample. Numbers lower than 1 indicate that respondent was given lower weighting because their demographics were over-represented in the sample. Average of all weights across sample is 1.00. All analyses using the data should be carried out using this weighting variable.

## `OtherLearningDummy`

This relates to one of the questions on courses attended by the respondent (columns AG to AM in the data set). After a set of listed options (including for example computer skills, or sports and fitness) which respondents could tick, they were given the choice to write in any other courses they attend.

0. Did not mention any other courses
1. Did mention another type of course (text deleted from this data set)

Missing value used if respondent did not answer of any of this set of questions.

## `ClassesCount`

Count of the number of types of course respondent said they attended (including *other courses*). Based on columns AG to AM and CZ. Sub-domain of learning dimension.

**Composite Method:** Count

## `Skills`

Mean of the three questions asking about skills (columns AO to AQ). Sub-domain of learning dimension.

## `Events`

Mean of the four questions asking about the ratings of different events and activities in the city (columns BC to BF).

## `HealthFacilities`

Mean of the two questions asking about health facilities (columns BK & BL). Sub-domain of health dimension.

## `Worries`

Mean of the three questions asking about financial concerns (columns BN to BP). Sub-domain of economy dimension.

## `Community`

Mean of six questions asking about community engagement (columns AT to AY). Sub-domain of overall community dimension.

## `SleepDeficit`

Recoded from original variable `HoursSleep` (column X)

0. Sleeps 7 hours or more
1. Sleeps 6 to 7 hours
2. Sleeps 5 to 6 hours
3. Sleeps less than 5 hours

## `IllnessCount`

Count of the number of illnesses / conditions identified by respondent (columns CG to CL)

## `HoursWorkBins`

Derived from `HoursWork` (column AR)

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

## `UnderWorked`

Derived from `HoursWork` (column AR)

0. Not underworked (working 26 hours or more)
1. Underworked (working 25 hours or less)

## `OverWorked`

Derived from `HoursWork` (column AR)

0. Not overworked (working 55 hours or less)
1. Overworked (working 56 hours or more)

## `veryworrieds`

Count of how many of the three questions asking about financial concerns (columns BN to BP) to which the respondent responded *Very worried*

## `moderatelyworrieds`

Count of how many of the three questions asking about financial concerns (columns BN to BP) to which the respondent responded *Moderately worried* or *Very worried*

## `PWB_Positive`

Positive emotions, sub-domain of personal wellbeing dimension. Average of the z-scores (standardised scores) for `LifeSat` (column A) and `Happy` (column H)

## `PWB_Negative`

Negative emotions, sub-domain of personal wellbeing dimension. Average of the z-scores (standardised scores) for `Sad` (column I) and `Stressed` (column J)

## `PWB_Flourishing`

Flourishing measures, sub-domain of personal wellbeing dimension. Average of the z-scores (standardised scores) for `Optimistic`, `FreeDecide`, `Accomplishment`, `Worthwhile` `HaveEnergy`, and `SeldomTime`, `ThingsGoWrong`, `Lonely` (last three reversed) (column B to G, and K to L)

## `Social_Networks`

Sub-domain of community dimension. Average of the z-scores (standardised scores) for `Lonely` (reversed, column L), `MeetSocially` (column P) and `StrangersSmile` (column BB)

## `Civic_Engagement`

Sub-domain of community dimension. Average of the z-scores (standardised scores) for `VoluntaryCharitable` (column Q), `CanInfluence` (column BG) and `TimeEffortCommunity` (column BH)

## `Pride_in_SM`

Sub-domain of place dimension. Average of the z-scores (standardised scores) for `MemberCommunity` (column BM), `OtherNhoods` (column BA) and `Beautiful City` (column BI)

## `Quality_Access`

Sub-domain of place dimension. Average of the z-scores (standardised scores) for `HouseSat` (column O), `OutDoors` (column R), `CommunityPublicSpaces` (column S), `HasBusinesses` (column BJ) and `Noise` (reversed, column AZ)

## `Learning_Access`

Sub-domain of learning dimension. Average of the z-scores (standardised scores) for `Events` (column DC), `OverWorked` (column DK, reversed) and `WorkLifeBalance` (column AS)

## `Health_Behaviour`

Sub-domain of health dimension. Average of the z-scores (standardised scores) for `PhysicalActivity` (column T), `FruitVegetables` (column W), `HourSleepOver9` (reversed, based on column X) and `SleepDeficit` (reversed, column DG)

## `DOM_CommunityOverall`

Community dimension. Average of `Social_Networks` (column DQ), `Civic_Engagement` (column DR) and z-score (standardised score) of `Community` (column DF).

## `DOM_Place`

Place dimension. Weighted average of `Pride_in_SM` (column DS, x3), `Quality_Access` (column DT, x2) and z-score (standardised score) of `Drive` (reversed, column Y, x1).

## `DOM_Learning`

Learning dimension. Average of `Learning_Access` (column DU), z-score (standardised score) of `Skills` (column DB), and z-score (standardised score) of `ClassesCount` (column DA).

## `DOM_HealthOverall`

Health dimension. Average of `Health_Behaviour` (column DV), z-score (standardised score) of `HealthFacilities` (column DD) and z-score (standardised score) of `Health` (column M)

## `DOM_Economy`

Economy dimension. Average of z-scores (standardised scores) of `Worries` (column DE), `JobSat` (column N), `Borrow` (column AX) and `ChildrenStay` (column BQ)

## `DOM_PWB`

Personal wellbeing (or outlook) dimension. Average of `PWB_Positive` (column DN), `PWB_Negative` (reversed, column DO) and `PWB_Flourishing` (column DP)

## `OVERALL`

Overall SM Index score. Average of `DOM_CommunityOverall`, `DOM_Place`, `DOM_Learning`, `DOM_HealthOverall`, `DOM_Economy`, `DOM_PWB` (columns DW to EB).
