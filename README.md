# Mdbook with pdf files

This repository demonstrates how to use pdf.js inside mdbook.  

## Get started locally with a simple example

Steps:
- Fork this repository
- [Install mdbook](https://rust-lang.github.io/mdBook/guide/installation.html)
- Run `mdbook serve`

You can then see two pages:
- src/ex_md.md, a sample markdown file
- src/ex_pdf.md, loading src/paper.pdf inside a pdf.js viewer:
```
<script type="text/javascript" src="utils.js"></script>

<iframe id="pdf-js-viewer" src="" title="webviewer" frameborder="0" width="100%" height="800"></iframe>

<script>
    window.onload = () => document.getElementById("pdf-js-viewer").src = url("paper.pdf") + "#zoom=page-width&pagemode=none";
</script>
```
Just change `url("paper.pdf")` to load another pdf file.

The table of contents can be modified inside src/SUMMARY.md.

## Publish to GitHub Pages

To publish on GitHub Pages, go to Settings -> Pages, select "Branch: gh-pages" and "Save".  
The next commit will publish your site (via .github/workflows/mdbook.yml)

## Complete example

Complete example for a course: https://fortierq.github.io/oc-m1-2021
