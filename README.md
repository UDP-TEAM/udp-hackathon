# UDP Hackathon

> TODO: придумается

## Репозитории

| Репозиторий | Назначение |
|---|---|
| [udp-hackathon](https://github.com/UDP-TEAM/udp-hackathon) | Бэкенд |
| [udp-frontend](https://github.com/UDP-TEAM/udp-frontend) | Фронтенд |

Задачи: [доска проекта](https://github.com/orgs/UDP-TEAM/projects/1)

## Запуск

### 1. Клонировать обе репы в одну папку

```bash
git clone https://github.com/UDP-TEAM/udp-hackathon.git
git clone https://github.com/UDP-TEAM/udp-frontend.git
```

Структура должна получиться такой:

```
your_folder/
├── udp-hackathon/
└── udp-frontend/
```

### 2. Запустить

TODO: команды запуска бэкенда и фронтенда.

После запуска:
- фронтенд: (адрес)
- бэкенд: (адрес)

## Правила работы

### Ветки

| Ветка | Назначение |
|---|---|
| `main` | Стабильная версия (надеюсь). Изменения только через PR из `dev` с 1 approve |
| `dev` | Рабочая ветка (по умолчанию), сюда вливаются все задачи |
| `feat/<номер>-<описание>` | Новая функция, например `feat/11-make-authentication` |
| `fix/<номер>-<описание>` | Исправление, например `fix/4-change-error-code` |

Номер берётся из issue на доске(Навреное)

### Процесс

1. Взять задачу на доске и перевести её в **In Progress**.
2. Создать ветку от свежего `dev`:

```bash
   git checkout dev
   git pull
   git checkout -b feat/12-login-form
```

3. Сделать коммиты и запушить ветку:

```bash
   git add .
   git commit -m "Добавлена форма логина"
   git push -u origin feat/12-login-form
```

4. Открыть PR в `dev`, в описании указать `Closes #номер задачи`. Ревью по желанию.
5. Мелкие правки можно пушить в `dev` напрямую, но сначала обязательно `git pull`.
6. Когда `dev` стабильна, открываем PR `dev → main`, нужен 1 approve.

### Важно

- Перед пушем всегда делаем `git pull`.
- Не пушим код, который не запускается.
- Никогда не используем `git push --force` в `dev` и `main`.
- Не коммитим `.env`, ключи и пароли (если будут)
- Перед правкой общих файлов (`package.json`, конфиги, `.env.example`) предупреждаем в чате.
- Открыл PR — написал в чат (по возможности)
