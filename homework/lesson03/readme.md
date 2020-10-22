**Pаблица с измененной структурой и лайками лежит в папке "04"**

_1 Проанализировать структуру БД vk, которую мы создали на занятии, и внести предложения по усовершенствованию (если такие идеи есть). Напишите пожалуйста, всё-ли понятно по структуре._

Данную БД можно расширять до бексконечности: например реализовать привязку фото к к аватару profile, создав связанное поле avatar_profile со связкой photos.
Заменить таблицу photo_albums, создав таблицы: albums и albums_type, так как тип альбомов в дальнейшем может быть различен. И т.д. это лишь малая часть расширения далее архитектура будет расти в зависимости от бизнес требований.

_2 Добавить необходимую таблицу/таблицы для того, чтобы можно было использовать лайки для медиафайлов, постов и пользователей._

Создаем таблицу likes с полями:
- like_from: айди пользователя
- media_id: id характеризующий саму запись

Это супер по чопорному, вопрос как это реализовано в вк, ведь есть фото у которых по 1кк лайков, и ВК известен каждый юзер который его поставил, по моей логике та могромная таблица будет с кучей записей.

_3 Используя сервис http://filldb.info или другой по вашему желанию, сгенерировать тестовые данные для всех таблиц, учитывая логику связей. Для всех таблиц, где это имеет смысл, создать не менее 100 строк. Создать локально БД vk и загрузить в неё тестовые данные._

Приложил sql с заполнением