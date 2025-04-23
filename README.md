# Практична-лабораторна робота №4
### Реалізація нової сутності, створення CRUD-операцій та відповідного RESTful API.

### Виконаємо міграцію
Для цього напишемо команду: ```npm run migration:generate test```
![Image](https://github.com/user-attachments/assets/d05c9b58-8f9b-43b3-8a01-b57e67338cb7)

В результаті у каталозі ```migrations``` з'язвляється файл тестовий

![Image](https://github.com/user-attachments/assets/691c13a4-a49b-4703-a299-581bd61b56fe)

### Так змінемо зміст файлу ```User.ts``` і заново запустимо міграцію.
В результаті отримаємо файл з міграцією 

![Image](https://github.com/user-attachments/assets/6b605475-78f1-4602-b250-63a430aa5588)


### Зміст файлу міграції

![Image](https://github.com/user-attachments/assets/788623d0-41cd-4dee-a32a-c72c39f57127)


Тепер видалемо стару мігрцію, аби не було помилки і тепер запустимо нашу міграцію.
### Напишемо команду ```npm run migration:run```

![Image](https://github.com/user-attachments/assets/9dbca9d8-9db1-422c-9686-b1b7fd4d027f)


### Тепер у вкладці БД оновимо її і з'явиться у таблицях user колонка test

![Image](https://github.com/user-attachments/assets/dedbe61a-8957-42dd-ba90-5afdd17836e0)


### Створимо у каталозі ```controllers``` каталог ```posts```, а у ньому додамо файл ```list.ts```

![Image](https://github.com/user-attachments/assets/4f501df1-4e4b-43af-9de1-7bbd64bb4b54)


### Замінимо зміст файлу. Замінемо ```User``` на ```Post```, а ```users``` на ```posts```. Зміст файлу

![Image](https://github.com/user-attachments/assets/ddeb7648-12d3-46cd-8c18-55b130299f9c)


Так у каталозі ```src/orm/``` створемо каталог posts а у ньому створемо файл ```Post.ts```

![Image](https://github.com/user-attachments/assets/eedc813a-303c-4e67-8360-416a9b63eb7c)


ось зміст файлу.

### Створемо  міграцію. Для цього введемо команду ```npm run migration:generate post```

![Image](https://github.com/user-attachments/assets/6b1d364c-11f4-44fd-a307-fb9ba2a54188)


Так тепер запустимо міграцію. Для цього виконаємо команду ```npm run migration:run```

![Image](https://github.com/user-attachments/assets/46e57d51-2ce2-474f-a992-0f1ebbcf2fc4)


### Тепер перевіремо чисто успішно виконалась міграція. Для цього в WebStorm ми натиснемо
Refresh у БД, і перевіремо чи дійсно успішно відбулась міграція.

![Image](https://github.com/user-attachments/assets/dd8851f0-92a4-4dfd-9fe0-8fa06d470782)


### Так тепер створемо наш ```Post```, для цього у каталозі ```/src/controllers/post``` створемо файл ```create.ts```

![Image](https://github.com/user-attachments/assets/3152e492-492c-4111-a709-d9bc4b884f5a)


![Image](https://github.com/user-attachments/assets/1f42180c-6a56-4ef1-82a5-60038e4b0ee1)


У папці routes створемо маршрут ```post.ts```

![Image](https://github.com/user-attachments/assets/dbd0f1c6-fba9-4557-a8ea-8afbd0b06740)



Так повернемось у наш каталог ```/src/controllers/post``` і створемо наступні файли:
```update.ts```, ```destroy.ts```, ```show.ts```, ```index.ts```, ```index.test.ts```

![Image](https://github.com/user-attachments/assets/762d7192-192d-4db9-a876-b6507823e6bd)


### Тепер заповнемо його даними:
### DELETE

![Image](https://github.com/user-attachments/assets/3b148280-2c5d-4794-b8db-b427b84ac0d1)

### SHOW

![Image](https://github.com/user-attachments/assets/8c11d1a1-98ce-47e9-9e9b-3becd967f350)


### UPDATE

![Image](https://github.com/user-attachments/assets/a1500dbc-41dd-4131-acf0-10b2d3226f38)


### INDEX

![Image](https://github.com/user-attachments/assets/65f563a2-38c7-438a-982e-19d3d4221e14)



### INDEX.TEST

![Image](https://github.com/user-attachments/assets/2f681a76-dd55-4524-94dd-a2296c8f201d)

![Image](https://github.com/user-attachments/assets/bbc17785-d3ea-4845-91a9-94b2c779baa1)



### Тепер перейдемо у файл ```src/router/v1``` і створюємо файл ```post.ts```. Тепер заповнемо його:

![Image](https://github.com/user-attachments/assets/5464c96c-aa44-4c64-b4c8-6e7b9a3e1466)



### Тепер у файлі ```index.ts``` додамо маршрут на наш пост

![Image](https://github.com/user-attachments/assets/16ca7547-c472-4855-941b-b4b7390cc22d)


### Зберігаємо і запускаємо наш сервер.

![Image](https://github.com/user-attachments/assets/9cd20135-9cbd-4087-a008-d80611d8303f)


### Так тепер перейдемо до Postman. Cтворемо нову колекцію.

![Image](https://github.com/user-attachments/assets/2dc901cb-00b3-4e2d-a63a-da34b6a543df)


### Тепер додамо наші ```POST```, ```GET```, ```PUT```, ```DELETE``` запити.

![Image](https://github.com/user-attachments/assets/feebe711-08c6-4aed-9453-aa4c696378f7)


# Тепер протестуємо.
- # Для POST

![Image](https://github.com/user-attachments/assets/7676c96c-08be-4a59-a632-3f6ad4a94203)

![Image](https://github.com/user-attachments/assets/249cfe4c-3ccd-4cf7-bb0d-c1be87667306)



- # Для GET усіх постів

![Image](https://github.com/user-attachments/assets/f5e3cbf9-d19f-4adf-b9d6-b756e13c266c)

![Image](https://github.com/user-attachments/assets/4ae5ec9b-9f41-4205-b8c6-5c124c51933d)



- # Для GET для конкретного поста

![Image](https://github.com/user-attachments/assets/d355778b-1029-4c84-8607-463be2d4a7a0)

![Image](https://github.com/user-attachments/assets/d0b93b03-ca02-4d88-b8b3-677370f51c82)


- # Для PUT

![Image](https://github.com/user-attachments/assets/d600b618-7cab-4f97-829a-412f301a35ca)

![Image](https://github.com/user-attachments/assets/bbb8b7f9-45d3-4a74-8e3d-a1ec5eacf50e)


- # Для DELETE

![Image](https://github.com/user-attachments/assets/d69a1169-fe76-4637-8ffc-f26f9712cc19)

![Image](https://github.com/user-attachments/assets/553e1dd7-b5af-4e9d-9ac7-02885e198c2d)


### Перевіремо чи дійсно видалилось

![Image](https://github.com/user-attachments/assets/64bc4fb0-7579-404f-bd5c-23bca4939cad)

### Перевірка оновлення
# ДО
![Image](https://github.com/user-attachments/assets/9ab4b477-e092-481b-a8f8-2aedbc7a910a)



# ПІСЛЯ

![after](https://github.com/user-attachments/assets/ba11140c-71e8-40c6-be97-68ec70c1931e)



Як бачимо дійсно все видаляє і оновлює.


# Висновок
У ході виконання практично-лабораторної роботи було реалізовано повноцінну CRUD-функціональність для нової сутності ```Post```. 
Було створено відповідну ORM-модель, проведено міграції для створення таблиці в базі даних, а також реалізовано маршрути, контролери та методи для обробки HTTP-запитів.
