# 1. Functional requirements

Для небольшого сайта, предназначенного для тренировки прохождения HR и технического собеседований, нужно было составить требования к функциональности.
Модули сайта:
а) Главная страница.
б) Этап прохождения собеседований.
в) Страницы "Поддержка" и "О нас".
г) Загрузка ответов и вопросов на платформу.

В портфолио приведены примеры составленных мною требований к модулям:
б) Этап прохождения собеседований.
г) Загрузка ответов и вопросов на платформу.

# 2. REST API test-cases
[REST API test-cases](https://github.com/nastyaist/portfolio/tree/main/REST%20API%20test-cases) - тестирование четырёх эндпойнтов (post, delete, get по id, get списка) для json-объекта "Жанр игры" (GenreGames) маркетплейса видеоигр.
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

P. S. [Swagger всего проекта](https://games.alpha.g-spot.website/swagger/). 

