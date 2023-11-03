# 1. Functional requirements

Для небольшого сайта, предназначенного для тренировки прохождения HR и технического собеседований, нужно было составить требования к функциональности.
Модули сайта:
1) Главная страница.
2) Этап прохождения собеседований.
3) Страницы "Поддержка" и "О нас".
4) Загрузка ответов и вопросов на платформу.

В портфолио приведены примеры составленных мною требований к модулям:
- Этап прохождения собеседований (interviewing stage).
- Загрузка ответов и вопросов на платформу (uploading questions and answers to the website).


# 2. REST API test-cases
Для маркетплейса видеоигр необходимо было протестировать бэкэнд. В портфолио приведены примеры REST API тест-кейсов для 4-х эндпойнтов (post, delete, get по id, get списка) для json-объекта "Жанр игры" (GenreGames).
```
{
id	integer
        title: ID
        readOnly: true
name*	string
        title: Genre
        maxLength: 50
        minLength: 1
}
```

# 3. API test-cases - Authorization
[API test-cases - Authorization](https://github.com/nastyaist/portfolio/tree/main/REST%20API%20test-cases) - тестирование эндпойнта POST /auth/login для двух пользователей - юзер и админ, проверка выданных прав.
```
{
  "email": "string",
  "password": "string"
}
```
