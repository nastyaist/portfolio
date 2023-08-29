GET - negative zero id genre
===

Предварительные условия
--
1. [Информация по авторизации](https://github.com/victoretc/GSPOTtestingdocumentation/blob/main/games/Authorization_data.md).

Действия в Postman
--
1. Создать запрос
- метод - GET
- URL - games.alpha.g-spot.website/api/v1/reference/genre/:id/

2. Вкладка Params / таблица Path Variables
- для id задать Value = "0"

3. Вкладка Authorization
ввести данные по авторизации - см. информацию по авторизации в предварительных условиях.

4. Вкладка Headers
- Столбец Key, значение = Accept
- Столбец Value, значение = application/json

5. Отправить запрос.

Ожидаемый результат
--
1. Status ответа: 404 Not Found
2. В Body ответа вернулось:

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
|06-07-2023|15:31|PASSED|Анастасия||
