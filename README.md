# PDFMake Contract with Image Attachments
JS template for PDF legal contract with optional image attachments 

### Introduction

`pdfmake-contract.html` uses the pdfmake library to generate a legal contract. It runs in the browser, JS client-side, and outputs a pdf file.

- template where keywords are replaced with user inputs and algorithms. 
- dynamic numbering, e.g. `1. This is a subheader` and `1.1 And this is a clause`.
- refer to another clause by keyword (so you don't need to keep track of numbering).
- two optional image attachments. Paste them from the clipboard while the browser tab is open.

### Get started

Watch video: https://youtu.be/hf6B14PqG5M

Or read this:

The `template` array is near the top of the script. Every header and paragraph must be given a level key of `'0'`, `'1'` or `'2'`.
- `'0'` is an un-numbered paragraph
- `'1'` is a subheader
- `'2'` is a clause

The very first element is the document title and does not require a level key.

All keywords you want replaced must be inside {curly brackets}. The `replacekey` object replaces any key it has defined. 

The sample script shows how to collect user input, as well as automatically set the date or copy values from another object.

### Limitation

No formatting is possible. If you want certain words in bold or italic, you'll need to write that functionality yourself. 

### Potential issue

I have tested the paste image method on FF and Chrome on Win 10. I suspect some browsers (now or in the future) block this feature.
