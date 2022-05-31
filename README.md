## Problem Statement

A university's bottom line metric is revenue, primarily dictated by tuition. This project aims to use SAT and ACT data to find the optimal target demographics so that universities can reevaluate the targeting in their marketing strategies, thus resulting in maximizing revenues.

## Background

This project operates under a few assumptions for the analysis to be valid. The first (1) assumption that this project operates under is that the largest revenue stream for a for-profit private university is tuition ([source](https://nces.ed.gov/programs/coe/indicator/cud#:~:text=The%20primary2%20sources%20of,and%20appropriations%3B%20and%20auxiliary%20enterprises.)). We can approach tuition in one of two ways: we can either-

1. Maintain a higher-priced tuition with a smaller student body, or
2. Maintain a lower-priced tuition with a higher student body.

I am going to focus on the latter option: maintaining a lower-priced tuition with a higher student body, as down the line, the school has a wider pool of students to reach out to for donations post-graduation. To have a higher student body, a school would need a high number of applicants on an annual basis, and those applicants will likely need to be 'high-quality' applicants so that post-graduation, they will have more disposable income to allocate towards donations to their alma mater.

Assumption 2: High SAT scores and high ACT scores are an indicator of high-quality students that will likely have more disposable income to allocate towards donations to their alma mater post-graduation.

Assumption 3: SAT and ACT participation is an indicator of interest in applying to colleges. This assumption can help a school target the right demographics when developing a marketing strategy.

Assumption 4: It will be a more effective use of marketing spend to target students that demonstrate interest in applying to colleges than those who don't.

## Datasets I am using:

1. act_2019.csv: the most recent ACT scores and participation rates grouped by state.
2. sat_2019.csv: the most recent SAT scores and participation rates grouped by state.
3. sat_2019_by_intended_college_major.csv: contains the amount of students that took the SAT in 2019, their scores, and their intended majors.

## Outside Research

In 2018 and 2019, the largest source of revenue for for-profit private educational institutions was tuition at 91%. ([source](https://nces.ed.gov/programs/coe/indicator/cud#:~:text=The%20primary2%20sources%20of,and%20appropriations%3B%20and%20auxiliary%20enterprises.))

There are 13 states that require that all students take the ACT, ([source](https://blog.prepscholar.com/which-states-require-the-act-full-list-and-advice)) and some states also required that students take the SAT in 2019. ([source](https://blog.collegevine.com/states-that-require-sat/))

## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*object*|SAT/ACT Data 2019|U.S. State|
|**participation_sat**|*float*|SAT/ACT Data 2019|Participation rate in the SAT, percentage as decimal (e.g. 10% == 0.10)|
|**scores_sat**|*int*|SAT/ACT Data 2019|Average score of the SAT by state (Out of 1600 points)|
|**participation_act**|*float*|SAT/ACT Data 2019|Participation rate in the ACT, percentage as decimal (e.g. 10% == 0.10)|
|**scores_act**|*int*|SAT/ACT Data 2019|Average score of the ACT by state (Out of 36 points)|

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**intended_major**|*object*|SAT Scores by Intended Major Data 2019|Students' intended major|
|**pct_participation**|*float*|SAT Scores by Intended Major Data 2019|Participation rate in the SAT, percentage as decimal (e.g. 10% == 0.10)|
|**scores**|*int*|SAT Scores by Intended Major Data 2019|Average score of the SAT by intended major (Out of 1600 points)|

**Visual assets, graphs, and charts can be found in the assets folder or the presentation file in this repo.**

## Conclusions and Recommendations

The goal of this project is to find the geographical and psychographical (intended major) areas to focus on targeting for a university's marketing strategy. This targeting focus is designed to increase revenue through the primary source of tuition and the secondary source of alumni donations. Increasing these revenue streams requires a high number of student applications (as we are measuring by SAT/ACT participation percentage) from high-quality students (as we are measuring by scores). From this data we can see that the states with the highest participation rates and scores include:

- Maine,
- New Hampshire,
- Maryland,
- New Jersey,
- Massachusetts,
- Minnesota,
- Missouri, and
- South Dakota,

indicating that these are the states where marketing investment should be prioritized.

To target high-quality students that have a higher likelihood of incomes with the most disposable income for alma mater donations post-graduation, the following programs should be advertised the most in those states:

- Biological and Biomedical Sciences,
- Business, Management, Marketing, and Related Studies, and
- Engineering

These are majors that typically lead to higher incomes relative to other majors (such as art and theatre), and these are also the intended majors that have the highest SAT participation rates, and have the higher than average SAT scores, suggesting that these are high-quality students.

To address any target demographic and state population concerns, this target demographic **should not** be the only demographic or psychographic that a school targets. However, these groups of students should be taken into consideration when developing a marketing strategy or incorporated into an existing marketing strategy.

If a private for-profit university wants to maximize revenue through tuition and post-graduate donations, while optimizing marketing spend, the above classifications should be included and prioritized in the target demographic and incorporated into the existing marketing strategy.