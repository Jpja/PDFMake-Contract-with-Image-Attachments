# PDFMake-Contract-with-Image-Attachments
JS template for PDF legal contract with optional image attachments 

### Introduction

`pdfmake-contract.html` uses the pdfmake library to generate a legal contract. It runs in the browser, JS client-side, and outputs a pdf file.

The contract is derived from a template where keywords are replaced with user inputs and algorithms. 
 
Two level dynamic numbering, e.g. `1. This is a subheader` and `1.1 And this is a clause`.

Refer to another clause by keyword (so you don't need to keep track of numbering).

Two optional image attachments. Paste them from the clipboard while the browser tab is open.

### How to use

The `template` array is near the top of the script. Every header and paragraph must be given a level key of `'0'`, `'1'` or `'2'`.
- `'0'` is an un-numbered paragraph
- `'1'` is a subheader
- `'2'` is a clause

The very first element is the document title and does not require a level key.

All keywords you want replaced must be inside {curly brackets}. The `replacekey` object replaces any key it has defined. 

The sample scripts shows how to collect user input, as well as automatically set the date or copy values from another object.

### Limitation

No formatting is possible. If you want certain words in bold or italic, you'll need to write that functionality yourself. 

### Potential issue

I have tested the paste image method on FF and Chrome on Win 10. I suspect some browser environments (now or in the future) block this feature.
