# MindForge - загрузка

Репозиторий сайта загрузки MindForge. Файлы раздаются как вложения GitHub Release.

| Файл | Размер | SHA-256 |
|---|---|---|
| `MindForge.Quiz.zip` | 129.56 МБ | `29b51c8af701bcc47da9590e6c581888c1763f171e41874c1e560d35739ad076` |
| `MindForge.Quiz.Android.apk` | 3.53 МБ | `03e98aec2c3060163b1615d9b914a6a1072ca5d78520001c81aa37216f8dbaf0` |
| `QuizForge.Studio.zip` | 129.56 МБ | `7779b8ba689bb21aab5858d7eb9d569aaf2f9550474603d6bffe37a8ec04917a` |
| `QuizForge.Studio.Android.apk` | 3.53 МБ | `c251ddd696f106b39ba73caa0410ee3bedabe831fe8574467d63b0d49fa869f6` |
| `MindForge.Admin.zip` | 129.57 МБ | `0af44dedd58d3bb5e736abde82acf410a3f2aafdd648f5ab1892ed199412259f` |
| `MindForge.Admin.Android.apk` | 3.53 МБ | `383d647137c2f65e4f369cba9ef3261dbf206d1018f0a2061802218a71828af7` |

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