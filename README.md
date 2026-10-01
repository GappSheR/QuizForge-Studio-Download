# MindForge - загрузка

Репозиторий сайта загрузки MindForge. Файлы раздаются как вложения GitHub Release.

| Файл | Размер | SHA-256 |
|---|---|---|
| `MindForge.Quiz.zip` | 129.56 МБ | `c69c550d7b8982c06cf158f11de406e38afb4e2b6791a40d1f726f59770fbb4f` |
| `MindForge.Quiz.Android.apk` | 3.53 МБ | `ef40cc98fdddefa95537c659fc16bc837aeb35acce197ff6ccd2530fa962f299` |
| `QuizForge.Studio.zip` | 129.56 МБ | `67226447aa3f978522a730aac8ee3b86e902b76a90ad4b04c513f1c344da6747` |
| `QuizForge.Studio.Android.apk` | 3.53 МБ | `bb7669326b8eb1fabcc59cb3a28a402b53576921d735fcd66bae863a1192632c` |
| `MindForge.Admin.zip` | 129.57 МБ | `483826523ff1546ed02bf689b0f7fe946c3c26f3de899775064061a7ef019fbc` |
| `MindForge.Admin.Android.apk` | 3.53 МБ | `460e84f361ac5bd7fd8684774f339e18a117fc123ec65e0839cecf71c2e7e056` |

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