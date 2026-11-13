# REPORT - Crafting an AI-Powered HR Assistant (DONE)
OpenAI GPT-4o-mini accessed via OpenRouter's OpenAI-compatible API; embeddings OpenAI text-embedding-3-small via OpenRouter.

**Steps met (all):** setup; PyPDFLoader load + cleaning + split (8 pages -> 25 chunks, 700/120); Chroma + OpenAI embeddings (1536-d); retrieval QA with GPT; prompt template (grounding, refusal, page citations); Gradio ChatInterface launched locally (share=False) and screenshotted for real with headless Chromium/Playwright; evaluation on 10 varied questions; integration/deployment notes.
**Key metrics:** 10/10 pass on keyword test set (coarse proxy); in-scope answer recall 1.00; retrieval hit 0.88; out-of-scope questions declined 2/2.
**Deviation:** brief says GPT-3.5 Turbo; openai/gpt-3.5-turbo failed on all provided keys, so GPT-4o-mini was used. Said so in the notebook.
**Run time:** ~3.5 min.
**Files:** Nestle_HR_Assistant.ipynb/.html, submission/{Writeup.docx, Screenshots.zip, Source_Code.zip (incl. the 1.5 MB policy PDF), ipynb}.
