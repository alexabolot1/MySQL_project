# MySQL_project
Проект базы данных STEAM.
Для своего проекта по созданию модели базы данных я выбрал  онлайн-сервис цифрового распространения компьютерных игр и программ, разработанный и поддерживаемый компанией Valve – STEAM.
Мой проект базы данных включает в себя такие таблицы как:
1)	users – данная таблица содержит в себе базовую информацию об аккаунте, которая необходима для регистрации нового пользователя (email, страна)
2)	profiles – таблица содержит в себе расширенную информацию о пользователе, которую он указывает после регистрации по своему желанию (никнейм, реальное имя, город проживания, краткую информацию о себе)
3)	countries и cities – содержат в себе перечень стран и городов. Также данные таблицы связаны между собой по внешнему ключу
4)	friendship – таблица дружественных отношений, поскольку приложения позволяет добавлять и удалять друзей. Данная таблица также имеет статус дружбы, дату подтверждения дружбы, создания и обновления статуса.
5)	communities – таблица, содержащая в себе группы (название, дата создания и обновления). А таблица communities_users является таблицей отношения между пользователями и группами. Связь происходит по внешнему ключу.
6)	games – таблица, содержащая в себе данные об играх, которые обслуживаются данной платформой. (название игры, цена, размер, занимаемый на жестком диске, описание, дата создания и обновления). Также имеется столбец с жанром игры, который связан по внешнему ключу с другой таблицей – game_genre, которая содержит в себе название игровых жанров.
7)	messages – таблица, в которой находятся данные о всех имеющихся сообщениях. (от какого юзера и к какому создано сообщение, текст сообщения, признак важности, признак доставки (если доставлено, то дата доставки), время создания и обновления сообщений.
8)	reviews – таблица, которая содержит в себе отзывы к играм. (От какого пользователя, к какой игре, заголовок отзыва, непосредственно сам отзыв и флаг, который показывает положительный отзыв или отрицательный). Таблица связана с таблицами users и games по внешнему ключу.

Данный проект базы данных заполнен тестовыми данными.
К данному проекту были созданы все необходимые внешние ключи, индексы, а также сформирована диаграмма отношений.
Для удобства аналитики, было также создано несколько представлений, которые создают условия для комфортного и быстрого анализа.
Я создал скрипты характерных выборок, которые помогут проанализировать базу данных, например, показать количество игр, отзывов и групп каждого пользователя, вывести количество негативных и положительных отзывов к игре и так далее.
Также я сформировал некоторые триггеры, которые позволят автоматизировать какое-либо действие, при добавлении, изменении или удалении данных из таблицы.
