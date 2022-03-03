# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1:

### Contents:
- [Overview](#Overview)
- [Data Dictionary](#Data-Dictionary)
- [Datasets](#Datasets)
- [Summary of Analysis](#Summary-of-Analysis)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)
- [Sources](#Sources)

---

### Overview

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. The test score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university. In 2017, 2.03 million high school students took the ACT([source](https://www.act.org/content/dam/act/unsecured/documents/cccr2017/CCCR_National_2017.pdf )), and 1.8 million students took the SAT([source](https://reports.collegeboard.org/archive/sat-suite-program-results/2017/overview#:~:text=The%20class%20of%202017%20is,takers%20took%20the%20new%20SAT)). The U.S. Department of Education is the agency of the federal government that establishes policies for education. By studying the relationship between participation rates and test scores, it can give recommendations on whether mandating students to participate in the ACT/SAT is beneficial in raising education standards in the country.

---

### Problem Statement

As an analyst in the United States Department of Education, I have been tasked to investigate if states that have a higher exam participation rate perform better than states with lower participation rates. If so, it would provide strong grounds for states to mandate that all students participate in the ACT/SAT.

---

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|State|Str|ACT/SAT|States of ACT/SAT data|
|act_participation_2017|float|ACT|Participation rate for 2017 ACT|
|sat_participation_2017|float|SAT|Participation rate for 2017 SAT|
|act_participation_2018|float|ACT|Participation rate for 2018 ACT|
|sat_participation_2018|float|SAT|Participation rate for 2018 SAT|
|act_composite_2017|float|ACT|Average state score for 2017 ACT, max 36|
|act_composite_2018|float|ACT|Average state score for 2018 ACT, max 36|
|sat_total_2017|float|SAT|Average state score for 2017 SAT, max 1600|
|sat_total_2018|float|SAT|Average state score for 2018 SAT, max 1600|

|Feature|Type|Dataset|Description|
|---|---|---|---|
|State|Str|Ethnic Data|States of USA|
|WhiteTotalPerc|float|Ethnic Data|Percentage of White persons by State|
|BlackTotalPerc|float|Ethnic Data|Percentage of Black persons by State|
|IndianTotalPerc|float|Ethnic Data|Percentage of Indians by State|
|AsianTotalPerc|float|Ethnic Data|Percentage of Asians by State|
|HawaiianTotalPerc|float|Ethnic Data|Percentage of Hawaiians by State|
|OtherTotalPerc|float|Ethnic Data|Percentage of persons not categorized under any of the above ethnicities|

---

### Datasets

* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`EthnicData.csv`](./data/EthnicData.csv): 2022 Ethnic Breakdown by State ([source](https://worldpopulationreview.com/states/states-by-race))
---

### Summary of Analysis

|Feature 1|Feature 2|Correlation|
|---|---|---|
|ACT/SAT Participation|ACT/SAT Score 2018|+|
|ACT/SAT Scores|ACT/SAT Participation| - |
|ACT Participation|SAT Participation| - |
|ACT Score|SAT Score| + |
|2017 Participation|2018 Participation| + |

Through our research, we also found that there is an increase in participation in the proportion of students taking SAT. This is possibly due to some states such as Colorado ([source](https://www.coloradoindependent.com/2017/07/06/from-csap-to-parcc-heres-how-colorados-standardized-tests-have-changed-and-whats-next/)) and Illinois ([source](https://www.chicagotribune.com/news/ct-illinois-chooses-sat-met-20160211-story.html)) mandating that their students should take the SAT. Moreover, we also realised that many of the underperforming states are from the South West, near the Mexican border. This prompted us to do more research on ethnicity, where we realised that states with higher Hispanic population tend to underperform for the exams. 

---

### Conclusion and Recommendations

- As there is a negative correlation between ACT/SAT scores and their respective participation rates, we cannot justify that mandating full participation of ACT/SAT for all students will lead to higher scores. This negative correlation could be caused by selection bias, as states who do not mandate or actively encourage students to take the ACT/SAT will result in only the best students choosing to sit for the exams as they know that they can score well ([source](https://blog.prepscholar.com/average-sat-and-act-scores-by-stated-adjusted-for-participation-rate)).

- The Department of Education can consider focusing their efforts in raising the education levels of the identified worst performing states, as they have the most room for improvement. This is especially so for New Mexico and Texas, which are the among the worst underperformers for both SAT and ACT. 
1. Utah
2. New Mexico
3.
4.
5.
6.
7.
8.
9.
10.

- Through closer examination of the breakdown in ethnicity, we note that states who have higher than average 'Others' ethnicity are in high risk of underperforming. Looking at state data for hispanic individuals in 2019, we can see that many underperforming states such as New Mexico, Texas, Arizona and Nevada are indeed states that have high hispanic populations [source](https://www.statista.com/statistics/259865/percentage-of-hispanic-population-in-the-us-by-state/)).Further research shows that certain states such as Texas and Illinois are not awarded equal amounts of education funding which is a significant factor as funds do play a part in raising education level [source](https://cdn.americanprogress.org/content/uploads/2018/11/08042733/LessonsLearned_SchoolFunding-report-4.pdf)). Hence, we must make sure that adequate resources are provided to people of 'Others' ethnicity, to improve the overall education level of the state.

---

### Sources
    
1. https://www.act.org/content/dam/act/unsecured/documents/cccr2017/CCCR_National_2017.pdf (ACT participation figures)
    
2. https://reports.collegeboard.org/archive/sat-suite-program-results/2017/overview#:~:text=The%20class%20of%202017%20is,takers%20took%20the%20new%20SAT (SAT participation figures)
    
3. https://worldpopulationreview.com/states/states-by-race (Breakdown by Ethnicity)
    
4. https://cdn.americanprogress.org/content/uploads/2018/11/08042733/LessonsLearned_SchoolFunding-report-4.pdf (Less funding)
   
5. https://www.statista.com/statistics/259865/percentage-of-hispanic-population-in-the-us-by-state/ (Hispanic Breakdown)
    
6. https://www.coloradoindependent.com/2017/07/06/from-csap-to-parcc-heres-how-colorados-standardized-tests-have-changed-and-whats-next/ (Colorado switch to SAT)

7. https://www.chicagotribune.com/news/ct-illinois-chooses-sat-met-20160211-story.html (Illinois switch to SAT)
    
8. https://www.alaskapublic.org/2016/07/01/alaska-changes-hs-diploma-requirements-no-more-sat-act/ (Alaska drop ACT/SAT for diploma)
    
9. https://blog.prepscholar.com/average-sat-and-act-scores-by-stated-adjusted-for-participation-rate (Selection Bias of participation rates)
