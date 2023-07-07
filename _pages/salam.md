---
layout: archive
title: "SALAM"
permalink: /salam/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<!DOCTYPE html>
<html>
<head>
    <title>Markdown with PDF Displayer</title>
    <style>
        /* CSS styles for the PDF displayer */
        #pdf-display {
            width: 100%;
            height: 600px;
        }
    </style>
</head>
<body>
    <div id="markdown-content">
        <!-- Your Markdown content goes here -->
    </div>

    <iframe id="pdf-display" src="files/OToragay_CV.pdf" width="100%" height="600px" frameborder="0"></iframe>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/markdown-it/12.0.4/markdown-it.min.js"></script>
    <script>
        // Parse and render the Markdown content
        var markdownContent = document.getElementById('markdown-content').textContent;
        var md = window.markdownit();
        var parsedContent = md.render(markdownContent);

        document.getElementById('markdown-content').innerHTML = parsedContent;
    </script>
</body>
</html>
