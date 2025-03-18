# Mission 2
## Part 0

[Сылка](https://cloud.mail.ru/public/Rzhx/gfg52eW78) на скринкаст 

## Part1

**Вопрос 1. Зачем нужен ssh? Ответ на пару предложений.**

Это протокол, через который можно взаимодействовать с системами, в основном часто используется разработчиками и админами для администрирования удаленных систем

**Вопрос 2. Предположим, у вас есть прямой доступ к серверу(терминалу) под управлением ubuntu. У вас есть коллега Вася, который хочет получить доступ к этому серверу. Он генерирует пару ssh ключей с помощью команды ssh-keygen и дает вам свой публичный ключ. В какой файл на сервере нужно записать ключ, чтобы Вася смог подключиться к терминалу сервера?**

Обычно добавления его ключа в папку .ssh достаточно, в некоторых случаях необходимо ещё прописать allias или что-то похожее, в зависимости от систем, где-то нужно добавить ключ в папку authorized key.

**Вопрос 3. Тут вопрос про АПИ. Разберитесь, что такое long polling и webhooks, опишите сами в нескольких предложениях, как они работают.**
На мой взгляд наибольшая разница в том что первое инициируется клиентов, а второе инициируется Телеграммом. Однако есть и другие различия, в случае с long polling вы подключившись можете держать долгое соединение таким образом создавая нагрузки на сервера, в то время как в случае с webbhook-амии, Телеграмм сам решает когда он перешлет вам сообщение. В этом случае если сервера загружены, доставка может затянуться. Скорее всего, не уверен, но в первом случае, доставка сообщений происходит быстрее чем в случае с webhook-ами

**Вопрос 4. Найдите информацию, что такое issues на гитхабе и для чего нужны. Также вставьте ссылки на пару примеров issues в популярных open source проектах.**
Это способ по сути учёта недочётов, багов и вещей для улучшения, который может выходить далеко за пределы GitHub-а. В своём [проекте](https://github.com/ipsissimus/spb-rpa-robots-source) на ГитХабе создал специально для этого вопроса [тикет](https://github.com/ipsissimus/spb-rpa-robots-source/issues/1)

**Вопрос 5. Ваш проект используется пустую папку images, но гит не поддерживает отслеживание пустых директорий. Что делать?**

Создания README.md файла или .gitkeep должно хватить для того чтобы объяснить цель папки или проигнорировать содержимое
