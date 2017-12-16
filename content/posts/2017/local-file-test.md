---
title: "Local File test"
date: 2017-12-09T13:55:37+08:00
categories: ["示例", "測試"]
tags: ["markdown", "local"]
toc: true
---

# Jupyter Notebook

<div class="jupyter-notebook">
    <script defer>
        function notebook_onload(obj) {
            var bg = window.getComputedStyle(document.body, null)['background-color']
            obj.style.height = obj.contentDocument.body.scrollHeight + 'px';
            obj.contentDocument.body.style.backgroundColor = bg;
        }
    </script>
    <iframe src="wine.html" scrolling="no"
        onload="notebook_onload(this)">
    </iframe>
</div>

# Image

![](./test.png)