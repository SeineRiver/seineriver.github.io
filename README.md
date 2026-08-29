# SeineRiver website

This repository hosts two independent, static web apps. No build step or server-side code is required.

## Apps

- [`abrsm-test/`](./abrsm-test/) — an ABRSM Music Theory Grades 1–3 mock-test app. Its setup, question-bank, and maintenance notes are in [`abrsm-test/README.md`](./abrsm-test/README.md).
- [`gallery/`](./gallery/) — an image gallery for the files in [`gallery/images/`](./gallery/images/). Its usage notes are in [`gallery/README.md`](./gallery/README.md).

## Site entry point

The root [`index.html`](./index.html) redirects visitors to the ABRSM test, so the published site opens that app by default. The gallery is available separately at [`gallery/index.html`](./gallery/index.html).

## Structure

```text
index.html             Redirects the root site to abrsm-test/
abrsm-test/            ABRSM mock-test app and its README
gallery/               Image gallery app, images, and its README
privacy-policy.html    Standalone privacy-policy page
```
