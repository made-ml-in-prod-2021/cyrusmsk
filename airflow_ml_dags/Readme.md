# Homework 3

Запуск Airflow:
```docker-compose up --build```

Остановка Airflow:
```docker-compose down```

Для использования в Windows необходим код в .env:
```COMPOSE_CONVERT_WINDOWS_PATHS=1```

Для работы оповещений также в файл .env необходимо определить параметры почты:
```MAIL_USERNAME=*** MAIL_PASSWORD=***```

Для корректного старта Airflow через docker в дистрибутивах linux: Arch, Manjaro перед запуском также необходимо стартовать демон докера, который не запущен по умолчанию:
```systemctl enable --now docker```

или просто
```systemctl start docker```

В качестве модели использовись данные из sklearn по классификации цифр.
Изначально начинал делать на Windows, но в Linux запуск значительно проще.
Единственное, что на стареньком ноутбуке (с Core2Duo и 4Gb памяти) делать это всё достаточно больно и медленно :(
Последние исправления вносились на макбуке - с одной стороны хорошо, что докер кросс-платформенный, с другой стороны проблем у него тоже хватает - словил пару вопросов и в issues примеров достаточно.

## Самооценка
```
  0  Выбрана папка
+ 5  DAG генерации данных
+ 10 DAG ппроцесс обучения модели
+ 5  DAG генерации и хранения предиктов
+ 3  Настроил сенсоры
+ 10 Все DAGи через докеры
- 0  Тесты не готовы
+ 0' Нет MLFlow
+ 0' Нет Mlflow Model Registry
+ 3' Настроил alert
+ 1  Самооценочка
-------------------------------------------------------------------------------------
```
**ИТОГО: 34 / 36 базовых баллов + 3 / 16 дополнительных =** `37 / 52 баллов`