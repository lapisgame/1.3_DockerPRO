В данном проекте используется Docker-compose для поочередного разворачивания двух приложений:

  1) База данных Postgres, со следующими данными для входа
   
    - Username = username
  
    - Password = secret
  
    - DB_name = database
  
    И инициализирующим скриптом init.sql

  2) Запуск Python скрипта, который выводит данные из БД в консоль


-------------------------------------------------------------


ЗАПУСК

Для корректного запуска рекомендуется сначала собрать Контейнер

*docker-compose build* (в данной директории)

После чего запустить непосредственное выполнение, если этого не произошло автоматически

*docker-compose up*

Результат выполнения Python скрипта можно будет увидеть в консоли, где и производился запуск

Проверить правильность при необходимости возможно путем подключение к БД по выше описанным данным