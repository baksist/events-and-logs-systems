# Практическое задание №1. Сбор логов

Выполнил Сердюков Матвей, группа ББМО-01-23

## `rsyslog`

### Установка `rsyslog` на сервер

![](screenshots/01-install-rsyslog-server.png)

![](screenshots/02-rsyslog-running.png)

### Настройка модулей `rsyslog`

![](screenshots/03-load-modules.png)

### Добавление правил обработки логов

![](screenshots/04-add-ruleset.png)

### Применение конфигурации `rsyslog`

![](screenshots/05-apply-config.png)

### Установка `rsyslog` на клиент

![](screenshots/06-install-rsyslog-client.png)

![](screenshots/07-client-rsyslog-running.png)

### Добавление правила пересылки логов на сервер

![](screenshots/08-add-client-rule.png)

### Применение конфигурации `rsyslog`

![](screenshots/09-apply-client-config.png)

### Просмотр полученных логов на сервере

![](screenshots/10-logs-recieved.png)

## Grafana Loki

### Загрузка compose-файла от разработчика

![](screenshots/11-download-loki-compose.png)

### Редактирование compose-файла с целью отключения компонента `promtail` на сервере

![](screenshots/12-edit-compose.png)

### Запуск Loki

![](screenshots/13-start-loki.png)

### Редактирование конфигурации `promtail` на клиенте

![](screenshots/14-promtail-config.png)

### comopose-файл для `promtail`

![](screenshots/15-promtail-compose.png)

### Запуск `promtail` на клиенте

![](screenshots/16-start-promtail.png)

### Просмотр логов клиента в Grafana

![](screenshots/17-viewing-logs.png)

## Signoz

### Запуск Signoz

Установка согласно https://signoz.io/docs/install/docker/#install-signoz-using-docker-compose

![](screenshots/18-start-signoz.png)

### Рабочая панель Signoz

![](screenshots/19-open-signoz.png)

### Редактирование конфигурации клиентского приложения для отправки данных в Signoz

Используемое приложение - https://github.com/SigNoz/sample-nodejs-app/

![](screenshots/20-update-compose-client.png)

### Запуск клиентского приложения

![](screenshots/21-start-client.png)

### Информация о приложении в Signoz

![](screenshots/22-dashboards.png)

![](screenshots/23-traces.png)
