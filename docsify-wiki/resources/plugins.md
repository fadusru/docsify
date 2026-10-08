# Подключение плагинов к Docsify

Многие [плагины](https://docsify.js.org/#/plugins) для Docsify описаны на официальном сайте.

Для добавления плагина в проект в большинстве случаев достаточно вставить ссылку на плагин до закрывающего тега "</body>".

Предлагаю совместно настроить несколько плагинов.

## Плагин Zoom image

Для подключения плагина [Zoom image](https://docsify.js.org/#/plugins?id=zoom-image) к нашему проекту, необходимо в файле "index.html" перед закрывающим тегом
"</body>" вставить тег:

```html
<script src="//cdn.jsdelivr.net/npm/docsify@5/dist/plugins/zoom-image.min.js"></script>
```

Внизу страницы текст моего файла "index.htlm" по результатам добавления всех плагинов.

## Плагин для копирования в буфер обмена

Для подключения плагина [Copy to Clipboard](https://docsify.js.org/#/plugins?id=copy-to-clipboard) к нашему проекту, необходимо в файле "index.html" перед закрывающим 
тегом "</body>" вставить тег:

```html
<script src="//cdn.jsdelivr.net/npm/docsify-copy-code/dist/docsify-copy-code.min.js"></script>
```

Внизу страницы текст моего файла "index.htlm" по результатам добавления всех плагинов.

## Плагин для создания табов на странице

Для подключения плагина [Tabs](https://docsify.js.org/#/plugins?id=tabs) к нашему проекту, переходим на страницу плагина
[docsify-tabs](https://jhildenbiddle.github.io/docsify-tabs/#/) и выполняем настройку по инструкции.

## Плагин для переключения между светлой и темной темами

Для подключения плагина перейдем в раздел [More plugins](https://docsify.js.org/#/plugins?id=more-plugins),
перейдем по ссылке "See [awesome-docsify](https://docsify.js.org/#/awesome?id=plugins)". На открывшейся странице найдем 
и перейдем по ссылке плагина "[docsify-darklight-theme](https://github.com/boopathikumar018/docsify-darklight-theme)".

На открывшей странице на GitHub найдем в строке "Switcher support for docsify-themeable. View [setup guide](https://docsify-darklight-theme.boopathikumar.me/#/docsifyThemeable) here." 
ссылку на [setup guide](https://docsify-darklight-theme.boopathikumar.me/#/docsifyThemeable). Переходим по ней и выполняем настройку по инструкции.

## Пример содержимого моего файла "index.html"

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