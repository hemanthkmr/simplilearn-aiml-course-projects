# Autonomous Driving (Capstone 1, Parts 1 and 2) - REPORT

Status: DONE. Notebook Autonomous_Driving.ipynb (executed, no errors), .html, and submission/ (Autonomous_Driving.ipynb, Source_Code.zip, Writeup.docx, Screenshots.zip). Data from course 07 Datasets.zip (Capstone 1: Images.zip, labels.csv, Tesla - Deaths.csv), copied to data/.

## Steps met
Part 1: (1) folder structure custom_training/; (2) dataset prepared (5,626 images extracted, labels filtered, per-image size handling, 70/15/15 split, YOLO label files); (3) YOLO-style CNN detector (pretrained MobileNetV2 width 0.5, stride-16 grid, 4 anchors, 11 classes); (4) test evaluation; (5) inference on 8 samples. Part 2: cleaning and all EDA items.

## Key metrics (844 test images)
mAP@0.5 = 0.2016. AP@0.5: pickup_truck 0.538, bus 0.469, car 0.447, work_van 0.176, motorcycle 0.166, articulated_truck 0.122, motorized_vehicle 0.105, single_unit_truck 0.095, bicycle 0.058, pedestrian 0.040, non-motorized_vehicle 0.000. Mean best-IoU 0.48. Inference 17 ms/image on CPU.
Tesla: 294 events, 353 deaths; driver died in 117 events, occupant in 43; cyclist/pedestrian died in 44; other vehicle in 110; 16 events with verified autopilot deaths (19 deaths).

## Deviations / notes
- CPU-limited: 160x240 input, MobileNetV2 width 0.5, 11 epochs (about 26 min). Validation loss was still falling, so mAP is modest; rare and small classes are weak.
- labels.csv lists 110,000 image ids but only 5,626 images exist; only those were used (17,967 boxes).
- Images have two sizes (720x480, 342x228); boxes are normalised per image (an earlier run that assumed one size was discarded).
- Tesla file has a Year typo (202) and footer summary rows, which were removed.
- submission/ also holds the executed notebook alone (4.5 MB) for the LMS .ipynb upload.

Run time: about 26 minutes.
