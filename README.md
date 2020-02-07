# Freddie Mac Single Family Loan Classification Project

## Summary: 
Using data collected at the start of the loan, I predict whether a loan will go default. At 75% recall, my model cut false positive rate almost by half compared to the strict credit score cutoff approach. This project is published in Towards Data Science on medium:  [Link](https://towardsdatascience.com/predicting-bad-housing-loans-using-public-freddie-mac-data-a-tutorial-on-working-with-imbalanced-d2852c003996).

## Aim
To predict whether a loan is good or bad using data collected when the loan is originated.

## Dataset
Single Family Loan-Level dataset downloaded from Freddie Mac's [website](http://www.freddiemac.com/research/datasets/sf_loanlevel_dataset.page)
Year range: 1999-2003
Only completed/terminated loans are used. A good loan is a loan that has been fully paid-off; a bad loan is a loan that was terminated by other reasons. Raw data is a stored in sqlite database.

## Preprocessing
 1. map values from letter to numeric values in true vs false columns
 2. clear NaN fields
 3. label encode catagorial fields

## Exploratory Data Analysis
Distribution of Credit Score by Loan Outcome

## Under-sampling
Subsample majority class (good loans) to match minority class (bad loans).
## Over-sampling
Resample minority class (bad loans) to match majority class (good loans).

## Classifiers for Balanced Data
1. Gradient Boosting Classifier
2. Random Forest Classifier
3. SGD Classfier (Logistic Classifier)
4. Hard Voting Classifier of all of the above
5. Light GBM

## Isolation Forest
Can we solve this problem with anamoly detection algorithm?

## Classifiers for Imbalanced Data
1. Balanced Bagging Classifier
2. Balanced Random Forest Classifier
3. Easy Ensemble Classifier
4. Voting Classifier
5. Light GBM

## Compared to Credit Score Cutoff
How does it fare compared to status quo?
