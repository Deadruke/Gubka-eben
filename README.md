# Gubka-eben

Простой Telegram-бот на Python с использованием **pyTelegramBotAPI** (telebot).

## Функционал

- `/start` — приветственное сообщение
- Любое текстовое сообщение — бот повторяет его с префиксом «Ты написал:»

## Требования

- Python 3.10+
- Токен бота от [@BotFather](https://t.me/BotFather)

## Установка

1. Клонируйте репозиторий:
   ```bash
   git clone https://github.com/Deadruke/Gubka-eben.git
   cd Gubka-eben
   ```

2. Создайте виртуальное окружение и установите зависимости:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/macOS
   # venv\Scripts\activate   # Windows
   pip install -r requirements.txt
   ```

3. Создайте файл `.env` в корне проекта и добавьте туда токен:
   ```env
   TELEGRAM_TOKEN=ваш_токен_от_BotFather
   ```

## Запуск на Render (Web Service)

1. **Type:** Web Service (не Background Worker!)
2. **Build Command:** `pip install -r requirements.txt`
3. **Start Command:** `python main.py`
4. **Environment Variables:**
   - `TELEGRAM_TOKEN` — токен бота
   - `RENDER_EXTERNAL_URL` — автоматически устанавливается Render (например, `https://gubka-eben.onrender.com`)
5. Деплой.

## Запуск локально

```bash
python main.py
```

Бот будет работать в режиме long polling.

## Структура проекта

```
Gubka-eben/
├── main.py           # Точка входа, код бота
├── requirements.txt  # Зависимости
├── .env              # Переменные окружения (не коммитится)
└── README.md         # Этот файл
```

## Примечания

- Токен **никогда не коммитите** в репозиторий. Используйте `.env` (добавлен в `.gitignore` при необходимости).
- Для Render Web Service бот использует `flask` для обработки вебхуков, что позволяет избежать ошибок `metadata-generation-failed` и `maturin`, связанных с `aiogram`.
- Если вы хотите использовать `aiogram` на Render, вам понадобится платный тариф или VPS с записью в файловую систему.