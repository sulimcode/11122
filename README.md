# Исламское Приложение для Молитв

Веб-приложение для мусульман, которое показывает точное время молитв на основе местоположения пользователя.

## Функции

- Отображение времен молитв для текущего дня
- Просмотр ежемесячного календаря молитв
- Автоматическое определение местоположения пользователя
- Поиск мест и просмотр популярных мест
- Обратный отсчет до следующей молитвы
- Многоязычная поддержка
- Тёмная и светлая темы

## Переменные окружения

Для работы приложения необходимо настроить следующие переменные:

- `DATABASE_URL` - URL для подключения к PostgreSQL базе данных (обязательно)
- `IP_INFO_API_KEY` - API ключ для сервиса [ipinfo.io](https://ipinfo.io) (для геолокации IP, опционально)
- `NODE_ENV` - среда выполнения (development или production)

## Технологии

- Frontend: React, TypeScript, Tailwind CSS, shadcn/ui
- Backend: Express, Node.js
- База данных: PostgreSQL с Drizzle ORM
- API: Prayer Times API, Geocoding API

## Разработка

```
npm install
npm run dev
```

## Деплой на Vercel

Это приложение оптимизировано для деплоя на Vercel. Выполните следующие шаги:

1. Подключите репозиторий через панель управления Vercel
2. Настройте переменные окружения:
   - `DATABASE_URL` - URL для подключения к PostgreSQL базе данных (например, Neon, Supabase, Railway)
   - `IP_INFO_API_KEY` - API ключ для сервиса ipinfo.io (опционально)
   - `NODE_ENV` - установите в `production`

3. После успешного деплоя, выполните миграцию базы данных:
   ```bash
   npx drizzle-kit push
   ```

4. Приложение будет доступно по URL, предоставленному Vercel