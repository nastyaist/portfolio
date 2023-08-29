GET - positive limit offset list
===

Предварительные условия
--
1. [Информация по авторизации](https://github.com/victoretc/GSPOTtestingdocumentation/blob/main/games/Authorization_data.md).
2. В БД 13 жанров, первые три жанра = admit, maybe, stringasd.

Действия в Postman
--
1. Создать запрос
- метод - GET
- URL - games.alpha.g-spot.website/api/v1/reference/genre/?limit=10&offset=2

2. Вкладка Authorization
ввести данные по авторизации - см. информацию по авторизации в предварительных условиях.

3. Отправить запрос

Ожидаемый результат
--
- Status: 200 OK
- В теле ответа: results содержат 10 жанров, начиная с жанра stringasd.

Автор: Анастасия

Прохождение тест-кейса:
----------------

|**Дата**|**Время**|**Результат**|**Имя**|**Баг № Trello**|
| :-: | :-: | :-: | :-: | :-: |
|09-07-2023|13:45|PASSED|Анастасия||