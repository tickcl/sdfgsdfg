# Базовий образ
FROM ubuntu:latest

# Встановлення залежностей
RUN apt update && apt install -y git docker.io docker-compose

# Клонування MailCow
RUN git clone https://github.com/mailcow/mailcow-dockerized.git /mailcow-dockerized

# Налаштування робочої директорії
WORKDIR /mailcow-dockerized

# Генерація конфігурації
RUN ./generate_config.sh

# Запуск MailCow
CMD ["docker-compose", "up", "-d"]
