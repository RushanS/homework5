# homework5

Интернет-магазин из предыдущих домашек растёт и развивается.
В нём уже много тысяч разных товаров. И постоянно появляются новые категории товаров.

Берём код из ДЗ 4.
Необходимо реализовать асинхронный перенос всех товаров из одной заданной категории в другую.
Нужно реализовать 2 http-метода.

### Создание задачи на перенос.
Метод принимает на вход два id: id из которой надо перенести товары, id категори в которую надо перенести.
Метод создаёт задачу для переноса, сам перенос должен выполняться асинхронно в фоне. Метод возвращает id задачи.

POST /move-products-task

Входные данные:

{
    "sourceCategoryId": 1
    "targetCategoryId": 2
}

Результат запроса:

{
    "taskId": 432
}

### Получение статуса запущенной задачи
GET /task-status?taskId=432

Результат запроса:

{
    "taskId": 432
    "taskStatus": WAITING / IN_PROGRESS / DONE / ERROR
}

### P.S
Мерж-реквест с решением не должен содержать в себе вспомогательные файлы,такие как mvnw, mvnw.cmd, gradlew и т.д.
Их можно один в начале раз закоммитить в мастер.
Код из предыдущих домашек так же можно сразу закоммитить в мастер.
Желательно, чтобы мерж-реквест содержал в себе только то, что относится к этой домашке.

Не забывайте про принципы SOLID, особеннно про принцип единой ответственности.
Логика по асинхронной обработке задач не должна быть перемешана с бизнес-логикой продуктов и котегорий.





