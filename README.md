# Ynamly CRM — коробочная версия

Установочный пакет Ynamly CRM для собственного сервера компании. Исходного кода здесь нет — только готовые релизы.

**Программа в пакете зашифрована.** Установить её можно только с паролем установки, который Ynamly Tor выдаёт клиенту вместе с договором. У каждой версии свой пароль. Пакет подписан ключом Ynamly Tor: изменённый или повреждённый пакет не установится.

## Требования

- Linux (Ubuntu 22.04+, Debian 12+), 4 ядра, 8 ГБ памяти, от 50 ГБ диска
- Docker Engine и Docker Compose (`docker-ce`, `docker-compose-plugin`), `openssl`, `curl`

## Установка

```sh
curl -LO https://github.com/vladimirsergacev025-jpg/ynamly-crm-box/releases/latest/download/ynamly-crm-box.tar
tar xf ynamly-crm-box.tar && cd ynamly-crm-box-*
sudo sh install.sh --url http://crm.company.tm
```

Установщик спросит пароль установки. Затем откройте `<адрес>/register` и создайте компанию.

Без лицензии CRM работает 30 дней, до 10 пользователей. Лицензию выдаёт Ynamly Tor по коду запроса из раздела «Лицензия».

## Обновление

Скачайте новый релиз, распакуйте и запустите из его папки `sudo sh update.sh` — он спросит пароль новой версии. Откат: `sudo sh /opt/ynamly-crm/update.sh --rollback`.

Подробная инструкция — `README.txt` внутри пакета.

---

© Ynamly Tor · https://ynamlycrm.com · Пакет распространяется только по лицензионному договору. Копирование, передача третьим лицам, изучение и изменение программы запрещены.
