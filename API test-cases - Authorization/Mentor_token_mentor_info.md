#authorization

#На запрос с валидным токеном mentor возвращается информация о mentor

#smoke

## Предварительные условия
1. Корректные данные для авторизации ...
2. {{baseUrl}} взять из файла ...

## Шаги
1. Создать запрос
- метод - POST
- URL - {{baseUrl}}/auth/login
- body 
{
  "email": "string",
  "password": "string"
}

email и password заполнить данными для аутентификации ментора (см. предварительные условия).
- выбрать формат данных raw / JSON

2. Отправить запрос

3. Из JSON ответа сохранить access-токен.

Пример:
"access": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsInVzZXJfaWQiOiIxMjM0NTY3OC0xMjM0LTU2NzgtMTIzNC01Njc4MTIzNDU2NzgiLCJ1c2VyX3Blcm1pc3Npb25zIjpbIm1lbnRvciJdLCJleHAiOjE2OTcyNzUxOTl9.hgw20vaKtuaAP328xNxTAuq2KCuugZSTZKEK2SkCZhQ"

4. Создать запрос
- метод - GET
- URL - http://82.147.71.207:8000/mentor/profile/
- Authorization:
Type: Bearer Token
Token: вставить сохранённый на шаге 3 токен.

5. Отправить запрос

## Ожидаемый результат
1) Запрос успешно отправлен.
2) Статус-код ответа - 200.
3) Время ответа сервера - не превышает 500ms.
4) Response header "Content-Type" - "application/json".
5) Example value of JSON:
{
  "timezone": "(UTC-11:00) Midway Island",
  "position": "string",
  "site": "string",
  "about": "string",
  "dev_experience": 0,
  "mentor_experience": 0,
  "competencies": [
    {
      "competence_name": "string"
    }
  ],
  "skills": [
    {
      "skill_name": "string"
    }
  ],
  "can_help_with": [
    {
      "can_help_with_name": "string"
    }
  ],
  "who_can_help": [
    {
      "who_can_help_name": "string"
    }
  ],
  "companies": [
    {
      "name": "string",
      "site": "string",
      "position": "string",
      "started_working": "2023-10-13T09:23:05.959Z",
      "stopped_working": "2023-10-13T09:23:05.959Z"
    }
  ],
  "educations": [
    {
      "university": "string",
      "specialty": "string",
      "graduated": "2023-10-13T09:23:05.959Z"
    }
  ],
  "projects": [
    {
      "name": "string",
      "url": "string",
      "value_on_project": "string"
    }
  ],
  "publications": [
    {
      "name": "string",
      "url": "string"
    }
  ],
  "courses": [
    {
      "name": "string",
      "description": "string",
      "link": "string"
    }
  ]
}

### Автор: Анастасия

### Тест выполнен
|     Дата    | Время | Результат   |   Имя  | Баг № Trello|
|     ---     |  ---  |    ---      |   ---  |      ---    |
|  2023-10-12 | 18:10 |passed| Анастасия    |ссылка на баг|