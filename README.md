# MindForge - загрузка

Репозиторий сайта загрузки MindForge. Файлы раздаются как вложения GitHub Release.

| Файл | Размер | SHA-256 |
|---|---|---|
| `MindForge.Quiz.zip` | 129.56 МБ | `a6d744fd71267a8119c71a19904ba1ff0fcd33e18178c60ca15d12657496f66b` |
| `MindForge.Quiz.Android.apk` | 3.53 МБ | `7c042baf95e0329ee6d7036b50eeb1c4bd7a451fe86d7e0385d0726763745ed0` |
| `QuizForge.Studio.zip` | 129.56 МБ | `72aac687743975dcfef5970b2d6d551e96b0aa9438cd4735eac11669b9c3f651` |
| `QuizForge.Studio.Android.apk` | 3.53 МБ | `c67050d4fdef694de4708d4bea6fa53448d21d7a484909947ddca5555ba7c7db` |
| `MindForge.Admin.zip` | 129.57 МБ | `68804257b48fbc0c0382f7738247685d78fc91a83b07eacd0573d54151e7f821` |
| `MindForge.Admin.Android.apk` | 3.53 МБ | `edc976e1d33154a206e5770b7fd29e97e197fdab85f6217f121c60750a2d072d` |

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