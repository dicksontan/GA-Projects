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

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university. In 2017, 2.03 million high school students took the ACT([source](https://www.act.org/content/dam/act/unsecured/documents/cccr2017/CCCR_National_2017.pdf )), and 1.8 million students took the SAT([source](https://reports.collegeboard.org/archive/sat-suite-program-results/2017/overview#:~:text=The%20class%20of%202017%20is,takers%20took%20the%20new%20SAT)). The U.S. Department of Education is the agency of the federal government that establishes policies for education. By studying the relationship between participation rates and test scores, it can give recommendations on whether mandating students to participate in ACT/SAT is beneficial in raising education standards in the country.

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

---

### Datasets

* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`EthnicData.csv`](./data/sat_2018.csv): 2022 Ethnic Breakdown by State ([source](https://worldpopulationreview.com/states/states-by-race))
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

### Conclusions and Recommendations


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
