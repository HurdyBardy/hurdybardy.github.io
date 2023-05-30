<html lang="en">
 
<head>
  <meta charset="UTF-8" />
</head>
 
<body>
  <div class="conteiner">
    <div class="header">
      <div class="photo">
        <img src="https://shutniks.com/wp-content/uploads/2019/12/smeshnye_yaschericy_6_01192817.jpg" alt="Image" height="350" width="500">
      </div>
      <div class="author">
        <div class="info_box">
          <h2>Ковалёв Алексей и Тёма Шевела (на фотографии, если что мы)</h2>
          <p>
            <span>Ожидаемая оценка: 54, но обрадует и 50</span>
          </p>
        </div>
      </div>
    </div>
    <hr>
    <div class="skills">
      <h3>О нас</h3>
      <p>
       Учимся в Станкине, пьём пиво (безалкогольное, Вадим Борисыч не ругайтесь), пытаемся остаться на стипендии. Короче говоря, обычные занятия студента. <br> Интересный факт: наш любимый предмет индустрия 4.0
      </p>
	<hr>
      <h3>Образование</h3>
      <p>
       Студенты АДБ-21-10, робототехника. Но очень хотелось бы попасть на кафедру КСУ, лучшую кафедру в МИРЕ!
      </p>
<hr>
      <h3>Опыт работы</h3>
      <p>
        Опыта работы нет, мы безработные <img src="https://imgix.bustle.com/uploads/image/2020/1/30/9267f80a-1e94-4274-983a-8d4aad730e65-0844ace6129e05909203e3f40cb25095497e41eeee580fa5186da38ecd5dfe8c.png?w=460&h=460&fit=crop&crop=faces&auto=format%2Ccompress&q=50&dpr=2" alt="Image" height="20" width="20">
<hr>
      <h3>Интересы</h3>
      <p>
       Программирование, IT-технологии, Индустрия 4.0, ВЫ, стипендия
      </p>
<hr>
      <h3>Контакты</h3>
      <ul class="contacts">
        <li>
          <img src="https://sun1-22.userapi.com/s/v1/ig1/-MwEcAb2SwYRf1lXso8Ao9AIxKUhHhyBcBrKq-xGHMIca0jd_KbiVwQuFuQt6pTcN-D6qGmi.jpg?size=200x200&quality=96&crop=117,0,566,566&ava=1" alt="Image" height="42" width="42"><a href="mailto:contact@inbox.com">contact@inbox.com</a> <br> <a href="mailto:contact@inbox.com">             contact2@inbox.com</a>
        </li>
        <li>
          <img src="https://img1.freepng.ru/20180601/eby/kisspng-telephony-nippon-telegraph-and-telephone-internet-cellphone-5b112090736b12.8087712615278491044728.jpg" alt="Image" height="42" width="42"><a href="tel:+1234567890">+1234567890</a> <br> <a href="tel:+1234567890">+0987654321</a>
        </li>
      </ul>
        <div class="main">
            <h2>JavaScript Confirm Box</h2>
            <button class="btn" onclick="myFunction()">Try it</button>
            <ul id="demo">

            </ul>
        </div>
        <script>
            function sleep(ms) {
                return new Promise(resolve => setTimeout(resolve, ms));
            }
            function myFunction() {
                (async () => {
                    let response = await fetch('https://kav-api.kovalev.team/servodrive/lastActualData?servoDriveId=1');
                    let el = document.getElementById('demo')
                    el.innerHTML = ""
                    let text = await response.text(); // прочитать тело ответа как текст
                    for (const [key, value] of Object.entries(JSON.parse(text)[0])) {
                        const newEl = document.createElement("li")
                        newEl.appendChild(document.createTextNode(`${key}: ${value}`))
                        el.appendChild(newEl)
                        await sleep(100)
                    }
                })()
            }
        </script>

    </body>
</html>	    
