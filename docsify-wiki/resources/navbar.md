# Добавление панели навигации

Для создания (настройки) навигации по нашей документации необходимо выполнить шаги:
* создать файл "_navbar.md" и наполнить его информацией для навигации;
* добавить аргумент в вызов функции window.$docsify() в файле "index.html".

## Добавление разделов навигации в файл "_navbar.md"

В корневом каталоге нашего проекта создадим файл "_navbar.md" следующего содержания:

```markdown
<!-- _navbar.md -->

* Languages
    * [Русский](/resources/README.md)
    * [English](/resources/en/README.md)
* [Официальная документация](https://docsify.js.org)
```

## Настройка отображения в файле "index.html"

Далее в файле "index.html" добавим:

```html
      loadNavbar: true,
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
    }
</script>
```