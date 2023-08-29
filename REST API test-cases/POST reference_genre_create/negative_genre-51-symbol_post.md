POST genre 51 symbols
===

Предварительные условия
--

1. [Информация по авторизации](https://github.com/victoretc/GSPOTtestingdocumentation/blob/main/games/Authorization_data.md).
2. Тестовые данные:

name = "cFp167Q02928SxOfCzxCTZJ7kXDRovkrIycasKZv7tdbSM94hDd"

id - не меняем.

Действия в Postman
--
1. Создать запрос
- метод - POST
- URL - games.alpha.g-spot.website/api/v1/reference/genre/

2. Вкладка Authorization
ввести данные по авторизации - см. информацию по авторизации в предварительных условиях.

3. Вкладка Body
- выбрать тип raw
- выбрать формат JSON
- тело запроса:

```json
{
  "name": "cFp167Q02928SxOfCzxCTZJ7kXDRovkrIycasKZv7tdbSM94hDd",
  "id": "<integer>"
}
```

4. Отправить запрос

Ожидаемый результат
--

1. Status ответа: 400 Bad Request.
2. В ответе вернулось:

```
{
    "name": [
        "Убедитесь, что это значение содержит не более 50 символов."
    ]
}
```

Автор: Анастасия

Прохождение тест-кейса:
----------------

|**Дата**|**Время**|**Результат**|**Имя**|**Баг № Trello**|
| :-: | :-: | :-: | :-: | :-: |
|27.06.2023|19:15|Passed|Анастасия|-|