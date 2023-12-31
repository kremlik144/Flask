# Курс по основам Flask

### Home Work 1 - [more details](https://github.com/kremlik144/Flask/tree/main/HW_1)

Создать базовый шаблон для интернет-магазина, содержащий общие элементы дизайна (шапка, меню, подвал), и дочерние шаблоны для страниц категорий товаров и отдельных товаров. Например, создать страницы «Одежда», «Обувь» и «Куртка», используя базовый шаблон.

___



### Home Work 2 - [more details](https://github.com/kremlik144/Flask/tree/main/HW_2)

Создать страницу, на которой будет форма для ввода имени и электронной почты, при отправке которой 
- будет создан cookie-файл с данными пользователя
- будет произведено перенаправление на страницу приветствия, где будет отображаться имя пользователя.
- на странице приветствия должна быть кнопка «Выйти», при нажатии на которую будет удалён cookie-файл с данными пользователя и произведено перенаправление на страницу ввода имени и электронной почты.

___



### Home Work 3 - [more details](https://github.com/kremlik144/Flask/tree/main/HW_3)

Создать форму регистрации для пользователя.
- Форма должна содержать поля: имя, электронная почта, пароль (с подтверждением), дата рождения, согласие на обработку персональных данных.
- Валидация должна проверять, что все поля заполнены корректно (например, дата рождения должна быть в формате дд.мм.гггг).
- При успешной регистрации пользователь должен быть перенаправлен на страницу подтверждения регистрации.
- Поле пароль должно содержать не менее 8 символов, включая хотя бы одну букву и одну цифру.
- Если данные формы не прошли валидацию, на странице должна быть выведена соответствующая ошибка.
- При отправке формы данные должны сохраняться в базе данных, а пароль должен быть зашифрован.

___


### Home Work 4 - [more details](https://github.com/kremlik144/Flask/tree/main/HW_4)

Написать программу, которая скачивает изображения с заданных URL-адресов и сохраняет их на диск. Каждое изображение должно сохраняться в отдельном файле, название которого соответствует названию изображения в URL-адресе.
Например, URL-адрес: https://example/images/image1.jpg -> файл на диске: image1.jpg

- Программа должна использовать многопоточный, многопроцессорный и асинхронный подходы.
- Программа должна иметь возможность задавать список URL-адресов через аргументы командной строки.
- Программа должна выводить в консоль информацию о времени скачивания каждого изображения и общем времени выполнения программы.

___


### Home Work 5 - [more details](https://github.com/kremlik144/Flask/tree/main/HW_5)

Необходимо создать API для управления списком пользователей. API должен содержать следующие конечные точки:
- GET /users — возвращает список всех пользователей.
- GET /users/{id} — возвращает пользователя с указанным идентификатором.
- POST /users — добавляет нового пользователя.
- PUT /users/{id} — обновляет пользователя с указанным идентификатором.
- DELETE /users/{id} — удаляет пользователя с указанным идентификатором.

___


### Home Work 6 - [more details](https://github.com/kremlik144/Flask/tree/main/HW_6)

Необходимо создать базу данных для интернет-магазина. База данных должна состоять из трёх таблиц: товары, заказы и пользователи.
- Таблица «Товары» должна содержать информацию о доступных товарах, их описаниях и ценах.
- Таблица «Заказы» должна содержать информацию о заказах, сделанных пользователями.
- Таблица «Пользователи» должна содержать информацию о зарегистрированных пользователях магазина.
    + Таблица пользователей должна содержать следующие поля: id (PRIMARY KEY), имя, фамилия, адрес электронной почты и пароль.
    + Таблица заказов должна содержать следующие поля: id (PRIMARY KEY), id пользователя (FOREIGN KEY), id товара (FOREIGN KEY), дата заказа и статус заказа.
    + Таблица товаров должна содержать следующие поля: id (PRIMARY KEY), название, описание и цена.

Создайте модели pydantic для получения новых данных и возврата существующих в БД для каждой из трёх таблиц.
Реализуйте CRUD операции для каждой из таблиц через создание маршрутов, REST API.