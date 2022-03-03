# Mdbook with pdf files

This repository demonstrates how to use pdf.js inside mdbook.  

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

The table of content can be modified inside src/SUMMARY.md.
