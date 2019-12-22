---
layout: default
permalink: /downloads/
---

## Downloads

<html>
  <body>
    <script>
      (async () => {
        const response = await fetch('https://api.github.com/repos/{{ site.user }}/{{ site.user }}.github.io/contents/downloads/');
        const data = await response.json();
        let htmlString = '<ul>';
        for (let file of data) {
          htmlString += `<li><a href="{{ site.baseurl | absolute_url }}${file.path}">${file.name}</a></li>`;
        }
        htmlString += '</ul>';
        document.getElementsByTagName('body')[0].innerHTML = htmlString;
      })()
    </script>
  <body>
</html>
