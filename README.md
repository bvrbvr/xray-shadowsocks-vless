# Disclaimer

В соответствии с новыми законами Российской Федерации, я должен предупредить вас, что **не рекомендую** использовать полученную вами информацию для посещения web сайтов заблокированных на территории Российской Федерации!
Вся предоставленная информация должна быть использована исключительно в целях **обучения**.

# Xray-Shadowsocks-VLESS

Простая "однокликовая" установка сервера Xray в Docker-контейнере.

## Как использовать

1. Запустите скрипт командой:  
   ```bash
   ./deploy.sh

# Main deploy.sh options
`./deploy.sh` script could be executed with special options
* `reload` — очистить и перезапустить инициализацию Xray-контейнера.
* `remove` - удалить контейнер Xray и его образ.
* `restart` - пересоздать контейнер (все настройки сохранятся).
* `uuid` - получить случайный UUID (работает только если контейнер запущен).
* `your@email.com` - указать ваш email для конфигурационного файла Xray.

Если скрипт запускается впервые, он соберет Docker-образ, запустит контейнер Xray и выведет данные для клиентской конфигурации.
При повторном запуске без параметров скрипт просто покажет данные для клиентской конфигурации.
Важно: Если вы укажете email как параметр, это всегда приведет к перезагрузке сервера Xray, и данные для клиентской конфигурации изменятся.

**WARN** Сервер имитирует обычный веб-сайт. Для этого при запуске случайным образом выбирается один адрес из файла `fake_sites.txt`
