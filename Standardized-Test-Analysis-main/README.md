<img src="http://imgur.com/1ZcRyrc.png" style="float: left; margin: 20px; height: 55px">

# Project 1: Standardized Test Analysis

### Name: Ahmad Khalil
### Date: 9 July 2021

### Contents:
- [Background](#Background)
- [Problem Statement](#The-Problem-Statement)
- [Data Import](#Data-Import)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Data Cleaning](#Data-Cleaning)
- [Data Visualization](#Visualize-the-Data)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)


## Background

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry. Lately, more and more schools are opting to drop the SAT/ACT requirement for their Fall 2021 applications ([*read more about this here*](https://www.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)).

## The Problem Statement

After browsing through the datasets given, SAT has lower participation rate than ACT. My objective is to provide solutions to improve participation rate for SAT.


## Data Import

Imported datasets for SAT and ACT for the years 2017-2019

## Exploratory Data Analysis

### Findings from SAT files

1. sat_2017 and sat_2018 both have 51 lines whereas sat_2019 has 53 lines

2. sat_2017 and sat_2018 both have the same column names whereas sat_2019 has a column name 'EBRW' in place of 'Evidence-Based Reading and Writing'

3. sat_2017 and sat_2018 both have the same column names whereas sat_2019 has a column name 'Participation Rate' in place of 'Participation'

4. All files have the same number of columns


### Findings from ACT files

1. act_2018 and act_2019 both have 3 columns only whereas act_2017 has 6 columns

2. All files have the same number of lines

### Import the external resource file 'State Region'

#### Source: 'https://github.com/cphalpert/census-regions/blob/master/us%20census%20bureau%20regions%20and%20divisions.csv'

## Data Cleaning

### First work on the SAT files

### Secondly work on the ACT files

### Combining the state region file with the sat_act file

## Visualize the Data

#### Plot out a figure for the participation Rate from 2017 - 2019

#### Plot a correlation figure for the states with 100% participation rate for every test per year seperately

## Insights

### Why are the students taking both tests to begin with?

1. There’s an overlap between content and strategies for the ACT and the SAT, prepping for one will help you on the other as well.
2. Most students who take both tests are applying to more selective schools.
3. Taking two tests will increase the number of test dates to choose from

More from the [source](https://blog.prepscholar.com/do-you-need-to-take-both-the-act-and-sat)

### We want to work on increasing the participation rate for SAT

1. Let's first work on seperating the regions
2. Look at which region needs to boost up participation rate
3. Look at which region to maintain participation rate
4. Any other insights will be added

### Compare the Participation Rate of SAT and ACT by region

### Findings:

- Three states particularly have high partcipation rate: Main, New Hamsphire and Rhode Island.
- Why is that so?
- Let's look at the sources:
 * [1. Rhode Island](#https://www.providencejournal.com/news/20181025/with-sat-required-ri-sees-jump-in-participation-decline-in-scores)
 * [2. Maine](#https://bangordailynews.com/2015/03/04/opinion/why-maine-should-keep-paying-for-students-to-take-the-sat/)
 * [3. New Hamsphire](#https://www.businessnhmagazine.com/article/the-shifting-role-of-the-sat-in-nh)
 
#### What does it say?


- The state makes it a requirement for college admission
- The state pays for the students taking the SAT test

## Conclusions and Recommendations

#### Based on my exploration of the data:

I started with choosing from a particular sets of datasets to work with: SAT 2017-2019 and ACT 2017-2019.

With just a general visualization I found out that there is big difference in the participation rate between both tests. Mainly the low participation rate for SAT in all of the years from 2017 - 2019. I wanted to focus my findings so I continued my research and divide the states into their own regions so I can find out each region's participation rate. After that, I found out that Midwest has the lowest rate whereas Northeast has the highest. 

So I targeted the midwest region to increase the participation rate. In finding ways to increase the rate I think it's crucial to suggest something that is proven and backed by resuts and evidence hence why I look up deeper into Northeast's states to find out the highest participation rate. So, the three states that have high participation rates are: Rhode Island, Main and New Hampshire.

Much research were done and finally I found out the reasons for the high participation rate which are:
- The state makes it a requirement for college admission
- The state pays for the students taking the SAT test

#### So my suggestion and recommendation to increase the participation rate for Midwest region by following best practices from succesful states as follows:

1. Partner with college and state to make it a requirement for admission to college
2. Help to fund students for taking the SAT tests
