#authorization

#Аутентификация с пустым email

#regression

## Предусловия
1. {{baseUrl}} взять из файла ...

## Шаги
1. Создать запрос
- метод - POST
- URL - {{baseUrl}}/auth/login
- body 
{
  "email": "",
  "password": "mentor"
}
- выбрать формат данных raw / JSON

2. Отправить запрос

## Ожидаемый результат
1) Запрос успешно отправлен.
2) Статус-код ответа - 422.
3) Время ответа сервера - не превышает 500ms.
4) Response header "Content-Type" - "application/json"
5) В JSON - присутсвует ключ detail с описанием проблемы.
 5.1) В JSON - присутствует ключ detail, с типом значения массив.
 5.2) В массиве есть обязательные поля type, loc, msg, input, url.
 5.3) В loc - указано, где находится ошибка. loc - является массивом
 5.4) В msg - пояснение к ошибке.
 5.5) В input - введённое значение.
 5.6) В type - указан тип ошибки
 5.7) В url - ссылка на https://errors.pydantic.dev

### Автор: Анастасия

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Баг № Trello|
|     ---     |  ---  |    ---      |   ---  |      ---    |
|  гггг-мм-дд | чч:мм |passed/failed| Имя    |ссылка на баг|