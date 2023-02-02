# Race and Wage: What can you do to earn more?

Repository for collaborative R project completed for academic purposes at the University of Toronto.


_This project was completed using ‘wage’ dataset was from the An Introduction to Statistical Learning with applications in R 2nd ed. and was assembled by Steve Miller of Inquidia Consulting on behalf of the US Census Bureau for the Supplement to Current Population Survey._

## Introduction & Background

- As of 2021, individuals of Caucasian descent were found to represent 63% of the population living in the Mid-Atlantic region (Middle Atlantic Race & Ethnicity, 2018, n.d). 
- A 2019 statistics report on the wealth gap by states has furthered identified New York, West Virginia, and New Jersey of the Mid-Atlantic region to be among the top states with the greatest income disparity (Gap between Rich and Poor by State U.S. 2021, n.d.). 

- **Thus, given this disproportionate distribution of races and income gap, this highlighted a need to look at such factors with respect to each race independently in determining what decisions an individual can make in maximizing their earning capacity with respect to their educational attainment, health, and marital status, based on historical trends.**

- We also note that this disproportionate distribution of racial groups is also reflected in the dataset with majority of the samples being white males representing an estimated 83% of the sample (see Table 1; Figure 1).

<p align="center">
<img width="733" alt="Screen Shot 2023-02-01 at 5 45 37 PM" src="https://user-images.githubusercontent.com/106416383/216181733-dbf4e159-e207-434e-8f40-9f3022d15f96.png">
</p>


## Summary of Methodology

### Part 1: Variable Selection
The present study focuses on three independent measures of wage. These factors were selected on the basis that a working individual could work towards, and thus, have reasonable control over with respect to wage at the beginning of their respective careers:

**1. Educational Attainment**
- There has been an observed positive association between level of education and one’s earning capacity at “different stages of [one’s career] and over a lifetime” (Tamborini et al., 2015, n.d.). 

**2. Marital Status**
- Existing literature have also reported an association between wages and the marital status of men (Antonovics et al., 2004; Stratton., 2002). 
- This income differential has been coined the “male marriage wage premium” ranging from 10 – 50% where studies have reported that characteristics valued by a partner is also valued by an employer. 

**3. Health Status**
- Employers have also been found to discriminate in favour of those who appear in good health with respect to higher wage outcome, such that one’s marginal productivity is often perceived to be reflected by their health status (Hsieha et al., 2012). 

The present study will not look at factors with respect to an individual’s age, job class, or health insurance. That is, an individual cannot control for their biological age. Furthermore, job class and health insurance are deemed to be a product of an individual’s employment, whereas the current study aims to look at factors prior to such.

### Part 2: Data Analysis

This study presents two analyses:
1. Exploratory Data Analysis (EDA): To describe and characterize the proportion of samples in each class of a category, and summary statistics of continuous variables with respect to age, wage, log wage, and year (Table 1. Descriptive Statistics).

2. Inferential Statistics: One-way ANOVA[^1] followed by post-hoc Tukey HSD test[^2]


## Summary of Tukey Results

[PDF of Tukey Results Table](https://github.com/tlieva/Implication_of_Race_on_Male_Wages/blob/8acc134be01f2817dcc5445ca05289e0d14e44bd/Tukey_Results.pdf)



1. **Wages vary by race:** Based on historical trends from 2003 to 2009, the mid-atlantic region have experienced an overall net upward trend in wage among the working Male. However, if we look at this with respect to race, this increase in wages was not universal for all the racial subgroups (Figure 3). This finding further validates our decision to subset the data into racial subgroups.

<p align="center">
<img width="322" alt="Screen Shot 2023-02-01 at 6 28 47 PM" src="https://user-images.githubusercontent.com/106416383/216190888-5315c4a3-26da-4e8f-9458-a49ea6c2e704.png">
</p>

2. **Higher education suggests higher wages for all racial subgroups:** For the racial subgroups of White, Black, and Asian, there was a correlation between higher level of education and higher wage. This suggests that regardless of your race it is best to get a higher level of education if you want to increase your wage.

3. **Marital status can impact wage depending on race:** White and black married men were found to have statistically significant higher wages. This observed relatinship may be attribute to the aforementioned findings in exisitng literature with respect to the "male marriage wage premium". This is further corroborated in the observed general decrease in wages with respect to males who were divorced or never married. However, it’s possible that people who have higher wages are more desirable as partners and therefore more likely to be married. The causal relationship cannot be discerned with the aforementioned tests. No signfiicant findings were found with respect to Asian males; however, this may be due to the small sample size and bias in the sample tow married men.

4. **Good health suggests higher wages depending on race:** Better health was found to be correlated with higher wages across all racial groups, with exception of Black males, which otherwise suggests that Black males should focus on other factors with respect to an individual's educational attainment and marital status to increase attractiveness in the job market.



## References

Antonovics, Kate, and Robert Town. 2004. "Are All the Good Men Married? Uncovering the Sources of the Marital Wage Premium." American Economic Review, 94 (2): 317-321.

Gap between rich and poor by state U.S. 2021. (n.d.). Statista. Retrieved October 14, 2022, from
https://www.statista.com/statistics/227249/greatest-gap-between-rich-and-poor-by-us-state/

Hsieha, W., Hsiaob, P., & Leec, J. (2012). The Impact of Health Status on Wages – Evidence from the Quantile Regression. Journal of International and Global Economic Studies, 5(1), 35-56.

Race and ethnicity in Middle Atlantic (division). The Demographic Statistical Atlas of the United States - Statistical Atlas. (n.d.). Retrieved December 10, 2022, from https://statisticalatlas.com/division/Middle-Atlantic/Race-and-Ethnicity

Stratton L. Examining the wage differential for married and cohabiting men. Economic Inquiry. 2002; 40:199–212.

Tamborini, C. R., Kim, C., & Sakamoto, A. (2015). Education and Lifetime Earnings in the United States. Demography, 52(4), 1383–1407. https://doi.org/10.1007/s13524-015-0407-0

U.S. Bureau of Labor Statistics. (n.d.). Education pays, 2021 : Career Outlook. U.S. Bureau of Labor Statistics. Retrieved December 11, 2022, from https://www.bls.gov/careeroutlook/2022/data-on- display/education-pays.htm




[^1]: _**Use of One-way ANOVA**_: one-way ANOVA was conducted in determining whether significant differences exist in the average wages between classes within each aforementioned independent variable (education, marital status, and health status). This allows for the comparison of a continuous dependent measure across multiple classes of an independent categorical variable. This test was repeated for each independent variable of interest with respect to each race: White, Black, and Asian. ‘Other’ was excluded due to its significantly small sample size (see Table 1)

[^2]: _**Post-Hoc Tukey HSD**_: Due to the nature of ANOVA, a post-hoc test was conducted within each racial subset to identify where exactly the wage differentials lie with respect to each factor, should significance be identified. The Tukey Honest Significant Difference (HSD) test was selected to compare the means of different classes within each independent variable of interest for each race subset. Results of such analysis will allow us to answer our question of which features in the dataset have a significant impact in maximizing the earning capacity of an individual given their race. 
