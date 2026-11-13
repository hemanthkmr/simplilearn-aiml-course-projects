# Creating Cohorts of Songs - report
Status: DONE. Notebook executed with no errors (about 1 min on CPU).

Done: cleaning and inspection, EDA with feature engineering, recommended albums, popularity vs features and era, PCA explanation, k selection, algorithm comparison, cluster definitions.
Key metrics: 1610 tracks (no missing/duplicate ids/erroneous rows). Recommended albums: Exile On Main Street and Sticky Fingers (editions grouped; 36 and 23 popular songs). PCA: 6 components reach 80% variance. K-Means k=4, silhouette 0.204 (Ward 0.165, GMM 0.125). Silhouette is low, so cohorts are soft.
All brief steps met. Deviations: the cleaning checks removed no rows (data was already clean); k=4 chosen as best silhouette for k>=3 (k=2 scores 0.235 but is too coarse).
Files: Creating_Cohorts_of_Songs.ipynb/.html, submission/ (Creating_Cohorts_of_Songs.ipynb, Source_Code.zip, Writeup.docx, Screenshots.zip), all under 10 MB.
