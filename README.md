# MindForge - загрузка

Репозиторий сайта загрузки MindForge. Файлы раздаются как вложения GitHub Release.

| Файл | Размер | SHA-256 |
|---|---|---|
| `MindForge.Quiz.zip` | 129.56 МБ | `55076a6707cd24e5a146ccf2ba5043da467ff99ad2d75be766f0a6c15c999aa8` |
| `MindForge.Quiz.Android.apk` | 3.53 МБ | `08b9040e8d7944b9e5776d3ed35cc216dbd7474d1631d3624026802c6c5907d1` |
| `QuizForge.Studio.zip` | 129.56 МБ | `52ff2190acf0719a80fd84651deef5613c3530b0c6392d8291bd9f05fe080947` |
| `QuizForge.Studio.Android.apk` | 3.53 МБ | `2f9e9270ba7380ee475ad338d9a8e1ff4021c9160917df20dda7bf6861c65912` |
| `MindForge.Admin.zip` | 129.57 МБ | `27757d07039b0fedff6b1b71ac02a9482ebb5cfc566c5144d508bc3a80c5e1a2` |
| `MindForge.Admin.Android.apk` | 3.53 МБ | `7def1572aaef5d0910095a75f78697c3906ede06816f0cfa0c055672507fc9f5` |

Прямые ссылки:

- [MindForge Quiz, ПК](https://github.com/GappSheR/QuizForge-Studio-Download/releases/latest/download/MindForge.Quiz.zip)
- [MindForge Quiz, Android](https://github.com/GappSheR/QuizForge-Studio-Download/releases/latest/download/MindForge.Quiz.Android.apk)
- [QuizForge Studio, ПК](https://github.com/GappSheR/QuizForge-Studio-Download/releases/latest/download/QuizForge.Studio.zip)
- [QuizForge Studio, Android](https://github.com/GappSheR/QuizForge-Studio-Download/releases/latest/download/QuizForge.Studio.Android.apk)
- [MindForge Admin, ПК](https://github.com/GappSheR/QuizForge-Studio-Download/releases/latest/download/MindForge.Admin.zip)
- [MindForge Admin, Android](https://github.com/GappSheR/QuizForge-Studio-Download/releases/latest/download/MindForge.Admin.Android.apk)

Сайт: https://gappsher.github.io/QuizForge-Studio-Download/

## Почему файлы в Release, а не в репозитории

GitHub не принимает в git файлы больше 100 МБ, а сборка ПК весит около 130 МБ.
Вложения Release ограничены 2 ГБ и отдаются по прямым ссылкам, поэтому архивы лежат именно там.

## Вход на сайте

Сайт спрашивает логин и пароль перед показом ссылок. Это только интерфейсная заглушка:
вложения Release публичны и доступны напрямую. Настоящая защита требует своего сервера.

## Загрузка новой версии

1. `powershell -File scripts\package-release.ps1` - пересобирает ZIP и APK, пишет `site-studio\hashes.txt`.
2. `powershell -File scripts\push-release.ps1` - заливает файлы в релиз.
3. `powershell -File scripts\push-site-studio.ps1` - обновляет сайт и README.

Сайт работает на GitHub Pages из ветки `main`, файл `index.html` в корне.