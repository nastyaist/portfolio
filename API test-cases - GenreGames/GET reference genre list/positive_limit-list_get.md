GET - positive limit list
===

Предварительные условия
--
1. [Информация по авторизации](https://github.com/victoretc/GSPOTtestingdocumentation/blob/main/games/Authorization_data.md).
2. В БД 11 жанров.

Действия в Postman
--
1. Создать запрос
- метод - GET
- URL - games.alpha.g-spot.website/api/v1/reference/genre/?limit=10

2. Вкладка Authorization
ввести данные по авторизации - см. информацию по авторизации в предварительных условиях.

3. Отправить запрос

Ожидаемый результат
--
- results содержат 10 жанров
- next = ссылка на запрос для следующей строки
- previous = null

```
{
    "count": 11,
    "next": "https://games.alpha.g-spot.website/api/v1/reference/genre/?limit=10&offset=10",
    "previous": null,
    "results": [
        {
            "id": 139,
            "name": "admit"
        },
        {
            "id": 140,
            "name": "maybe"
        },
        {
            "id": 156,
            "name": "stringasd"
        },
        {
            "id": 157,
            "name": "string"
        },
        {
            "id": 99,
            "name": "Acti1245!@#$"
        },
        {
            "id": 100,
            "name": "!@#$"
        },
        {
            "id": 62,
            "name": "strin"
        },
        {
            "id": 101,
            "name": "下来顔文字"
        },
        {
            "id": 102,
            "name": "Հայկականتحتاجفقطإلىنسخלבדוק"
        },
        {
            "id": 103,
            "name": "En Ru"
        }
    ]
}
```

Автор: Анастасия

Прохождение тест-кейса:
----------------

|**Дата**|**Время**|**Результат**|**Имя**|**Баг № Trello**|
| :-: | :-: | :-: | :-: | :-: |
|09-07-2023|13:45|PASSED|Анастасия||