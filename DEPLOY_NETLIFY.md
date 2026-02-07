# Деплой на Netlify

## Способ 1: Через Git (рекомендуется)

1. Создайте репозиторий на GitHub/GitLab/Bitbucket
2. Загрузите проект в репозиторий
3. Перейдите на [app.netlify.com](https://app.netlify.com)
4. **Add new site** → **Import an existing project**
5. Подключите Git-провайдера и выберите репозиторий
6. Настройки сборки оставьте пустыми (или используйте из `netlify.toml`):
   - **Build command:** пусто
   - **Publish directory:** `.` или оставить по умолчанию
7. Нажмите **Deploy site**

## Способ 2: Drag & Drop

1. Перейдите на [app.netlify.com](https://app.netlify.com)
2. Перетащите папку проекта в область **Drag and drop your site output folder here**
3. Netlify загрузит файлы и выдаст ссылку на сайт

> ⚠️ Папку `требования/` можно исключить из загрузки — она не нужна для работы сайта. При использовании Git добавьте её в `.gitignore`.

## Что подготовлено

- **netlify.toml** — конфигурация для Netlify (пустой build, publish из корня)
- **404.html** — кастомная страница «Страница не найдена»
- **.gitignore** — исключает лишние файлы при работе с Git

## Домен

После деплоя сайт будет доступен по адресу вида `random-name-123.netlify.app`. В настройках Netlify можно подключить свой домен.
