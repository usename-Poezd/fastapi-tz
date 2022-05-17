# Тех. Задание по Fast API
Необходимо реализовать простой сервис для постов

## Сущности
### Пользователть
Поля у пользователя:
 - UID
 - Имя
 - Email
 - Пароль(должен шифроваться)
 - Дата создание аккаунта

### Пост
Поля для поста:
 - Название
 - Описание
 - Картинка для анонса
 - Дата редактирования
 - Статус(Опубликован или нет)
 - UID пользователя, который добавил пост
 - Дата создания

## Роуты
### ```POST /auth/login```
Должен принимать запрос по входу в аккаунт по почте и паролю.
Выдавать назад должен юзера, у которого данные совпадают и JWT ключ для защиты других роутов(Которые будут доступны только авторизированным пользователям)

### ```POST /auth/login/registration```
Роут для регистрации пользователя.
Должен принимать необходимые поля для регистрации пользователя.

### ```GET /posts```
Выводит список всех постов с информацией о пользователе, который его добавил.

### ```GET /posts/{id}```
Возвращает пост по id.

### ```POST /posts```
Роут для добавленияя поста, должен вернуть информацию о добавленном посте

### ```PUT /posts/{id}```
Роут для обновления поста, должен вернуть информацию о обновленном посте

### ```DELETE /posts/{id}```
Роут для удаления поста по id.
