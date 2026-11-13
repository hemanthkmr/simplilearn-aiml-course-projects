# REPORT: Performing Facial Recognition with Deep Learning (project 11642)
Status: DONE

## What was done
Pooled the 400 ORL images (20 subjects x 20) from ORL_faces.npz, viewed samples, built a stratified 70/15/15 train/validation/test split (280/60/60), scaled and reshaped to 112x92x1, built a 3-block Conv+MaxPool CNN with a dense head (Model A), trained and plotted it, then iterated with Model B (augmentation + dropout + LR schedule).

## Key metrics (test set of 60 images)
- Model A: validation accuracy 1.000, test accuracy 0.967
- Model B: validation accuracy 0.983, test accuracy 1.000 (train 1.000)
- Target above 90% accuracy: met by both.

## Brief steps
Steps 1-9 all met, in order, with a markdown heading per step. Transfer learning was optional and not used.

## Deviations and notes
- Dataset has 20 subjects (not the 40 in the problem statement); this is what the supplied ORL_faces.npz contains.
- A first Model B variant with batch normalisation and early stopping on validation accuracy failed (about 10% accuracy); I replaced it with the augmentation + dropout version above and the notebook shows the final one only.
- With 60 test images one image is worth 1.7 points; results are baseline numbers.

## Run time
About 5-10 minutes on CPU (4.3 min in a quiet run, longer when other jobs share the machine).

## Files
- Notebook (executed): `Facial_Recognition_ORL.ipynb`, HTML: `Facial_Recognition_ORL.html`
- `submission/Facial_Recognition_ORL.ipynb` (the file for the LMS upload), `submission/Source_Code.zip`, `submission/Writeup.docx`, `submission/Screenshots.zip`
