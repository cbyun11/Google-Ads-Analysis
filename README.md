# Google Ads Performance Analysis using Python

I wrote this file to help me analyze Google Ads performance.

There are four functions:
1) fill_missing_date: This function fills in missing dates with all 0s. This was necessary because reports downloaded from Google Ads omit any dates that recorded all 0s in metrics (0 impression).
2) split_data: This function splits data based into current and previous period to prepare for statistical significance tests.
3) sig_test: This function runs significance tests. If the sample size of current and previous periods are both larger than 30, based on the Central Limit Theorem, I assume a normal distribution and run t-tests. Otherwise, I run a Shapiro-Wilk test to determine normality. If the test rejects normality, it then runs either a Wilcoxon or Mann-Whitney U test, depending on the lengths of current and previous periods.
4) prop_test: This function is to run Z-tests to compare either the CTR or CVR of current and previous periods.
