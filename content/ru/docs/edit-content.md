# Редактирование контента на minter.network

Весь контент на [minter.network](https://minter.network) представлен в виде Markdown файлов с раширением `.md`. Редактировать их можно либо через Github, либо клонировать репозиторий и локально использовать любимый редактор, а затем запушить обратно в репозиторий. 

Всё, что попадает в ветку `master` будет автоматически залито на сайт [minter.network](https://minter.network).  
Для тестирования или во время разработки нужно использовать ветку `dev`, из неё будет заливаться на [beta.minter.network](https://beta.minter.network) 

## Структура директорий
Файлы должны располагаться в директории `/content` и разбиты по категориям: 
- `/content/docs`
- `/content/tools`
- `/content/solutions`
- `/content/how-to`

Такие файлы будут автоматически превращены в html страницы. Адрес страницы будется основываться на пути файла, отбрасывая начальный `/content` и завершающие `.md` или `index.md` части.

| Файл | URL |
|:-----|:----|
| `/content/docs/index.md` | /docs |
| `/content/docs/second.md` | /docs/second |
| `/content/ru/tools/third.md` | /ru/tools/third |

## Изображения

Изображения должны располагаться в папке `/asets/img`. 

Путь до изображения должен соответствовать расположению статьи. Например, для статьи `/content/ru/docs/second.md` изображение должно лежать по пути `/assets/img/docs/second/my-image.jpg`. Локаль не указывается в пути картинки, т.к. в большинстве случаев изображение будет одно для всех локалей. Если же нужно несколько версий картинки под каждую локаль, то можно добавить суффикс в название файла: `my-image.jpg`, `my-image-ru.jpg`.

На сайте они будут доступны по тому же адресу, только без префикса `/assets`. Т.е. использовать эту картинку можно будет так:  
 `![My image](/img/docs/second/my-image.jpg)`
 
## Markdown разметка
Помимо [базового синтаксиса](https://www.markdownguide.org/basic-syntax) поддерживается расширенный набор возможностей: [GitHub Flavored Markdown (GFM)](https://guides.github.com/features/mastering-markdown/#GitHub-flavored-markdown)

Заголовок первого уровня будет использован в боковом меню, для навигации по категории (например, по категории /docs).
```
# Заголовок 1
```

Заголовки второго уровня будут отображены в боковом меню для удобной навигации по текущей странице. 
```
## Заголовок 2

## Ещё один заголовок 2
```

