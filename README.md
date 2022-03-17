# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2: Predicting Housing Prices with Linear Regression

### Contents:
- [Problem Statement](#Problem-Statement)
- [Datasets](#Datasets)
- [Data Dictionary](#Data-Dictionary)
- [Summary of Analysis](#Summary-of-Analysis)
- [Conclusion and Recommendations](#Conclusion-and-Recommendations)
- [Sources](#Sources)

### Problem Statement
The problem that I would like to tackle in this project is: 

* What are the features of a property that sellers should look out for in order to sell their houses at a higher price in Ames?

Conversely, this will also be useful for buyers who might be looking to resell their house.

Based on this problem statement, I will create a linear predictive model using using Linear, Lasso, Ridge or ElasticNet regression to investigate and identify the features which have a strong positive or negative relationship with housing sale prices.

### Datasets

The dataset used for this project is based off the greater region of Ames, Iowa. It is collected from 2006 to 2010 by the Ames Assessor's Office. 

## Data Dictionary

|Feature|Format|Type|Description|
|---|---|---|---|
|**Id**|*integer*|Nominal|Identifier for each property.|
|**PID**|*integer*|Nominal|Parcel identification number - can be used with city web site for parcel review.|
|**MS SubClass**|*integer*|Nominal|Identifies the type of dwelling involved in the sale.| 
|**MS Zoning**|*string*|Nominal|Identifies the general zoning classification of the sale.| 
|**Lot Frontage**|*float*|Continuous|Linear feet of street connected to property.| 
|**Lot Area**|*integer*|Continuous|Lot size in square feet.|
|**Street**|*string*|Nominal|Type of road access to property.|
|**Alley**|*string*|Nominal|Type of alley access to property.| 
|**Lot Shape**|*string*|Ordinal|General shape of property.|
|**Land Contour**|*string*|Nominal|Flatness of the property.| 
|**Utilities**|*string*|Ordinal|Type of utilities available.| 
|**Lot Config**|*string*|Nominal|Lot configuration.|
|**Land Slope**|*string*|Ordinal|Slope of property.| 
|**Neighborhood**|*string*|Nominal|Physical locations within Ames city limits.| 
|**Condition 1**|*string*|Nominal|Proximity to various conditions.|
|**Condition 2**|*string*|Nominal|Proximity to various conditions.|
|**Bldg Type**|*string*|Nominal|Type of dwelling.|
|**House Style**|*string*|Nominal|Style of dwelling.|
|**Overall Qual**|*integer*|Ordinal|Rates the overall material and finish of the house.|
|**Overall Cond**|*integer*|Ordinal|Rates the overall condition of the house| 
|**Year Built**|*integer*|Discrete|Original construction date| 
|**Year Remod/Add**|*integer*|Discrete|Remodel date (same as construction date if no remodeling or additions)|
|**Roof Style**|*string*|Nominal|Type of roof|
|**Roof Matl**|*string*|Nominal|Roof material| 
|**Exterior 1**|*string*|Nominal|Exterior covering on house| 
|**Exterior 2**|*string*|Nominal|Exterior covering on house|
|**Mas Vnr Type**|*string*|Nominal|Masonry veneer type|
|**Mas Vnr Area**|*float*|Continuous|Masonry veneer area in square feet| 
|**Exter Qual**|*string*|Ordinal|Evaluates the quality of the material on the exterior| 
|**Exter Cond**|*string*|Ordinal|Evaluates the present condition of the material on the exterior| |**Foundation**|*string*|Nominal|Type of foundation| 
|**Bsmt Qual**|*string*|Ordinal|Evaluates the height of the basement|
|**Bsmt Cond**|*string*|Ordinal|Evaluates the general condition of the basement| 
|**Bsmt Exposure**|*string*|Ordinal|Refers to walkout or garden level walls| 
|**BsmtFin Type 1**|*string*|Ordinal|Rating of basement finished area| 
|**BsmtFin SF 1**|*float*|Continuous|Type 1 finished square feet|
|**BsmtFinType 2**|*string*|Ordinal|Rating of basement finished area (if multiple types)|
|**BsmtFin SF 2**|*float*|Ordinal|Type 2 finished square feet| 
|**Bsmt Unf SF**|*float*|Continuous|Unfinished square feet of basement area| 
|**Total Bsmt SF**|*float*|Continuous|Total square feet of basement area|
|**Heating**|*string*|Nominal|Type of heating|
|**HeatingQC**|*string*|Ordinal|Heating quality and condition|
|**Central Air**|*string*|Nominal|Central air conditioning| 
|**Electrical**|*string*|Ordinal|Electrical system| 
|**1st Flr SF**|*integer*|Continuous|First Floor square feet|
|**2nd Flr SF**|*integer*|Continuous|Second floor square feet|
|**Low Qual Fin SF**|*integer*|Continuous|Low quality finished square feet (all floors)| 
|**Gr Liv Area**|*integer*|Continuous|Above grade (ground) living area square feet| 
|**Bsmt Full Bath**|*float*|Discrete|Basement full bathrooms| 
|**Bsmt Half Bath**|*float*|Discrete|Basement half bathrooms| 
|**Full Bath**|*integer*|Discrete|Full bathrooms above grade|
|**Half Bath**|*integer*|Discrete|Half baths above grade| 
|**Bedroom AbvGr**|*integer*|Discrete|Bedrooms above grade (does NOT include basement bedrooms)|
|**Kitchen AbvGr**|*integer*|Discrete|Kitchens above grade| 
|**KitchenQual**|*string*|Ordinal|Kitchen quality|
|**TotRmsAbvGrd**|*integer*|Discrete|Total rooms above grade (does not include bathrooms)| |**Functional**|*string*|Ordinal|Home functionality (Assume typical unless deductions are warranted)| |**Fireplaces**|*integer*|Discrete|Number of fireplaces| 
|**FireplaceQu**|*string*|Ordinal|Fireplace quality| 
|**Garage Type**|*string*|Nominal|Garage location|
|**Garage Yr Blt**|*float*|Discrete|Year garage was built| 
|**Garage Finish**|*string*|Ordinal|Interior finish of the garage| 
|**Garage Cars**|*float*|Discrete|Size of garage in car capacity| 
|**Garage Area**|*float*|Continuous|Size of garage in square feet| 
|**Garage Qual**|*string*|Ordinal|Garage quality| 
|**Garage Cond**|*string*|Ordinal|Garage condition| 
|**Paved Drive**|*string*|Ordinal|Paved driveway| 
|**Wood Deck SF**|*integer*|Continuous|Wood deck area in square feet| 
|**Open Porch SF**|*integer*|Continuous|Open porch area in square feet| 
|**Enclosed Porch**|*integer*|Continuous|Enclosed porch area in square feet| 
|**3-Ssn Porch**|*integer*|Continuous|Three season porch area in square feet| 
|**Screen Porch**|*integer*|Continuous|Screen porch area in square feet| 
|**Pool Area**|*integer*|Continuous|Pool area in square feet| 
|**Pool QC**|*string*|Ordinal|Pool quality|
|**Fence**|*string*|Ordinal|Fence quality| 
|**Misc Feature**|*string*|Nominal|Miscellaneous feature not covered in other categories| 
|**Misc Val**|*integer*|Continuous|Dollar value of miscellaneous feature| 
|**Mo Sold**|*integer*|Discrete|Month sold (MM)|
|**Yr Sold**|*integer*|Discrete|Year sold (YYYY)| 
|**Sale Type**|*string*|Nominal|Type of sale| 
|**SalePrice**|*integer*|Continuous|Sale price of houses|

A comprehensive data dictionary describing the features is also included in the link below:

[Data Dictionary](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt)

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
    1. New Mexico
    2. Texas
    3. Utah
    4. West Virginia
    5. Illinois
    6. Hawaii
    7. OKlahoma
    8. Alaska
    9. Arizona
    10. Nevada

- Through closer examination of the breakdown in ethnicity, we note that states who have higher than average 'Others' ethnicity are in high risk of underperforming. Looking at state data for hispanic individuals in 2019, we can see that many underperforming states such as New Mexico, Texas, Arizona and Nevada are indeed states that have high hispanic populations ([source](https://www.statista.com/statistics/259865/percentage-of-hispanic-population-in-the-us-by-state/)).Further research shows that certain states such as Texas and Illinois are not awarded equal amounts of education funding which is a significant factor as funds do play a part in raising education level ([source](https://cdn.americanprogress.org/content/uploads/2018/11/08042733/LessonsLearned_SchoolFunding-report-4.pdf)). Hence, we must make sure that adequate resources are provided to people of 'Others' ethnicity, to improve the overall education level of the state.

---

### Sources
    

1. https://www.cityofames.org/government/departments-divisions-i-z/public-works/alley-maintenance

   Summary: Government website summarising alley length where we infer that many houses probably will not have alleys.
   
2. https://www.census.gov/construction/chars/
    
   Summary: Goverment data which shows number of houses that own fireplaces broken down by year. From 2006-2010, about 40% of houses do not have fireplaces.
   
3. https://statisticalatlas.com/neighborhood/Iowa/Ames/Stone-Brooke/Household-Income

   Summary: The source displays graphs that show how Stone Brook had a higher household income at each percentile as compared to the general Ames population.
   
4. https://www.weichert.com/search/community/neighborhood.aspx?hood=60290

   Summary: The article displayed graphs which show that 75% of the workforce in NorthRidge Heights were white collar jobs, indicating higher wealth.
   
5. https://www.99.co/singapore/insider/factors-affecting-resale-value/

   Summary: We see that age, condition, size and location all play a part in housing valuation.


6. https://www.thebalance.com/pricing-houses-to-sell-1798968
   
   Summary: Perceptions of desirability causes neighborhoods to have a relationship with house prices. Wealthier neighborhoods allows for one to flaunt their status. Age of the house is also crucial


7. https://www.compmort.com/home-location-and-property-value/

   Summary: This article highlights the importance of neighborhoods and proximity to amenities like schools and hospitals.
   

8. https://www.investopedia.com/articles/mortages-real-estate/11/factors-affecting-real-estate-market.asp
   
   Summary: This article highlights how government policies/subsidies and economic factors like inflation and supply/demand have a relationship with house prices.
