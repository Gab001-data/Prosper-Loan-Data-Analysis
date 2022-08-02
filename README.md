## Prosper Loan Data Analysis
The objective of this analysis project is to demonstrate the importance of data visualizations techniques (exploratory and explanatory) in the data analysis process in identifying patterns/trends, cleaning task and communicating findings to others. For this analysis we used the Loan data from Prosper. The dataset contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others. The goal of this analysis is to determine features that affect the borrower’s APR or interest rate with focus on ProsperScores(risk measure).
click [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv) to access the Prosper loan data. also this [dictionary](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0) explains all of the features/variables available in the dataset.

## Dependencies
It is highly recommended that you use the [Anaconda distribution](https://www.anaconda.com/products/distribution) to install Python, since the distribution includes all necessary Python libraries as well as Jupyter Notebooks. The following libraries are expected to be used in this project:
```
- NumPy
- pandas
- Matplotlib
- Seaborn

```

Check the [Jupyter Notebook](https://github.com/Gab001-data/Prosper-Loan-Data-Analysis/blob/master/Part_I_exploration_template.ipynb) for a workthrough of the analytical process implemented in this project which include.

1. Import Libraries
2. Data acquision and import into pandas dataframe
3. Data assessement
4. Data cleaning
5. Exploratory visualization/analysis
6. Explanatory visualization
7. Slide deck creation.

## Pair-wise Relationship between variables of Interest
![variables pair-wise relationship](https://github.com/Gab001-data/Prosper-Loan-Data-Analysis/blob/master/pair-wise-relationship.png)

The borrowers interest rate shows a strong negative relationship with ProsperScore and CreditScoreRangeLower variables as expected (since they indicate risk). Interest rate also has a negative correlation to LoanOriginalAmount albert not so strong since the LoanOriginalAmount is distributed over large intervals.

There is also a moderate positive correlation between ProsperScore and CreditScoreRangeLower. the loan term does not have a strong correlation with any of the other numeric variables as such I won't be performing any further exploration/investigation on this variable.

## BorrowerRate vs ProsperScore for Levels of ProsperRatings
![rate-prosperscore for ProsperRating encoding](https://github.com/Gab001-data/Prosper-Loan-Data-Analysis/blob/master/intRatevsPscore_for_ProsperRating.png)

We see a clear interaction of the ProsperRating with the relationship between BorrowerRate and ProsperScore. For a given ProsperScore the BorrowerRate (interest rate) declines with increasing Prosper rating. from the plot, higher ratings of A, AA have very low interest rate of about 10%

## Summary/Insights

From our exploration of the ProsperLoan dataset, here are a few insights we derived;

The BorrowerRate/interest rate shows a strong negative relationship with ProsperScore and CreditScoreRangeLower variables. this is expected since ProsperScore and CreditScoreRangeLower measures risk/probality of the loan going bad or past the due date. Interest rate also has a negative correlation to LoanOriginalAmount albert not so strong. although this was not explored expensively in this analysis.

In exploring the relationship between our variable of interest (BorrowerRate) and other categorical variable we see a steady decline in BorrowersRate for increased ProsperRating which also has a strong positive correlation with ProsperScore.

Interestingly, Loan collected for student use (ListingCategory 5) has one of the highest median BorrowerRate for all loan categories despite having the highest median ProsperScore. this is absurd since we have establish a strong negative relationship between BorrowersRate and ProsperScore. and may be due to fact they are unsecured loan without tangible assets backing (collaterals).

individual with earnings above 50k receive the least BorrowersRate for all income ranges (evident by the movement of the dark color to lower left in the heatmap for IncomeRange upward of $50k).

finally, out of job individuals recorded the hightest median BorrowersRate across all available employment statuses. They have the least median ProsperScore alongside self employed individuals and people with no specified employement status.

__It is important to note that these insights are tentative and not exhaustive since we only explored a few of the features available in the dataset. Also we didn't consider loan data prior to july 2009 in our analysis due to unavailability of ProsperScores.__

## Relevant Links

- [Jupyter Notebook](https://github.com/Gab001-data/Prosper-Loan-Data-Analysis/blob/master/Part_I_exploration_template.ipynb)
- [Linkedln](https://www.linkedin.com/in/gabriel-ogih-609a091a1/)
- [Twitter](https://twitter.com/dev_gabby)
- [Medium Article]()
