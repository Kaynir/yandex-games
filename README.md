# Описание
Пакет содержит инструменты для успешной публикации Unity Yandex Games.
Включает плагин взаимодействия с Yandex SDK и Unity WebGL шаблон, отвечающий требованиям площадки.
# Инструкция
1. Импортируйте пакет в проект Unity через окно Package Manager.
2. Установите WebGL шаблон из раздела Samples, следуя [инструкции](https://github.com/Kaynir/unity-webgl-templates).
3. Создайте игровой объект Yandex SDK через меню редактора *Kaynir/Yandex Games/*, либо вручную.
4. **ВАЖНО:** Сообщение браузера с Unity WebGL осуществляется методом *SendMessage*. При ручном создании объекта следует убедиться, что имя соответствует константе *YandexSDK*, заданной в коде плагина и шаблона. Для правильной работы любые сервисы и модули плагина должны располагаться на данном объекте. Сам объект желательно расположить на сцене, где происходит основное внедрение зависимостей проекта.
5. Для получения данных о статусе авторизации, языке и устройстве игрока следует обращаться к свойствам YandexSDK.
6. Для работы с облачным сервисом Яндекса обращайтесь к компоненту, реализующему интерфейс ICloudService.
7. Для работы с рекламным сервисом Яндекса обращайтесь к компоненту, реализующему интерфейс IAdvService.
8. Модуль Audio Mute предназначен для отключения звука во время показы рекламы и требует настройки пары Audio Mixer Snapshot.
