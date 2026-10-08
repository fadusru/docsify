# Добавление главной страницы

Для настройки главной страницы (страницы "по умолчанию") нашей документации необходимо выполнить шаги:
* создать файл "_coverpage.md" и наполнить его содержимым;
* добавить аргумент в вызов функции window.$docsify() в файле "index.html".

## Добавление разделов титульной страницы в файл "_coverpage.md"

В корневом каталоге нашего проекта создадим файл "_coverpage.md" следующего содержания:

```markdown
<!-- _coverpage.md -->

![logo](/resources/assets/icon.svg ':size=20%')

# Docsify

[Документация](/resources/README.md)
[Официальный сайт](https://docsify.js.org)
[Исходный код](https://github.com/docsifyjs/docsify/)
```

## Настройка отображения в файле "index.html"

Далее в файле "index.html" добавим аргумент в вызов функции window.$docsify():

```html
      coverpage: true,
```

Пример как получилось у меня (привожу пример фрагмента файла "index.html"):

```html
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
```