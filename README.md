# PDF to Text: Accurate Multilingual OCR for Scanned Documents

Building AI course project

## Summary

This project turns scanned PDFs and photos of pages into editable text in many languages. It combines open source OCR engines with image cleanup and automatic checking to get the most accurate result possible. Building AI course project.

## Background

Many important documents exist only as scanned images: old books, official papers, student notes, and records. The text inside them cannot be searched, copied or edited.

* Free OCR tools often make many mistakes on poor scans
* Accuracy drops sharply for non-Latin scripts such as Arabic and Bengali
* Many good tools need an expensive paid service or technical skill
* Retyping a long document by hand takes hours

My motivation: I work with texts in Arabic, Bengali and English, and I have seen how much time is lost when a scanned book cannot be copied or searched. I want a tool that handles all of these languages well.

## How is it used?

1. The user uploads a PDF or a photo of a page
2. The system cleans the image (straightening, removing noise, improving contrast)
3. The OCR engine reads the text in the chosen language
4. A checking step flags words it is unsure about
5. The user downloads the result as a text file (Word output later)

Users are students, researchers, teachers and office workers who have scanned material. Documents may contain private information, so uploads must be handled with care.

## Data sources and AI methods

| Need | Source | Method |
| --- | --- | --- |
| Text recognition | Open source engines such as Tesseract and PaddleOCR | Deep learning OCR |
| Test documents | My own scans and public domain books | Manual comparison against correct text |
| Image cleanup | Standard image processing libraries | Deskewing, denoising, thresholding |
| Language models for checking | Open dictionaries and word lists | Spell checking, confidence scores |
| Accuracy measurement | Hand-typed reference pages | Character error rate and word error rate |

I will run several engines on the same pages and compare their error rates, then keep the best one for each language.

## Challenges

* No OCR is perfect, especially on blurry, handwritten or damaged pages
* Right to left scripts and pages with diacritics are harder to read correctly
* Complex layouts such as tables and multiple columns can come out in the wrong order
* Large PDFs need a lot of computing power
* Uploaded documents may be private, so they should be deleted after processing
* Accuracy claims must come from real tests, not guesses

## What next?

* Test and compare engines on a small set of pages in each language
* Add Word file output that keeps paragraphs and headings
* Support more languages over time
* Add a review screen where users can correct flagged words
* Work with people who have OCR and machine learning experience

## Acknowledgments

* Tesseract OCR, open source, Apache 2.0 licence
* PaddleOCR, open source, Apache 2.0 licence
* Elements of AI and Building AI, University of Helsinki and Reaktor
