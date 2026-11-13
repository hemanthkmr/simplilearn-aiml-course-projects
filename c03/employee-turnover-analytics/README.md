# Employee Turnover Analytics - report
Status: DONE. Notebook executed with no errors (about 4 min on CPU).

Done: all 7 brief steps in order (quality check, correlation heatmap, 3 distribution plots, project-count bar plot with inference, K-Means k=3 on leavers, get_dummies, stratified 80:20 split random_state=123, SMOTE on train, 5-fold CV for LR/RF/GB with classification report plots, ROC/AUC, confusion matrices, recall-vs-precision discussion, four risk zones with strategies).
Key metrics (test set, threshold 0.5): Random Forest acc 0.987, recall 0.978, precision 0.969, AUC 0.995 (best); Gradient Boosting AUC 0.986, recall 0.934; Logistic Regression AUC 0.820, recall 0.709. Red zone actual leave rate 99.4%, Green 0.5%.
Notes: dataset column "sales" renamed Department. 3008 duplicate rows kept. 5-fold CV on the SMOTE-upsampled train set (as specified) is optimistic (RF AUC 0.998), so a leak-free CV (SMOTE inside folds, RF AUC 0.992) and the held-out test results are also reported. Test cell for markdown cluster/tenure statements was checked against computed values.
Files: Employee_Turnover_Analytics.ipynb/.html, submission/ (the .ipynb, Source_Code.zip, Writeup.docx, Screenshots.zip), all under 10 MB.
