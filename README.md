# MindForge - загрузка

Репозиторий сайта загрузки MindForge. Файлы раздаются как вложения GitHub Release.

| Файл | Размер | SHA-256 |
|---|---|---|
| `MindForge.Quiz.zip` | 129.56 МБ | `6c83593fe079153af44d2df0976cebe2a599d296a64df1411aa37d3230558765` |
| `MindForge.Quiz.Android.apk` | 3.53 МБ | `f39a7f1a9f45319497273a9b0b994adc51ac116783eb852ff559001411037045` |
| `QuizForge.Studio.zip` | 129.56 МБ | `6cd469141b3cfaeb488068c8040d6631f7304fd551196a4bdcf9f268ad876c69` |
| `QuizForge.Studio.Android.apk` | 3.53 МБ | `c7f4e8f183017bdcffa6478f3f29a603b117acd969dbc4f60e7e407bc6534f6e` |
| `MindForge.Admin.zip` | 129.57 МБ | `178362f0320f018e14193af79ff9c4fb6190c29c0bbe638f7f2bff1e3b823c27` |
| `MindForge.Admin.Android.apk` | 3.53 МБ | `9c57fae424c5e7190aefbbaf21f3cb7f14dc7d2bed1ec0a56946069a2ac5c7e8` |

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