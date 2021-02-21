## HR Analytics

**NOTE :**  Dataset and problem statement has been collected by [Analytics Vidhya](https://datahack.analyticsvidhya.com/contest/wns-analytics-hackathon-2018-1/).

Extensive EDA on this dataset has been done using Matplotlib and Seaborn. 2 models have been created : Random Forest and XG Boost. Random Forest gave a much better F1 score (for training and test dataset, and also for the unseen dataset (public score) submitted for the hackathon), which is also the evaluation metric for this competition. 

### Files:
1. train.csv - Training Dataset
2. test.csv - Unseen Test Dataset
3. sample_submission.csv - Sample Submission File for the submission format
3. submission_rf.csv - Submission CSV File with Random Forest to AnalyticsVidhya
4. submission_xgb.csv - Submission CSV File with XG Boost to AnalyticsVidhya


### Problem Statement
Your client is a large MNC and they have 9 broad verticals across the organisation. One of the problem your client is facing is around identifying the right people for promotion (only for manager position and below) and prepare them in time. Currently the process, they are following is:

1. They first identify a set of employees based on recommendations/ past performance
2. Selected employees go through the separate training and evaluation program for each vertical. These programs are based on the required skill of each vertical
3. At the end of the program, based on various factors such as training performance, KPI completion (only employees with KPIs completed greater than 60% are considered) etc., employee gets promotion

For above mentioned process, the final promotions are only announced after the evaluation and this leads to delay in transition to their new roles. Hence, company needs your help in identifying the eligible candidates at a particular checkpoint so that they can expedite the entire promotion cycle.

![Image](https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2018/09/wns_hack_im_1.jpg)

They have provided multiple attributes around Employee's past and current performance along with demographics. Now, The task is to predict whether a potential promotee at checkpoint in the test set will be promoted or not after the evaluation process.

------

## Dataset Description

| Variable  | Definition   |
|---|---|
| employee_id | Unique ID for employee |
| department | Department of employee |
| region | Region of employment (unordered) |
| education | Education Level |
| gender | 	Gender of Employee |
| recruitment_channel | Channel of recruitment for employee |
| no_of_trainings | no of other trainings completed in previous year on soft skills, technical skills etc.|
| age | Age of Employee |
| previous_year_rating | Employee Rating for the previous year |
| length_of_service | Length of service in years |
| KPIs_met >80% | if Percent of KPIs(Key performance Indicators) >80% then 1 else 0 |
| awards_won? | if awards won during previous year then 1 else 0 |
| avg_training_score | 	Average score in current training evaluations |
| is_promoted | (Target) Recommended for promotion |