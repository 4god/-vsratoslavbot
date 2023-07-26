# Клон телеграм-бота @vsratoslavbot

Бот получает от пользователя картинку, выбирает из файла-сборника случайную подпись и рисует её на картинке пользователя. Полученную картинку бот отправляет пользователю и предлагает ей поделиться в публичном канале.

## Использование

Клонируем репозиторий
```
git clone https://github.com/r4hx/ptlab-test.git
```
Переходим в рабочий каталог
```
cd ptlab-test
```
Устанавливаем виртуальное окружение
```
python3 -m venv venv
```
Активируем его
```
source venv/bin/activate
```
Устанавливаем зависимости
```
pip install -r requirements.txt
```
Для полноценной работы бота, ему необходимо передать значение переменных окружения

- **TOKEN** - токен вашего бота
- **TEXT_FILE** - файл со списком фраз (по умолчанию: **text.txt**)
- **IMAGE_DIR** - каталог с изображениями пользователей (по умолчанию: **images**)
- **FONT_FILE** - файл шрифта (по умолчанию: **Lobster-Regular.ttf**)
- **REPOST_CHANNEL** - идентификатор канала для репостов(отрицательное число)



## Запуск с помощью docker-контейнера

В директории с проектом лежит Dockerfile, в котором необходимо указать переменные окружения. После указания переменных переходим к сборке.

```shell
docker build -t ptlab .
```

Для запуска выполните команду

```shell
docker run ptlab
```

