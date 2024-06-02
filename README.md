# Telegram Bot с функциями TTS и STT

Этот проект представляет собой Telegram бот, который использует функции преобразования текста в речь (TTS) и речи в текст (STT). Бот также взаимодействует с моделью GPT для обработки и генерации текстовых ответов.

## Функции

- Обработка текстовых сообщений и генерация ответов с помощью модели GPT.
- Преобразование текста в голосовые сообщения.
- Преобразование голосовых сообщений в текст.
- Ведение логов активности бота.
- Ограничение количества пользователей и использование токенов.

## Требования

### Общие требования

- **Python**: Версия 3.7 или выше.
- **Токен Telegram**: Получите токен у BotFather в Telegram.
- **Учетные данные Yandex Cloud**: Для использования сервисов Yandex для TTS и STT.

### Установка зависимостей

Используйте `pip` для установки необходимых пакетов:

pip install -r requirements.txt

#### Конфигурация
Создайте файл config.py с необходимыми конфигурациями:

# config.py

TELEGRAM_TOKEN = 'your-telegram-bot-token'
LOGS = 'path/to/your/logfile.log'
COUNT_LAST_MSG = 5  # или любое другое число

##### Запуск бота
Запустите скрипт бота командой:

python bot.py
###### Структура проекта
bot.py: Главный скрипт бота.
config.py: Файл конфигурации.
yandex_gpt.py: Модуль для взаимодействия с моделью GPT.
speechkit.py: Модуль для преобразования текста в речь и речи в текст.
database.py: Модуль для работы с базой данных.
validators.py: Модуль для валидации данных и ограничений.
###### Команды
/start и /help: Отправка приветственного сообщения.
/debug: Отправка файла логов.
/tts: Включение режима преобразования текста в речь.
/stt: Включение режима преобразования речи в текст.
