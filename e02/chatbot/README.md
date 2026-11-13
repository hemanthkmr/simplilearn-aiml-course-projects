# REPORT: NLP and Speech Recognition Chatbot (project 11657)
Status: DONE (speech input path written but not executable here)

## What was done
Own implementation following the brief's structure: loaded commands.json (14 intents, 47 patterns in 9 patterned intents), tokenise and lemmatise, bag-of-words, 3-layer Keras network (128-64-softmax, dropout 0.5, SGD Nesterov, 200 epochs, batch 5), response engine with confidence threshold and context-driven multi-turn follow-ups, `read_command()` (SpeechRecognition microphone) and `talk()` (pyttsx3 if present), scripted demo conversations.

## Key metrics
- Training accuracy 1.000 (47 patterns, vocabulary 87)
- Held-out paraphrases (30 queries I wrote): 29/30 = 0.967; in-scope 1.000; out-of-scope fallback 3 of 4 (0.75)

## Brief steps
Install/import, load data, preprocessing, training data, model, train and save, predict responses, speech functions: all present.

## Deviations and notes
- The zip content was used only as data (commands.json) and brief text. No supplied code, pickle or .h5 file was executed or loaded; the model was retrained.
- Speech recognition and TTS could not be exercised: no microphone/PyAudio, no internet speech API, no TTS engine. The functions fall back to text input; the chatbot logic was tested through that path. SpeechRecognition was installed with pip into the shared environment.
- Confidence threshold was raised from 0.25 to 0.60 after the first run showed the fallback never triggered, judged on the same 30 queries, so the held-out figure is slightly optimistic.
- The dataset is a healthcare-support example, not event support; used unchanged.

## Run time
About 2-3 minutes.

## Files
- Notebook (executed): `Chatbot_NLP_Speech.ipynb`, HTML: `Chatbot_NLP_Speech.html`
- `submission/Chatbot_NLP_Speech.ipynb` (the file for the LMS upload), `submission/Source_Code.zip`, `submission/Writeup.docx`, `submission/Screenshots.zip`
