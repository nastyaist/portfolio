#authorization

#На запрос с истекшим токеном admin возвращается ошибка аутентификации

#regression

## Предусловия
1. {{baseUrl}} взять из файла ...

## Шаги
1. Создать запрос
- метод - GET
- URL - {{baseUrl}}/admin/competence/
- Authorization:
Type: Bearer Token
Token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwidXNlcl9pZCI6IjIyMzQ1Njc4LTEyMzQtNTY3OC0xMjM0LTU2NzgxMjM0NTY3OCIsInVzZXJfcGVybWlzc2lvbnMiOlsiYWRtaW4iXSwiZXhwIjoxNjk3MTk1NDQ5fQ.d9BBlmlLkN-Qa2rwu_JowVYxAuk3XIYciw8qW6uxvaM

2. Отправить запрос

## Ожидаемый результат
1) Запрос успешно отправлен.
2) Статус-код ответа - 427.
3) Время ответа сервера - не превышает 500ms.
4) Response header ""Content-Type"" - ""application/json"".
5) В JSON присутствует ключ detail с описанием проблемы, пример:
{
    ""detail"": ""Token lifetime is expired""
}

### Автор: Анастасия

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Баг № Trello|
|     ---     |  ---  |    ---      |   ---  |      ---    |
|  2023-10-12 | 18:10 |passed| Анастасия    |ссылка на баг|