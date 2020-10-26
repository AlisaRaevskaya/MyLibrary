# MyLibrary<h5>Развертывание Symfony приложения из git репозитория</h5>

### Шаг 1 - клонирование проекта git

git clone https://github.com/AlisaRaevskaya/MyLibrary.git

### Шаг 2 -установка зависимостей проекта
Чтобы развернуть все нужные компоненты нужен composer. Качаем c [https://getcomposer.org/], ставим.

Открываем терминал в директории проекта symfony, запускаем команду:
`composer install`. 

### Шаг 3 - База данных
В файле-образце env. прописать данные подключения к бд.

Выполнить команду
`php bin/console doctrine:database:import dump.sql`


### Шаг 4 - очистить кэш

`php app/console cache:clear --env=prod --no-debug`

### Шаг 5 - проверить недостающие компоненты php система скажет чего не хватает и попросить поставить то что нужно
`php app/check.php`
