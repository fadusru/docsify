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

## Darklight theme

### Рекомендации по настройке Darklight theme для версии 4.x.x Docsify

[Darklight theme](https://github.com/boopathikumar018/docsify-darklight-theme)

Позволяет менять тему с темной на светлую и наоборот.

Для установки в файле  index.html перед окончанием </body>  впишите:

```html
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify-darklight-theme@3/dist/docsify-themeable/style.min.css" type="text/css">

<!-- docsify-themeable styles-->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/docsify-themeable@0/dist/css/theme-simple.css" title="light">
<link rel="stylesheet alternative" href="https://cdn.jsdelivr.net/npm/docsify-themeable@0/dist/css/theme-simple-dark.css" title="dark">
```

А также перед окончанием </head> :

```html
<script
    src="//cdn.jsdelivr.net/npm/docsify-darklight-theme@3/dist/docsify-themeable/main.min.js"
    type="text/javascript">
</script>

<script
    src="//cdn.jsdelivr.net/npm/docsify-darklight-theme@3/dist/docsify-themeable/index.min.js"
    type="text/javascript">
</script>
```

## Копирование содержимого тега code в буфер обмена (Copy code)

Для подключения плагина [Copy to Clipboard](https://docsify.js.org/#/plugins?id=copy-to-clipboard) к нашему проекту, необходимо в файле "index.html" перед закрывающим 
тегом "</body>" вставить тег:

```html
<script src="//cdn.jsdelivr.net/npm/docsify-copy-code/dist/docsify-copy-code.min.js"></script>
```

Внизу страницы текст моего файла "index.htlm" по результатам добавления всех плагинов.

## Создание табов на странице (tabs)

Для подключения плагина [Tabs](https://docsify.js.org/#/plugins?id=tabs) к нашему проекту, переходим на страницу плагина
[docsify-tabs](https://jhildenbiddle.github.io/docsify-tabs/#/) и выполняем настройку по инструкции.

Позволяет переключаться между вкладками на странице.

### Рекомендации по настройке tabs для версии 4.x.x Docsify

Для установки в файле  index.html перед окончанием </body>  впишите:

```html
<!-- docsify (latest v4.x.x)-->
<script src="https://cdn.jsdelivr.net/npm/docsify@4"></script>

<!-- docsify-tabs (latest v1.x.x) -->
<script src="https://cdn.jsdelivr.net/npm/docsify-tabs@1"></script>
```

А также в секции window.$docsify впишите:

```html
window.$docsify = {
// ...
tabs: {
persist    : true,      // default
sync       : true,      // default
theme      : 'classic', // default
tabComments: true,      // default
tabHeadings: true       // default
}
};
```

## Переключение между светлой и темной темами (docsify-darklight-theme)

Для подключения плагина перейдем в раздел [More plugins](https://docsify.js.org/#/plugins?id=more-plugins),
перейдем по ссылке "See [awesome-docsify](https://docsify.js.org/#/awesome?id=plugins)". На открывшейся странице найдем 
и перейдем по ссылке плагина "[docsify-darklight-theme](https://github.com/boopathikumar018/docsify-darklight-theme)".

На открывшей странице на GitHub найдем в строке "Switcher support for docsify-themeable. View [setup guide](https://docsify-darklight-theme.boopathikumar.me/#/docsifyThemeable) here." 
ссылку на [setup guide](https://docsify-darklight-theme.boopathikumar.me/#/docsifyThemeable). Переходим по ней и выполняем настройку по инструкции.

## Вставка диаграмм (Mermaid)

[github.com: Mermaid](https://github.com/Leward/mermaid-docsify)

Позволяет вставлять Mermaid диаграммы.

Для установки в файле index.html перед окончанием </body>  впишите:

```html
<script src="//unpkg.com/mermaid/dist/mermaid.js"></script>
<script src="//unpkg.com/docsify-mermaid@latest/dist/docsify-mermaid.js"></script>
<script>mermaid.initialize({ startOnLoad: true });</script>
```

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
<!-- zoom-image -->
<script src="//cdn.jsdelivr.net/npm/docsify@5/dist/plugins/zoom-image.min.js"></script>
<!-- copy-code -->
<script src="//cdn.jsdelivr.net/npm/docsify-copy-code/dist/docsify-copy-code.min.js"></script>
<!-- memraid -->
<script src="//unpkg.com/mermaid/dist/mermaid.js"></script>
<script src="//unpkg.com/docsify-mermaid@latest/dist/docsify-mermaid.js"></script>
<script>mermaid.initialize({ startOnLoad: true });</script>

</body>
</html>

```