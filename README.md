# problem_with_standardized_testing
*exploring the way SAT and the ACT are designed to keep underprivileged students from receiving a higher education*

***Pegah Mirghafari***
___

## WHY?!

Many research and studies have found that the SAT and the ACT are designed in a way to keep the underprivilaged students from reciving a higher education. Having information on pverty, SAT and ACT scores and participation, I decided to further explore the situation.
___

## Index:
- [Good Reads](#Good-Reads)
- [Data Dictionary](#Data-Dictionary)
- [Preprocessing](#Preprocessing)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Conclusion](#Conclusion)

___

## Good Reads:
<br/>
- [Historically low ACT scores ‘a red flag for our country’](https://www.daytondailynews.com/news/historically-low-act-scores-red-flag-for-our-country/djfx9Urp719WyEaMfykyxL/)
- [These four charts show how the SAT favors rich, educated families](https://www.washingtonpost.com/news/wonk/wp/2014/03/05/these-four-charts-show-how-the-sat-favors-the-rich-educated-families/) 
___

## Data Dictionary:
<br/>
Data gathered are from 
- [SAT](https://ipsr.ku.edu/ksdata/ksah/education/6ed16.pdf)
- [ACT 2017](https://www.act.org/content/dam/act/unsecured/documents/cccr2017/ACT_2017-Average_Scores_by_State.pdf)
- [ACT 2018](https://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf)
- [Poverty Census Data](https://www.census.gov/data/tables/2019/demo/income-poverty/p60-266.html)

||Feature|Type|Dataset|Description|
|---|---|---|---|
|State|string|All|One of 50 States + Washington, D.C.| 
|sat_partic_17|float|SAT '17|% of students participating in the SAT in 2017|
|sat_read_write_17|float|SAT '17|SAT Reading and Writing Score, 2017|
|sat_math_17|float|SAT '17|SAT Math Score, 2017|
|sat_total_17|float|SAT '17|SAT Total Score, 2017|
|act_partic_17|float|ACT '17|% of students participating in the ACT in 2017|
|act_eng_17|float|ACT '17|ACT English Score, 2017|
|act_math_17|float|ACT '17|ACT Math Score, 2017|
|act_read_17|float|ACT '17|ACT Reading Score, 2017|
|act_sci_17|float|ACT '17|ACT Science Score, 2017|
|act_composite_17|float|ACT '17|ACT Composite Score, 2017|
|sat_partic_18|float|SAT '18|% of students participating in the SAT in 2018|
|sat_read_write_18|float|SAT '18|SAT Reading and Writing Score, 2018|
|sat_math_18|float|SAT '18|SAT Math Score, 2018|
|sat_total_18|float|SAT '18|SAT Total Score, 2018|
|act_partic_18|float|ACT '18|% of students participating in the ACT in 2018|
|act_composite_18|float|ACT '18|ACT Composite Score, 2018|
|poverty|float|Census Poverty|% of people living in poverty, 2017-2018 average|
|total_partic_17|float|Generated Feature|Sum of sat_partic_17 and act_partic_17|
|total_partic_18|float|Generated Feature|Sum of sat_partic_18 and act_partic_18|
|poverty_above_median|bool|Generated Feature|True if poverty index is below national median|

<br/> 
___
## Preprocessing
<br/> There were quite a bit of mistakes in the data that had to be fixed by referring to the original datasets. 
Furthermore, I had to combine all the datasets to create a comprehensive data frame to analyze. 
you can find that in [this notebook]()

<br/> 
___

## Exploratory Data Analysis

<br/> 

there is an indepth data analysis of the dataset in [this notebook]() 
<br/> 


## Conclusion 
<br/> 

After extensively exploring this data, our key takeaways are as follows:
- When investigating SAT and ACT scores at the state level, it is critical to compare 'apples to apples,' i.e. high-participation states to other high-participation states.
- State-level SAT and ACT scores both have demonstrable connection to state-level poverty. This connection is still evident if we take a deeper dive into a state's demographic score breakdown and poverty distributions.

SAT and ACT scores shouldn’t be considered objective without factoring in family wealth on an individual level, or poverty and race on an aggregate level.

We recommend cheaper access to test prep and equitable school funding to help equalize the US college admissions process, and that efforts should continue to eliminate unintentional biases in SAT and ACT questions and formats.

We further recommend statistical modeling to put numbers to the patterns and effects we have been able to observe through visualizations.
