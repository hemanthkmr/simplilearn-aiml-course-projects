# Marketing Campaigns: REPORT
Status: DONE. Notebook executed with no errors; run time about 1.5 minutes.

Files: Marketing_Campaigns.ipynb / .html; submission/Marketing_Campaigns.ipynb (the LMS upload), Source_Code.zip, Writeup.docx, Screenshots.zip (all under 2 MB).

Steps met (all in order, each with a heading and interpretation): 1 import and verify Dt_Customer/Income; 2 clean Education/Marital_Status and impute 24 missing Income by Education x Marital median; 3 Total_Children, Age, Total_Spending; 4 Total_Purchases; 5 box plots/histograms and outlier capping (Age 3, Income 8); 6 ordinal (Education) and one-hot (Marital_Status, Country) encoding; 7 heatmap; 8 four hypothesis tests; 9 five visual analyses.

Key metrics: H1 not supported (store share 0.485 for 55+ vs 0.512, p~1); H2 web share higher for parents (0.353 vs 0.273, p<0.001) but web count not higher; H3 no cannibalisation (store vs web r=0.50, vs catalog r=0.52); H4 US 13.51 vs 12.49, p=0.072 not significant. Wines 50.2% of revenue, Fruits lowest. Age vs Response r=-0.020. Spain most accepters (176). Children vs spending rho=-0.48. 21 complaints.

Deviations/assumptions: Age uses reference year 2014 (latest enrolment); "older" = 55+; Alone/YOLO/Absurd mapped to Single; 2n Cycle merged into Master; spending/purchase tails not capped (genuine heavy buyers). Outputs kept light. Note: the first draft of the notebook text was written before results; all interpretations were then checked against the executed outputs.
