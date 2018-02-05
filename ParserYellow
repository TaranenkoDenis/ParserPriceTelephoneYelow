import re
import urllib.request
from lxml.html import fromstring  # подключаем библиотеку lxml

# site = urllib.request.urlopen('https://news.yandex.ru/')
# Функция urllib.request.urlopen() создает файлоподобный объект,
# который читается методом read(). Другие методы этого объекта: readline(),
# readlines(), fileno(), close(), работают как и у обычного файла, а также есть метод info(),
# который возвращает соответствующий полученному с сервера Message-объект.
response = urllib.request.urlopen('https://yellow.ua/apple-iphone-x-64gb-silver/').read()

# делаем из нашей строки объект для манипулирования страницей
page = fromstring(response)

# получаем все элементы с переданным xpath
price = page.xpath('/html/body/div[1]/div/div/div[2]/div[2]/div/div[2]/div[2]/form/div[4]/div[1]/div/div/span/span')

# выводим результат
for p in price: print(p.text)
