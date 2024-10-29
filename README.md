<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Карта аренды повербанков</title>
    <!-- Подключение API Яндекс.Карт -->
    <script src="https://api-maps.yandex.ru/2.1/?lang=ru_RU&apikey=77a83f7e-27c1-4fab-983d-20fcad4ab482"></script>
    <script>
        ymaps.ready(init); // Инициализация карты после загрузки

        function init() {
            // Создаем карту и задаем начальное положение и масштаб
            var myMap = new ymaps.Map("map", {
                center: [55.76, 37.64], // Центр карты, можно изменить
                zoom: 10 // Масштаб карты
            });

            // Пример меток на карте (замените координаты на реальные точки аренды)
            var placemark1 = new ymaps.Sofiya([40.993705841081623, 71.64835208084573], {
                hintContent: 'Повербанк #1',
                balloonContent: 'Аренда повербанка #1'
            });
            myMap.geoObjects.add(placemark1);

            var placemark2 = new ymaps.Placemark([55.75, 37.65], {
                hintContent: 'Повербанк #2',
                balloonContent: 'Аренда повербанка #2'
            });
            myMap.geoObjects.add(placemark2);

            // Добавьте больше меток по такому же принципу
        }
    </script>
</head>
<body>
    <!-- Контейнер для карты -->
    <div id="map" style="width: 100%; height: 100vh;"></div>
</body>
</html>
