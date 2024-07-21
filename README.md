# ---
Телеграм-бот для мониторинга системы

Телеграм-бот для мониторинга параметров системы, таких как температуры CPU и GPU, использование CPU и памяти, а также состояния дисплея. Бот также может выполнять различные системные операции, такие как включение/выключение дисплея, выключение системы, блокировка экрана и другие.
Возможности

    Мониторинг состояния системы:
        Проверка температур CPU и GPU.
        Мониторинг использования CPU и памяти.

    Управление дисплеем:
        Включение или выключение дисплея.
        Отображение текста на весь экран.

    Системные операции:
        Выключение системы.
        Блокировка экрана.
        Выполнение системных команд.
        Закрытие Firefox.

    Уведомления:
        Получение уведомлений при превышении температур CPU или GPU.
        Получение уведомлений при превышении использования CPU или памяти.

Требования

    Python 3.7 или выше
    Библиотека python-telegram-bot
    Библиотека psutil
    zenity (для отображения текста на весь экран)
    nvidia-smi (для температуры GPU, если применимо)
    sensors (для температуры CPU)
    xset (для управления дисплеем)
    loginctl (для управления блокировкой экрана)

Установка

    Клонируйте репозиторий:

    bash

git clone https://github.com/yourusername/system-monitoring-telegram-bot.git
cd system-monitoring-telegram-bot

Создайте виртуальное окружение (опционально, но рекомендуется):

bash

python -m venv venv
source venv/bin/activate  # Для Windows используйте `venv\Scripts\activate`

Установите необходимые пакеты:

bash

pip install -r requirements.txt

Настройте переменные окружения:

Создайте файл .env в корневом каталоге и добавьте токен вашего Телеграм-бота:

env

TELEGRAM_BOT_TOKEN=ваш_токен_телеграм_бота_здесь

Запустите бот с правами root:

bash

    sudo python your_script_name.py

Использование

    Запустите бота, отправив команду /start в Телеграм.
    Используйте интерактивное меню для:
        Мониторинга параметров системы
        Управления настройками дисплея
        Выполнения системных операций
        Выполнения команд
        Отображения текста на весь экран

Настройка

    Порог температуры CPU: Установите в коде (CPU_TEMP_THRESHOLD).
    Порог температуры GPU: Установите в коде (GPU_TEMP_THRESHOLD).
    Порог использования CPU: Установите в коде (CPU_USAGE_THRESHOLD).
    Порог использования памяти: Установите в коде (MEMORY_USAGE_THRESHOLD).

Вы можете изменить пороги и функциональность по своему усмотрению.
