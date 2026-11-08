# Gubka-eben

Простой Telegram-бот на Python с использованием **aiogram 3**.

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

## Запуск

```bash
python main.py
```

Бот начнет опрашивать обновления (long polling). Для остановки нажмите `Ctrl+C`.

## Структура проекта

```
Gubka-eben/
├── main.py           # Точка входа, код бота
├── requirements.txt  # Зависимости
├── .env              # Переменные окружения (не коммитится)
└── README.md         # Этот файл
```

## Примечания

- Токен **никогда не коммитьте** в репозиторий. Используйте `.env` (добавлен в `.gitignore` при необходимости).
- Бот использует `aiogram 3.13.1` и `python-dotenv` для загрузки переменных окружения.