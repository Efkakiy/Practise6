# Используем образ Ubuntu
FROM ubuntu:latest
# Эта строка выполняет команды внутри контейнера. Она обновляет списки пакетов APT (Advanced Package Tool) с помощью apt-get update, а затем устанавливает пакеты x11-apps и xauth с помощью apt-get install -y. Параметр -y указывает на автоматическое подтверждение установки без запросов подтверждения. После установки пакетов, команда rm -rf /var/lib/apt/lists/* удаляет списки пакетов APT для экономии места.
RUN apt-get update && apt-get install -y \
x11-apps \
xauth \
&& rm -rf /var/lib/apt/lists/*
# Эта строка устанавливает переменную среды DISPLAY в значение :0. Переменная DISPLAY используется для указания дисплея X-сервера, к которому приложения могут подключаться.
ENV DISPLAY=:0
# Эта строка определяет команду, которая будет выполняться при запуске контейнера.
CMD ["xeyes"]