# Практическая работа №3. Wazuh

Выполнил Сердюков Матвей, ББМО-01-23

## Подготовка стенда, создание виртуальных машин

![](./screenshots/01-vm.png)

## Установка сервера Wazuh

![](./screenshots/02-install.png)

![](./screenshots/03-dashboard.png)

## Установка агента Wazuh

![](./screenshots/04-agent-install.png)

![](./screenshots/05-agent.png)

![](./screenshots/06-agent.png)

## Подключенный агент в дашборде

![](./screenshots/07-agent-ready.png)

## Найденные уязвимости в конфигурации по умолчанию

![](./screenshots/08-default-alerts.png)

## Настройка проверки целостности файлов

![](./screenshots/09-filecheck.png)

![](./screenshots/10-restart.png)

### Изменение конфигурационного файла `/etc/hosts`

![](./screenshots/11-edit-hosts.png)

### Срабатывание правила

![](./screenshots/12-file-alert.png)

## Настройка проверки уязвимостей

![](./screenshots/13-vulncheck.png)

## Настройка выявления скрытых процессов

### Установка необходимых пакетов

![](./screenshots/14-prepare-for-rootkit.png)

### Настройка мониторинга процессов в агенте Wazuh

![](./screenshots/15-configure-rootcheck.png)

### Сборка и запуск руткита

![](./screenshots/16-compile.png)

![](./screenshots/17-rootkit.png)

### Использование руткита для скрытия процесса

![](./screenshots/18-hide-proc.png)

### Срабатывание правила

![](./screenshots/19-alert.png)

## Настройка выявления SQL-инъекций

### Установка веб-сервера Apache

![](./screenshots/20-install-apache.png)

![](./screenshots/21-apache-installed.png)

![](./screenshots/22-apache-works.png)

### Конфигурация мониторинга логов Apache

![](./screenshots/23-enable-log-analysis.png)

### Демонстрационная атака

![](./screenshots/24-sqli.png)

### Срабатывание правила

![](./screenshots/25-alert.png)

## Проверка выявления атаки Shellshock

![](./screenshots/26-shellshock.png)

![](./screenshots/27-alert.png)
