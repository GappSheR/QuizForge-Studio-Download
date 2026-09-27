# MindForge - загрузка

Репозиторий сайта загрузки MindForge. Файлы раздаются как вложения GitHub Release.

| Файл | Размер | SHA-256 |
|---|---|---|
| `MindForge.Quiz.zip` | 129.56 МБ | `55076a6707cd24e5a146ccf2ba5043da467ff99ad2d75be766f0a6c15c999aa8` |
| `MindForge.Quiz.Android.apk` | 3.53 МБ | `32fb952f1271bf895d84fce095af410b41fd4ae0e41cc3c8a4453386714fc39a` |
| `QuizForge.Studio.zip` | 129.56 МБ | `52ff2190acf0719a80fd84651deef5613c3530b0c6392d8291bd9f05fe080947` |
| `QuizForge.Studio.Android.apk` | 3.53 МБ | `7fe44c1d41e821321853e9c0a82fdd9d5184d8d7066668086ad33510c36e5572` |
| `MindForge.Admin.zip` | 129.57 МБ | `27757d07039b0fedff6b1b71ac02a9482ebb5cfc566c5144d508bc3a80c5e1a2` |
| `MindForge.Admin.Android.apk` | 3.53 МБ | `f5bfd1375b69ea10a3c455b73e7f89db841df414613114dd8b4c2c3ab82b48fc` |

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