GET - reference genre list read
===

Предварительные условия
--
1. [Информация по авторизации](https://github.com/victoretc/GSPOTtestingdocumentation/blob/main/games/Authorization_data.md).
2. В БД есть два genre c name =:
- action
- приключения

Действия в Postman
--
1. Создать запрос
- метод - GET
- URL - games.alpha.g-spot.website/api/v1/reference/genre/

2. Вкладка Params / таблица Query Params
Проверить, что у limit и offset сняты чекбоксы.

3. Вкладка Authorization
ввести данные по авторизации - см. информацию по авторизации в предварительных условиях.

4. Отправить запрос

Ожидаемый результат
--
1. Status ответа: 201 OK.
2. В Body ответа вернулись id и name обоих жанров. Пример (id могут отличаться от приведённых ниже):

```
[
    {
        "id": 139,
        "name": "action"
    },
    {
        "id": 140,
        "name": "приключения"
    }
]
```

Автор: Анастасия

Прохождение тест-кейса:
----------------

|**Дата**|**Время**|**Результат**|**Имя**|**Баг № Trello**|
| :-: | :-: | :-: | :-: | :-: |
|08-07-2023|23:41|PASSED|Анастасия||