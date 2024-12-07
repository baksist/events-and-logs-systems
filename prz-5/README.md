# Практическая работа №5. Threat Hunting

Выполнил Сердюков Матвей, ББМО-01-23

Для работы были использованы уже ранее созданные в [ПРЗ №3](../prz-3/) стенды Wazuh.

![](./screenshots/vmconnect_y3LMvKk6CP.png)

## Установка и настройка IDS Suricata

Добавление репозиториев `suricata` в пакетный менеджер `apt`:

![](./screenshots/vmconnect_hskFtg5UVw.png)

Установка IDS Suricata из репозитория:

![](./screenshots/vmconnect_ZZo0CtHTpK.png)

Загрузка правил обнаружения:

![](./screenshots/vmconnect_Ife4jPHgOj.png)

Настройка переменных конфигурации в файле `/etc/suricata/suricata.yaml`:

![](./screenshots/vmconnect_oRYm2H4QQO.png)

Настройка импорта логов Suricata в Wazuh и перезапуск агента:

![](./screenshots/vmconnect_4TojIz78qH.png)

![](./screenshots/vmconnect_FAs9COnmz6.png)

## Установка и настройка Yara

### Настройка агента

Загрузка и распаковка дистрибутива:

![](./screenshots/vmconnect_UwvIipoUNf.png)

Установка Yara:

![](./screenshots/vmconnect_liQg8VBizk.png)

![](./screenshots/vmconnect_jWnCNrKs6O.png)

![](./screenshots/vmconnect_Q5oqdrJrLv.png)

Загрузка YARA-правил:

![](./screenshots/vmconnect_WAHiNucv27.png)

Создание скрипта `yara.sh` для Wazuh и установка корректных привилегий согласно документации:

![](./screenshots/vmconnect_48PLim48iG.png)

Настройка правил мониторинга в файле `/var/ossec/etc/ossec.conf`, перезапуск агента:

![](./screenshots/vmconnect_z0cpgX3Lf8.png)

![](./screenshots/vmconnect_JqYOFah7j9.png)

### Настройка сервера

Настройка правил Wazuh для отслеживания изменений и срабатывания правил YARA:

![](./screenshots/WindowsTerminal_x83ampQmD3.png)

Настройка декодера результатов сканирования Yara:

![](./screenshots/WindowsTerminal_jb97X8Qtde.png)

Настройка команд Wazuh, который будут запускать сканирование при обнаружении изменений в отслеживаемой директории:

![](./screenshots/WindowsTerminal_EduUSQI5El.png)

Завершение конфигурации, перезапуск сервера Wazuh:

![](./screenshots/WindowsTerminal_gEW9JQ64tu.png)

## Эмуляция атаки

Для осуществления атак в гипервизоре также была развёрнута виртуальная машина с Kali Linux:

![](./screenshots/explorer_mvpRr5dgF2.png)

Для проверки работы IDS Suricata было запущено сканирование защищаемого узла сканером веб-уязвимостей `nuclei`:

![](./screenshots/vmconnect_WJXVKX9AGd.png)

События, созданные IDS Suricata:

![](./screenshots/uLpS4k5Wn6.png)

Эти события также можно отфильтровать, например, вывести только попытки эксплуатации уязвимостей (по тегу правила Suricata `ET EXPLOIT`).

![](./screenshots/firefox_2QKh2VMFhT.png)

Для проверки работы Yara средством `msfvenom` был создан реверс-шелл.

![](./screenshots/vmconnect_IhDHCM77l3.png)

Загрузка и запуск исполняемого файла:

![](./screenshots/vmconnect_pvyaWZyImR.png)

![](./screenshots/vmconnect_xpxHkjjOYH.png)

Сработка Yara-правила в Wazuh:

![](./screenshots/firefox_V9BuShkulF.png)
