# REPORT: Help Twitter Combat Hate Speech Using NLP and ML (project 11652)
Status: DONE

## What was done
All 15 tasks: read_csv, tweet list, cleanup (lowercase, handles, URLs, TweetTokenizer, stop words, amp/rt, #), drop 1-char terms, top-10 terms with Counter, join tokens and stratified train/test split (75/25), TF-IDF (5000 terms), plain logistic regression, evaluation, class_weight='balanced', GridSearchCV (C x penalty) with StratifiedKFold(4) scoring recall, best params, evaluation on test.

## Key metrics (test set, hate class = 1)
| Model | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| Plain LR | 0.950 | 0.908 | 0.317 | 0.470 |
| Balanced LR | 0.924 | 0.474 | 0.779 | 0.590 |
| Tuned LR (C=1, L2) | 0.924 | 0.476 | 0.779 | 0.591 |

Train recall of plain LR is low (0.38), balanced 0.97. Best CV recall 0.774.

## Brief steps
All numbered steps met.

## Deviations and notes
- The data columns are id/label/tweet (matches the main brief); the PDF slides mention comment_text/toxic, which does not apply.
- I also dropped pure-punctuation tokens (for example '...') in step 4, and 'user' (the dataset's handle placeholder) and 'via', 'u', 'ur' as redundant terms.
- Tuning gives essentially the same test result as the balanced default.

## Run time
About 1-3 minutes.

## Files
- Notebook (executed): `Twitter_Hate_Speech_Detection.ipynb`, HTML: `Twitter_Hate_Speech_Detection.html`
- `submission/Twitter_Hate_Speech_Detection.ipynb` (the file for the LMS upload), `submission/Source_Code.zip`, `submission/Writeup.docx`, `submission/Screenshots.zip`
