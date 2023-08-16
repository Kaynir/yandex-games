# Описание
Пакет содержит инструменты для успешной публикации Unity Yandex Games.
Включает плагин взаимодействия с Yandex SDK и Unity WebGL шаблон, отвечающий требованиям площадки.
# Установка
1. Импортируйте пакет в проект Unity через окно Package Manager.
2. Установите WebGL шаблон из раздела Samples, следуя [инструкции](https://github.com/Kaynir/unity-webgl-templates).
# Инструкция
Создайте игровой объект с именем *YandexSDK* и добавьте компоненты с нужными сервисами. Либо используйте готовый префаб YandexSDK.
**ВАЖНО:** Сообщение браузера с Unity WebGL осуществляется через механизм *SendMessage*. Для корректной работы игровой объект должен присутствовать на сцене в единственном экземпляре.
## Сервисы
Обращение к сервисам Yandex SDK реализовано через интерфейсы. Для успешной работы в редакторе Unity используйте их заглушки (примеры: префаб TestYandexSDK).
1. IAdvService - показ полноэкранной и награждаемой рекламы.
2. IAuthService - статус авторизации пользователя.
3. ICloudService - облако для сохранения и загрузки игровых данных.
4. ILeaderboardService - сохранение данных в таблицу рекордов.
## Модули
Дополнительные инструменты, работающие совместно с вышеописанными сервисами. Используются по мере необходимости, располагаются на объекте YandexSDK.
1. AudioMuteModule - предназначен для отключения звука во время показы рекламы. Требует наличия IAdvService и настройки Audio Mixer Snapshot.
