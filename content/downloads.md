---
layout: default
permalink: /downloads/
---

## Downloads

<!-- <html> -->
  <!-- <body> -->
    <script>
      (async () => {
        const response = await fetch('https://api.github.com/repos/{{ site.user }}/{{ site.user }}.github.io/contents/downloads/');
        const data = await response.json();
        let htmlString = '<ul>';
        for (let file of data) {
          htmlString += str.concat('<li><a href="https://github.com/{{ site.user }}/{{ site.user }}.github.io/blob/master',${file.path},'">',${file.name},'</a></li>');
        }
        htmlString += '</ul>';
        <!-- body = document.getElementsByTagName('body')[0].innerHTML; -->
        <!-- document.getElementsByTagName('body')[0].innerHTML = body + htmlString; -->
      })()
    </script>
  <!-- <body> -->
<!-- </html> -->
