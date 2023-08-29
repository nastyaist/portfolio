POST negative existing name homonyms
===

Предварительные условия
--

1. [Информация по авторизации](https://github.com/victoretc/GSPOTtestingdocumentation/blob/main/games/Authorization_data.md).
2. В базе данных есть жанр с именем "экшн".
3. Тестовые данные:

name = "Экшн"

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
  "name": "Экшн",
  "id": "<integer>"
}
```

4. Отправить запрос

Ожидаемый результат
--

1. Status ответа: 400 Bad Request.
2. Вернулся ответ:

```
{
    "name": [
        "genre с таким Genre уже существует."
    ]
}
```

Автор: Анастасия

Прохождение тест-кейса:
----------------

|**Дата**|**Время**|**Результат**|**Имя**|**Баг № Trello**|
| :-: | :-: | :-: | :-: | :-: |
|27.06|19:08|Failed|Анастасия|[Можно создать Genres с омонимичными names, введённых в разных регистрах](https://trello.com/c/oQD7Qyzp/234-%D0%BC%D0%BE%D0%B6%D0%BD%D0%BE-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D1%82%D1%8C-genres-%D1%81-%D0%BE%D0%BC%D0%BE%D0%BD%D0%B8%D0%BC%D0%B8%D1%87%D0%BD%D1%8B%D0%BC%D0%B8-names-%D0%B2%D0%B2%D0%B5%D0%B4%D1%91%D0%BD%D0%BD%D1%8B%D1%85-%D0%B2-%D1%80%D0%B0%D0%B7%D0%BD%D1%8B%D1%85-%D1%80%D0%B5%D0%B3%D0%B8%D1%81%D1%82%D1%80%D0%B0%D1%85)|
