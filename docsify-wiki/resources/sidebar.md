# Добавление меню (разделов)

Для создания (настройки) разделов нашей документации необходимо выполнить шаги:
* создать файл "_sidebar.md" и наполнить его информацией для меню;
* добавить аргумент в вызов функции window.$docsify() в файле "index.html".

Давайте сделаем это.

## Добавление пунктов меню в файл "_sidebar.md"
В корневом каталоге нашего проекта создадим файл "_sidebar.md" следующего содержания:

```markdown
<!-- _sidebar.md -->

* [На главную](/)
* [О проекте](/resources/README.md)
* [Установка](/resources/install.md)
* [Создание проекта](/resources/create_project.md)
* [Запуск проекта](/resources/run_project.md)
* [Добавление меню (разделов)](/resources/sidebar.md)
* [Добавление панели навигации](/resources/navbar.md)
* [Добавление главной страницы](/resources/coverpage.md)
* [Настройка темы](/resources/themes.md)
* [Подключение плагинов](/resources/plugins.md)
* [Пример получившегося проекта](/resources/project_example.md)
```

## Настройка отображения в файле "index.html"

### Добавление бокового меню
Далее в файле "index.html" добавим:

```html
      loadSidebar: true,
```

Пример как получилось у меня (привожу пример фрагмента файла "index.html"):

```html
  <script>
    window.$docsify = {
        name: '',
        repo: '',
        loadSidebar: true,
    }
</script>
```
### Настройка уровня вложенности бокового меню

Для настройки уровня вложенности меню в файле "index.html" добавим аргумент:

```html
      subMaxLevel: 3
```

В моем примере указан уровень вложенности заголовков 3, установите необходимый уровень для своего проекта.

Пример как получилось у меня (привожу пример фрагмента файла "index.html"):

```html
  <script>
    window.$docsify = {
        name: '',
        repo: '',
        loadSidebar: true,
        subMaxLevel: 3,
    }
</script>
```