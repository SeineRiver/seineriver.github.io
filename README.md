# ABRSM Music Theory Test App

A simple, strictly client-side mock-test application for ABRSM Music Theory Grades 1–3.

## How to use

No local server, build step, or package installation is required.

Open [`index.html`](./index.html) directly in a web browser.

## How the mock test works

- Each test contains 15 questions.
- Five questions are randomly selected from each grade.
- The 15 questions are mixed before they are shown.
- Each question has four answer choices: one correct answer and three distractors selected from the same grade bank.
- Questions are answered one at a time.
- Progress and the current score are shown during the test.
- After the final question, the result page lists incorrect answers alongside the correct answers.
- **Do another test** starts a fresh randomized test.

## Ground truth and question bank

The maintained ground truth for the app is the PDF question bank:

[`output/pdf/abrsm-terms-and-signs-grades-1-3.pdf`](./output/pdf/abrsm-terms-and-signs-grades-1-3.pdf)

The PDF is the canonical reference for the questions, answers, grade grouping, and notation graphics. The question data in [`app.js`](./app.js) is the client-side runtime copy used by the application and should be kept synchronized with the PDF whenever the bank changes.

The PDF was compiled from:

- The supplied Grade 1, Grade 2, and Grade 3 Terms & Signs PPSX presentations
- The attached ABRSM terms-and-signs PDF
- The attached ABRSM terms-and-signs DOCX

Notation images used by both the app and the PDF are stored under [`assets/`](./assets).

## Project structure

```text
index.html                         Application markup
styles.css                         Application styling
app.js                             Question bank and test logic
assets/                            Musical notation images
output/pdf/                        Canonical PDF question bank
```

## Updating the bank

When adding or correcting questions:

1. Update the canonical PDF question bank first.
2. Update the corresponding grade array in `app.js`.
3. Keep question wording, answers, grade tags, and image paths aligned between the PDF and app.
4. Run a JavaScript syntax check before committing:

   ```bash
   node --check app.js
   ```

