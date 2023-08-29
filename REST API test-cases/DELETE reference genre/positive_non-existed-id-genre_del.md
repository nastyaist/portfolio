DEL - non-existed id genre product 
===

Предварительные условия
--
1. [Информация по авторизации](https://github.com/victoretc/GSPOTtestingdocumentation/blob/main/games/Authorization_data.md).
2. В БД нет жанра c id = "1"

Действия в Postman
--
1. Создать запрос
- метод - GET
- URL - games.alpha.g-spot.website/api/v1/reference/genre/:id/?=1

2. Вкладка Authorization
ввести данные по авторизации - см. информацию по авторизации в предварительных условиях.

3. Отправить запрос

Ожидаемый результат
--
1. 404, Not Found
2. Тело ответа:

```
{
    "detail": "Страница не найдена."
}
```

Автор: Анастасия

Прохождение тест-кейса:
----------------

|**Дата**|**Время**|**Результат**|**Имя**|**Баг № Trello**|
| :-: | :-: | :-: | :-: | :-: |
|10-07-2023|18:01|PASSED|Анастасия||