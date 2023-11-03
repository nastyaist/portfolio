GET - negative invalid id genre
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
- для id задать Value = "a~!@#$%^&()_+!“№;%:?()_+/,?><:”}{[];’,./<>"

3. Вкладка Authorization
ввести данные по авторизации - см. информацию по авторизации в предварительных условиях.

4. Вкладка Headers
- Столбец Key, значение = Accept
- Столбец Value, значение = application/json

5. Отправить запрос.

Ожидаемый результат
--
1. Status ответа: 400 Bad Request
2. В Body ответа вернулось:

```
{
    "id": "Неверное значение поля id."
}
```

Автор: Анастасия

Прохождение тест-кейса:
----------------

|**Дата**|**Время**|**Результат**|**Имя**|**Баг № Trello**|
| :-: | :-: | :-: | :-: | :-: |
|06-07-2023|14:21|FAILED|Анастасия|[404 ответ вместо 400 при вводе невалидных данных в запросе GET id genre](https://trello.com/c/WCqDvZz9/246-404-%D0%BE%D1%82%D0%B2%D0%B5%D1%82-%D0%B2%D0%BC%D0%B5%D1%81%D1%82%D0%BE-400-%D0%BF%D1%80%D0%B8-%D0%B2%D0%B2%D0%BE%D0%B4%D0%B5-%D0%BD%D0%B5%D0%B2%D0%B0%D0%BB%D0%B8%D0%B4%D0%BD%D1%8B%D1%85-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85-%D0%B2-%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81%D0%B5-get-id-genre)|
