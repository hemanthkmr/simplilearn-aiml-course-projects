# Home Loan Data Analysis: REPORT
Status: DONE. Notebook executed with no errors (~151 s on CPU).
Files: Home_Loan_Data_Analysis.ipynb/.html, submission/ (Home_Loan_Data_Analysis.ipynb for LMS upload, Source_Code.zip, Writeup.docx, Screenshots.zip), data/.
Steps met: load, null check (67 columns with nulls), TARGET percentage (91.93% payers / 8.07% defaulters), balance (train under-sampling 50:50), plots (imbalanced and balanced), encoding (one-hot + label), sensitivity, ROC-AUC.
Test metrics (untouched 20% stratified split): sensitivity 0.666, specificity 0.686, accuracy 0.684, precision 0.157, F1 0.254, ROC-AUC 0.736.
Deviation: random under-sampling instead of SMOTE (CPU time); columns >40% null dropped.
