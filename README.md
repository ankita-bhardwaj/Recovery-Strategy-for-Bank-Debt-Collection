# which debts are worth banks efforts?

# Background:
For retrieving the debts back, bank first calculates an expected recovery amount.
This recovery amount is actually calculated on a lot of factors such as probability of the customer paying, the total debt, and other factors that a bank finds relevant.
Based on this amount, they form recovery strategies such that they invest more as the recovery amount keeps on increasing.

There are various levels of recovery strategy and each level is decided by a certain threshold. 
For instance, level 0 is for the expected recovery amount $0 to $1000, level 1 is from $1000 to $2000 and so on. 
With an increase in level, the cost incurred by the bank also increases (by $50 per level)

# Objective:
In this project, the objective is to find out if the recovery in higher levels is able to recover the costs that the bank has incurred.
i.e. recovery startegy is the one that causes change in the actual amount above and below the threshold and the change is more than its cost.

# Steps:
- Check if age ranges remain the same above and below the threshold (ideally it should)
- Check if sex propertions remain the same above and below the threshold (ideally it should)
- Check if actual recovery amount depends on the expected recovery amounts (ideally it should)
- Check if the recovery strategy impacts the actual recovery amount (ideally it should)
- Fit linear regression models on the features that impacts the actual recovery amount and check the p value and coefficients

# Results:
- Age and sex proportions remain the same irrespective of the strategy which shows that for the thresholds created, they are the same in every group.
- Actual recovery amount is dependent on the expected recovery amount.
- Recovery strategy heavily impacts the actual recovery amount.
- The coefficient of recovery strategy in a linear regression model ,with it and expected recovery amount being the independent variables, is way more than 50.
- Hence, the recovery startegy is actually profitable
