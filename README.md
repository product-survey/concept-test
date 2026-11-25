# MOP Concept Test — Version 3 (GitHub Pages)

Custom survey page. Each respondent gets the 5 concepts in a **fully random order**
(stored on their device, so refreshing keeps the same order). Answers go to a hidden
Google Form → Google Sheet.

## Setup (once)
1. **Data sink**: in script.google.com, paste `MOP_Concept_Test_v3_DataSink.gs`, run `setupDataSink()`.
2. Open the new spreadsheet → tab **Paste into index.html** → copy cell A2.
3. In `index.html`, replace the `const SINK = {...};` block with what you copied.
4. **GitHub**: new public repository (e.g. `mop-survey`) → upload `index.html` and the `images` folder.
5. Settings → Pages → Deploy from a branch → `main` / `(root)` → Save.
6. Your link: `https://<username>.github.io/mop-survey/`

## Before sharing
- Open the link, finish the survey, and check that one row appears in the spreadsheet.
- Test on a phone of someone whose device blocked Apps Script.
- After someone sends their answers, the link starts fresh again on that device (no duplicate blocking).
- Delete test rows in the Google Form (Responses → Delete all responses).

## Analysis
Run `buildCleanData()` → **Clean data** tab: one row per respondent × concept, with position.
