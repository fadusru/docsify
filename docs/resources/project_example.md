# Пример получившегося проекта

В ходе подготовки данной документации у меня получилась:

* следующая структура дерева файлов:

<img src="/resources/assets/tree_files.webp">

* и текст файла "index.html":

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Document</title>
  <meta name="description" content="Description">
  <meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
  <link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify@5/dist/themes/core.min.css">
  <link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify@5/dist/themes/addons/vue.min.css">
<!--  <link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify@5/dist/themes/addons/core-dark.min.css" />-->
</head>
<body>
  <div id="app"></div>
  <script>
    window.$docsify = {
      name: '',
      repo: '',
      loadSidebar: true,
      subMaxLevel: 3,
      loadNavbar: true,
      coverpage: true,
    }
  </script>
  <!-- Docsify resource -->
  <script src="//cdn.jsdelivr.net/npm/docsify@5"></script>
  <script src="//cdn.jsdelivr.net/npm/docsify@5/dist/plugins/zoom-image.min.js"></script>
  <script src="//cdn.jsdelivr.net/npm/docsify-copy-code/dist/docsify-copy-code.min.js"></script>
</body>
</html>
```