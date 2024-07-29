# Система управления пользователями

Это система управления пользователями, построенная на основе Spring Boot. Она позволяет выполнять CRUD-операции с пользователями и ролями, а также предоставляет простой веб-интерфейс для их управления.

## Возможности
- Добавление, обновление, удаление пользователей.
- Назначение ролей пользователям.
- Добавление новых ролей.
- Обработка ошибок с помощью глобального обработчика исключений.
- Простой веб-интерфейс для управления пользователями.

## Начало работы

### Необходимые условия
- Java 11 или выше
- Maven
- База данных (например, MySQL, H2 и т.д.)

### Установка
1. Клонируйте репозиторий:
    ```sh
    git clone https://github.com/yourusername/user-management-system.git
    ```
2. Перейдите в директорию проекта:
    ```sh
    cd user-management-system
    ```
3. Обновите файл `application.properties` с настройками вашей базы данных:
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/yourdatabase
    spring.datasource.username=yourusername
    spring.datasource.password=yourpassword
    spring.jpa.hibernate.ddl-auto=update
    ```
4. Соберите проект:
    ```sh
    mvn clean install
    ```
5. Запустите приложение:
    ```sh
    mvn spring-boot:run
    ```

## Использование
После запуска приложения, откройте ваш веб-браузер и перейдите по адресу [http://localhost:8080/users](http://localhost:8080/users), чтобы получить доступ к интерфейсу управления пользователями.

## Структура проекта
- **Model**: Содержит классы сущностей `User` и `Role`.
- **Repository**: Содержит интерфейсы репозиториев `UserRepository` и `RoleRepository`.
- **Service**: Содержит класс сервиса `UserService` для бизнес-логики.
- **Controller**: Содержит `ViewController` для обработки веб-запросов и `GlobalExceptionHandler` для обработки исключений.
- **Configuration**: Содержит `WebConfig` для настройки скрытых HTTP-методов.
