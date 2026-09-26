# QuizForge Studio - загрузка

Репозиторий сайта загрузки QuizForge Studio. Файлы раздаются как вложения GitHub Release.

## Что отдаём

| Файл | Размер | SHA-256 |
|---|---|---|
| `QuizForge.Studio.zip` | 288.3 МБ | `c18eab002b10c5a2a6f50deef8b44353a64c3d72b812d181cd3b54a767509baa` |
| `QuizForge.Studio.Android.apk` | 3.53 МБ | `c5eb7e30318b69a3b5068ec6fe31aa8bfcfb309f06ce4b48306f131b633a3407` |

Прямые ссылки:

- https://github.com/GappSheR/QuizForge-Studio-Download/releases/latest/download/QuizForge.Studio.zip
- https://github.com/GappSheR/QuizForge-Studio-Download/releases/latest/download/QuizForge.Studio.Android.apk

Сайт: https://gappsher.github.io/QuizForge-Studio-Download/

## Почему файлы в Release, а не в репозитории

GitHub не принимает в git файлы больше 100 МБ, а портативная сборка Studio весит 288 МБ.
Вложения Release ограничены 2 ГБ и отдаются по прямым ссылкам, поэтому архив лежит именно там.

## Почему zip без сжатия

Архив собран методом Store (без сжатия) - распаковывается быстро, без распаковки каждого файла.
Сжатый вариант весит примерно 81 МБ, но распаковка занимает минуту.

## Загрузка новой версии

1. Создать релиз с новым тегом.
2. Загрузить в него `QuizForge.Studio.zip` и `QuizForge.Studio.Android.apk`.
3. Обновить ссылки и SHA-256 в `index.html` и в этом файле.
4. Сайт работает на GitHub Pages из ветки `main`, файл `index.html` в корне.