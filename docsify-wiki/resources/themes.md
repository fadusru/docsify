# Настройка темы в Docsify

Ознакомиться с примерами тем можно на [официальном сайте](https://docsify.js.org/#/themes).

Например, мы хотим настроить темную тему для нашего сайта, для этого открываем файл "index.html", в нем находим тег
со ссылкой на текущую тему, ставим комментарий (символы "!--" после знака "<" и символы "--" перед знаком ">").

```html
  <!--link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify@5/dist/themes/addons/vue.min.css"-->
```
После вставляем тег со ссылкой на нужную нам тему:

```html
  <link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify@5/dist/themes/addons/core-dark.min.css" />
```

Пример моего файла "index.html":

```html 
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Document</title>
  <meta name="description" content="Description">
  <meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
  <link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify@5/dist/themes/core.min.css">
    <!--  link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify@5/dist/themes/addons/vue.min.css"-->
  <link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify@5/dist/themes/addons/core-dark.min.css" />
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
</body>
</html>
```