Практична робота №4
Реалізація нової сутності, 
створення CRUD-операцій та відповідного RESTful API.

Виконаємо міграцію. Для цього напишемо команду: npm run migration:generate test
migration run.png
В результаті у каталозі migrations з'язвляється файл тестовий
test-ts.png
Так змінемо зміст файлу User.ts і заново запустимо міграцію.
В результаті отримаємо файл з міграцією 
new_test_ts.png
Зміст файлу міграції
new_test_content.png
Тепер видалемо стару мігрцію, аби не було помилки і тепер запустимо нашу міграцію.
Напишемо команду npm run migration:run
  migration_run.png
Тепер у вкладці БД оновимо її і з'явиться у таблицях user колонка test
DB.png
Створимо у каталозі controllers каталог posts, а у ньому додамо файл list.ts
posts_list.png
Замінимо зміст файлу. Замінемо User на Post, а users на posts. Зміст файлу
list_content.png
Так у каталозі src/orm/ створемо каталог posts а у ньому створемо файл Post.ts
Post_ts.png
ось зміст файлу.
Створемо  міграцію. Для цього введемо команду npm run migration:generate post
migratio_generate_post.png
Так тепер запустимо міграцію. Для цього виконаємо команду npm run migration:run
migration_run_post.png
Тепер перевіремо чисто успішно виконалась міграція. Для цього в WebStorm ми натиснемо
Refresh у БД, і перевіремо чи дійсно успішно відбулась міграція.
DB_post_check.png
Так тепер створемо наш Post, для цього у каталозі /src/controllers/post створемо файл
create.ts
create_content.png
create_content_new.png
У папці routes створемо маршрут post.ts
router_post.png
Так повернемось у наш каталог /src/controllers/post і створемо наступні файли:
update.ts, destroy.ts, show.ts, index.ts, index.test.ts
catalog_posts_conetent.png
Тепер заповнемо його даними:
destroy_content.png
DELETE
---list_content_new.png
---LIST
show_content.png
SHOW
update_content.png
UPDATE
index_content.png
INDEX
index_test_content_1.png
index_test_content_2.png
INDEX.TEST
Тепер перейдемо у файл src/router/v1 і створюємо файл post.ts. Тепер заповнемо його:
router_post_new.png
Тепер у файлі index.ts додамо маршрут на наш пост
v1_index.png
Зберігаємо і запускаємо наш сервер.
DB_connected.png

Так тепер перейдемо до Postman. Cтворемо нову колекцію. 
create_collection.png
Тепер додамо наші POST, GET, PUT, DELETE запити.
request.png
Тепер протестуємо.
Для POST
POST_1.png
POST_2.png
Для GET усіх постів
GET_all_1.png
GET_all_2.png
Для GET для конкретного поста
GET_1.png
GET_2.png
Для PUT
PUT_1.png
PUT_2.png
Для DELETE 
DEL_1.png
DEL_2.png
Перевіремо чи дійсно видалилось
check_del.png
Перевірка оновлення
before.png
ДО
after.png
ПІСЛЯ
Як бачимо дійсно все видаляє і оновлює.
