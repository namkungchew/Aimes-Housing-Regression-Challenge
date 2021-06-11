# Project 1 : Recommending to College Board on the efficient way to improve SAT Participation Rate

## Table of Contents
- [Executive Summary](#Exective-Summary)
- [2017 Data Import & Cleaning](#2017-Data-Import-and-Cleaning)
- [2018 Data Import and Cleaning](#2018-Data-Import-and-Cleaning)
- [Data Dictionary](#Data-Dictionry)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Data Visualization](#Visualize-the-data)
- [Additional Plots](#Additional-Plots)
- [Descriptive and Inferential Statistics](#Descriptive-and-Inferential-Statistics)
- [Outside Research](#Outside-Research)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)
- [References and Data Sources](#References-and-Data-Sources)


## Executive Summary

This report provides an analysis and evaluation of the factors that affect SAT (and its biggest competitor ACT) Participation Rate during 2017 and 2018 in the United States. It also seek to track the effect of the new format for the SAT released in Mar 2016 in increasing SAT Participation Rate and recommends where money is best spend to further improve it. In the report, we investigate similarities and differences in SAT and ACT through participation rate, scores data Our findings shows that SAT and ACT are certainly in direct competition for market share. There are 2 main populations who will take the tests. First population will take the either of these 2 tests to use it as part of their college application requirements. This population will only take the tests if they will they can do well in it and if they intended to apply for college. The second population took the test as to fulfill the federal requirement for 'No Child Left Behind' for high school students. This is a bigger population which the first population is a subset of as all students not just the ones that intend to go to college have to take. The new format have been effective in helping SAT established itself as meeting the requirement as a test for the second population and helped the College Board to successfully win new contracts with the education administration of the states of Colorada, Illinois, Rhodes Island etc to make it as the go to test for the federal requirement in that state. We recommend that the College Board continue with this strategy as it have been very effective in increasing particpation in SAT and that to target Tennessee next.

---
### Data Dictionary

|Feature|Type|Dataset|Description|
|:--|:-:|:-:|:--|
|**state**|*object*|ACT/SAT|One of the 50 states of United States of America|
|**sat17_par**|*integer*|SAT 2017|Participation rate in SAT in year 2017| 
|**sat17_essay**|*integer*|SAT 2017|Scores of Evidence-Based Reading and Writing section in SAT'17| 
|**sat17_math**|*integer*|SAT 2017|Scores of Math section in SAT'17| 
|**sat17_total**|*integer*|SAT 2017|Total Score of SAT'17| 
|**act17_par**|*integer*|ACT 2017|Participation rate in ACT in year 2017| 
|**act17_eng**|*float*|ACT 2017|Scores of English section in ACT'17| 
|**act17_math**|*float*|ACT 2017|Scores of Math section in ACT'17| 
|**act17_read**|*float*|ACT 2017|Scores of Reading section in ACT'17| 
|**act17_sci**|*float*|ACT 2017|Scores of Science section in ACT'17| 
|**act17_comp**|*float*|ACT 2017|Composite Average Score of the 4 sections ACT'17| 
|**sat18_par**|*integer*|SAT 2018|Participation rate in SAT in year 2018| 
|**sat18_essay**|*integer*|SAT 2018|Scores of Evidence-Based Reading and Writing section in SAT'18| 
|**sat18_math**|*integer*|SAT 2018|Scores of Math section in SAT'18| 
|**sat18_total**|*integer*|SAT 2018|Total Score of SAT'18| 
|**act18_par**|*integer*|ACT 2018|Participation rate in ACT in year 2018| 
|**act18_eng**|*float*|ACT 2018|Scores of English section in ACT'18| 
|**act18_math**|*float*|ACT 2018|Scores of Math section in ACT'18| 
|**act18_read**|*float*|ACT 2018|Scores of Reading section in ACT'18| 
|**act18_sci**|*float*|ACT 2018|Scores of Science section in ACT'18| 
|**act18_comp**|*float*|ACT 2018|Composite Average Score of the 4 sections ACT'18| 

---
## Conclusion

- SAT and ACT are in direct competition for market share
- SAT and ACT tests have 2 uses
    - To fulfill college entrance requirements
    - To fulfill federal requirement of 'No child left behind'
- Taking the test for college entrance requirement is personal and voluntary, as such students will only take a test if they know they can do well in it and if they need the test to go college.
- For the federal requirement, states' education administration need to fulfill this requirement and thus made taking the SAT or ACT mandatory for all student in the state, even the students who do not make the grade to go college will have to take the test thus pulling down the average score
- There is not much differences in the score distribution of the 2 test. A student cannot expect to be higher in the distribution of 1 test than the other
- Both tests do not give surprises to the student so a student can generally expect to do well if he do well in mock test based on previous year questions.
- Might not be the most effective to compete with ACT using scores given the similarities between the 2 tests. Also college might adjust the benchmarking
- When given a choice, e.g. in Ohio, ACT is more likely to be chosen
- Efforts by the College Board with states contracts from the Colorado, Illinois, Rhodes Island resulted in a big increase of SAT participation from single digit participation to 100%
- Giving free / subsidized testing have mixed results in increasing participation rate

---
## Recommendation

- To maximize use of resources, recommended to increase SAT participation by focusing on making it the test states to use to fulfill federal requirement
- As there is a trend of more colleges are dispensing with SAT or ACT test as compulsory for college entrance requirement, the population to use SAT for college entrance is in the danger of shrinking over time
- Its use as a test for the federal requirement is more long term and also the population catchment is much larger
- State education still need a mandatory test for the federal requirement for ‘No Child Left Behind’. Better it be SAT than other test
- Furthermore, the College Board have tried and tested successful in states like Colorado and Illinois
- There are still many states with low participation so the return per resource we put in would be the greatest
- Out of these low participation states, Iowa, Missouri, South Dakota, Minnesota, Arkansas, Kansas, Tennessee, Oklahoma do not have arrangement with ACT and is up for grabs
- We recommend to target Tennessee followed by Missouri at the moment since these 2 states have a larger population than the other states in the above list

---
