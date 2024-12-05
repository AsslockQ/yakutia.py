# yakutia.py
from flask import Flask, render_template

app = Flask(__name__)

@app.route("/")
def home():
    return """
    <!DOCTYPE html>
    <html lang="ru">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Туризм в Якутии</title>
        <style>
            body {
                font-family: Arial, sans-serif;
                line-height: 1.6;
                margin: 0;
                padding: 0;
                background: #f9f9f9;
            }
            header {
                background: #2c3e50;
                color: #fff;
                padding: 20px 0;
                text-align: center;
            }
            main {
                padding: 20px;
            }
            section {
                margin-bottom: 20px;
            }
            footer {
                text-align: center;
                padding: 10px 0;
                background: #2c3e50;
                color: #fff;
            }
            a {
                color: #3498db;
                text-decoration: none;
            }
            a:hover {
                text-decoration: underline;
            }
            .extra-link {
                font-size: 1.1em;
                color: #2ecc71;
                margin-top: 20px;
                display: block;
                text-align: center;
            }
        </style>
    </head>
    <body>
        <header>
            <h1>Добро пожаловать в Якутию!</h1>
            <p>Откройте для себя край вечной мерзлоты, захватывающих пейзажей и древней культуры</p>
        </header>
        <main>
            <section>
                <h2>О Якутии</h2>
                <p>Якутия — крупнейший регион России и один из самых загадочных уголков планеты. Здесь суровая природа соседствует с богатой культурой и традициями.</p>
            </section>
            <section>
                <h2>Что посмотреть?</h2>
                <ul>
                    <li><strong>Ленские столбы:</strong> уникальный природный парк. <a href="https://ru.wikipedia.org/wiki/%D0%9B%D0%B5%D0%BD%D1%81%D0%BA%D0%B8%D0%B5_%D1%81%D1%82%D0%BE%D0%BB%D0%B1%D1%8B" target="_blank">Подробнее</a></li>
                    <li><strong>Оймякон:</strong> полюс холода и самое холодное место на Земле. <a href="https://ru.wikipedia.org/wiki/%D0%9E%D0%B9%D0%BC%D1%8F%D0%BA%D0%BE%D0%BD" target="_blank">Подробнее</a></li>
                    <li><strong>Мамонтова гора:</strong> место находок древних животных. <a href="https://ru.wikipedia.org/wiki/%D0%9C%D0%B0%D0%BC%D0%BE%D0%BD%D1%82%D0%BE%D0%B2%D0%B0_%D0%B3%D0%BE%D1%80%D0%B0" target="_blank">Подробнее</a></li>
                </ul>
            </section>
            <section>
                <h2>Как добраться?</h2>
                <p>Регулярные рейсы в Якутск доступны из Москвы и других крупных городов России. После этого, чтобы добраться до интересных мест, можно воспользоваться следующими маршрутами:</p>
                <ul>
                    <li><strong>Ленские столбы:</strong> Можно добраться на автомобиле или катере. Есть маршрутные рейсы из Якутска. <a href="https://ru.wikipedia.org/wiki/%D0%9B%D0%B5%D0%BD%D1%81%D0%BA%D0%B8%D0%B5_%D1%81%D1%82%D0%BE%D0%BB%D0%B1%D1%8B#%D0%94%D0%BE%D0%B1%D1%80%D0%B0%D0%BF%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D1%8B%D0%B5_%D0%BC%D0%B0%D1%80%D1%88%D1%80%D1%83%D1%82%D1%8B" target="_blank">Подробнее</a></li>
                    <li><strong>Оймякон:</strong> Добраться можно на автомобиле из Якутска, но важно учитывать, что зимой дорога может быть закрыта из-за сильных морозов. <a href="https://ru.wikipedia.org/wiki/%D0%9E%D0%B9%D0%BC%D1%8F%D0%BA%D0%BE%D0%BD#%D0%94%D0%BE%D0%B1%D1%80%D0%B0%D0%BF%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D1%8B%D0%B5_%D0%BC%D0%B0%D1%80%D1%88%D1%80%D1%83%D1%82%D1%8B" target="_blank">Подробнее</a></li>
                    <li><strong>Мамонтова гора:</strong> Мамонтову гору можно посетить, совершив пеший маршрут из ближайших населённых пунктов. <a href="https://ru.wikipedia.org/wiki/%D0%9C%D0%B0%D0%BC%D0%BE%D0%BD%D1%82%D0%BE%D0%B2%D0%B0_%D0%B3%D0%BE%D1%80%D0%B0#%D0%94%D0%BE%D0%B1%D1%80%D0%B0%D0%BF%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D1%8B%D0%B5_%D0%BC%D0%B0%D1%80%D1%88%D1%80%D1%83%D1%82%D1%8B" target="_blank">Подробнее</a></li>
                </ul>
            </section>
            <section>
                <h2>Уникальные явления</h2>
                <p>Полярное сияние зимой и белые ночи летом делают Якутию особенным местом для туристов.</p>
            </section>
            <section>
                <h2>Для более глубокого понимания Якутии</h2>
                <p>Обязательно посетите этот <a href="https://www.kp.ru/russia/yakutiya/dostoprimechatelnosti/" target="_blank" class="extra-link">сайт</a> для еще более детального ознакомления с природными и культурными достопримечательностями Якутии.</p>
            </section>
        </main>
        <footer>
            <p>&copy; 2024 Туризм в Якутии. Все права защищены.</p>
        </footer>
    </body>
    </html>
    """

if __name__ == "__main__":
    app.run(debug=True, host='0.0.0.0')
    
