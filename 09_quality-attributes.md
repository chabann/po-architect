## Атрибуты качества для выделенных НФТ

### 1. Пользовательский домен

1. Время аутентификации пользователя ≤ 1 сек при 10 тыс. RPS (**Производительность**, **Масштабируемость**)
2. Шифрование персональных данных. Необходимо использование AES-256, соответствие Закону о защите персональных данных (**Безопасность**)
3. Защита от утечек паролей. В системе используется многофакторная авторизация (**Безопасность**)
4. Поддержка роста количества пользователей до 5 млн. без деградации скорости авторизации (**Производительность**, **Масштабируемость**)
5. Uptime ≥ 99.5% времени (**Надежность**)
6. Защита от DDoS-атак. Введение автоматического ограничения запросов (Rate Limiting) (**Безопасность**, **Надежность**)

---

### 2. Социальный домен

1. Задержка при отправке сообщений не превышает 500 мс при 50 тыс. активных пользователях (**Производительность**)
2. Поддерживается работа групп до 10 тыс. участников с синхронным обновлением ленты (**Производительность**)
3. При сбое сервера восстановление данных занимает не более 2 минут (**Доступность**)
4. Система должна поддерживать горизонтальное масштабирование, позволяя добавлять новые серверы для обработки увеличивающейся нагрузки при пиковых нагрузках (например, онлайн мероприятие) (**Масштабируемость**)

---

### 3. Тренировочный домен

1. Обработка данных с устройств в реальном времени (задержка ≤ 500 мс) (**Производительность**)
2. Погрешность трекинга GPS ≤ 5 метров (**Надежность**)
3. Поддерживается обработка более 1 млн. тренировок в день, хранение данных за 5 лет (**Производительность**)
4. В системе имеется возможность переключения на запасной сервис трекинга (**Надежность**)
5. В системе имеется возможность подключения упрощенной системы обработки получаемых данных при отказе ML-модели (**Надежность**)

---

### 4. Экипировочный домен

1. Загрузка каталога товаров занимает не более 2 сек при 100тыс. артикулов товаров (**Производительность**)
2. Время восстановления системы после сбоя не более 20 минут (**Доступность**)
3. Система должна поддерживать горизонтальное масштабирование, позволяя добавлять новые серверы для обработки увеличивающейся нагрузки (**Масштабируемость**)
4. Должна поддерживаться обработка более 10 тыс. запросов/мин в пиковые нагрузки (например, во время распродажи) (**Производительность**, **Масштабируемость**)

---

### 5. Маркетинговый домен

1. Для формирования / обновления пользовательских предложений за основу берется персональная истории активности (**Удобство использования, Гибкость**)
2. Локализация контента поддерживает не менее 10 регионов (**Удобство использования, Расширяемость**)
3. Должна быть возможность запустить промо-акции параллельно на нескольких инстансах сервиса для распределения нагрузок (**Масштабируемость, Гибкость**)
4. Система должна поддерживать ежегодный прирост количества участников акций пользователей на 20% и мгновенный на 60% (**Масштабируемость, Производительность**)

---

### 6. Интеграционный домен

1. Поддерживаются протоколы Bluetooth 5.0, ANT+, Wi-Fi Direct (**Взаимодействие с дургими системами, Конфигурируемость**)
2. При потере соединения с устройством более чем на 1 мин проводится синхронизации данных (**Надежность**)
3. Система поддерживает добавление интеграции с более 10 новыми моделями устройств в месяц без изменения API (**Расширяемость, Конфигурируемость**)
4. Поддерживается автоматический переход на запасной канал связи при сбоях соединения (**Надежность, Конфигурируемость**)

---

### 7. Финансовый домен

1. Операции оплаты поддерживают стандарт PCI DSS (**Безопасность, Надежность**)
2. Проведение транзакции  занимает не более 3 сек при 1 тыс. операций / сек (**Производительность, Производительность**)
3. Система должна быть способна поддерживать добавление более 3 валют и 5 платёжных систем в год (**Расширяемость, Взаимодействие с дургими системами**)
4. Подтверждение транзакций пользователем в ручном режиме (подключение второго фактора) (**Безопасность**)

---

### 8. Административный домен

1. Система поддерживает Управление доступом на основе ролей с не менее 5 уровнями для модераторов (**Безопасность, Конфигурируемость**)
2. Логи администрирования хранятся не менее 1 года (**Надежность**)
3. Система поддерживает работу более 100 модераторов без конфликтов (**Конфигурируемость, Расширяемость**)
4. Производится автоматическая блокировка подозрительных аккаунтов с последующим уведомлением администратора (**Безопасность**)

---

### 9. Дополнительные сервисы (уведомления, поиск)

1. Доставка уведомления занимает не более 3 сек для 95% пользователей (**Производительность**)
2. Релевантность информационного поиска составляет более 0.9 (**Удобство использования**)
3. Индексация данных (более 10 млн записей) в Elasticsearch должна занимать не более чем 2 часа (**Производительность**)
4. Доступно отключение отправки несущественных уведомлений при перегрузке (**Конфигурируемость, Надежность**)
5. Взаимодействие сервисов между собой в части сценариев происходит через брокер сообщений (**Взаимодействие с другими системами, Расширяемость**)
