# Lending Club Loan Data Analysis: REPORT
Status: DONE. Notebook executed with no errors (~113 s on CPU).
Files: Lending_Club_Loan_Data_Analysis.ipynb/.html, submission/ (the .ipynb for LMS upload, Source_Code.zip, Writeup.docx, Screenshots.zip), data/.
Steps met: Task 1 label encoding of purpose; Task 2 EDA; Task 3 correlation matrix and dropping one of each |r|>0.7 pair (int.rate/fico pair); Task 4 Keras network with class weights.
Test metrics (stratified 20%): sensitivity 0.557, specificity 0.682, accuracy 0.662, precision 0.251, F1 0.346, ROC-AUC 0.673.
Deviation: the brief mentions input.csv/output.csv; none exist in the datasets, only loan_data.csv was used.
