GET - reference genre read
===

Предварительные условия
--
1. [Информация по авторизации](https://github.com/victoretc/GSPOTtestingdocumentation/blob/main/games/Authorization_data.md).

Действия в Postman
--
1. Создать жанр по [тест-кейсу](https://github.com/victoretc/GSPOTtestingdocumentation/blob/main/games/reference/reference_genre_create/positive_standard-name_post.md) с тестовыми данными:
- name = "action"
- id - не меняем.

2. Сохранить id нового жанра.

3. Создать запрос
- метод - GET
- URL - games.alpha.g-spot.website/api/v1/reference/genre/:id/

4. Вкладка Params / таблица Path Variables
- для id задать Value = id созданного в п. 1 жанра

4. Вкладка Authorization
ввести данные по авторизации - см. информацию по авторизации в предварительных условиях.

5. Вкладка Headers
- Значение Key = Accept
- Значение Value = application/json

6. Отправить запрос

Ожидаемый результат
--
1. Status ответа: 201 OK.
2. В Body ответа вернулись id и name жанра. Пример:

```
{
    "id": 3,
    "name": "action"
}
```

Автор: Анастасия

Прохождение тест-кейса:
----------------

|**Дата**|**Время**|**Результат**|**Имя**|**Баг № Trello**|
| :-: | :-: | :-: | :-: | :-: |
|06-07-2023|15:06|PASSED|Анастасия||