# nodejs-hw

Мінімальний Express-сервер для роботи з колекцією нотаток.

## Запуск

```bash
npm install
npm run dev   # режим розробки (nodemon)
npm start     # звичайний запуск
```

У корені проєкта створіть файл `.env`:

```
PORT=3000
```

## Маршрути

| Метод | Шлях              | Опис                                     |
| ----- | ----------------- | ---------------------------------------- |
| GET   | `/notes`          | `{ "message": "Retrieved all notes" }`   |
| GET   | `/notes/:noteId`  | `{ "message": "Retrieved note with ID: …" }` |
| GET   | `/test-error`     | Навмисно кидає помилку для перевірки 500 |

Будь-який інший шлях повертає 404 з повідомленням `Route not found`.

## Стек

- express
- cors
- dotenv
- pino-http
- nodemon, eslint (dev)
