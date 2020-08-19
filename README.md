# pycharm-learn
python爬虫
import os
import requests
from urllib import request
from bs4 import BeautifulSoup
url="http://www.gaokw.com/fenshu/heilongjiang/192011.html"
headers={"User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:79.0) Gecko/20100101 Firefox/79.0"}
resp=requests.get(url,headers=headers)
text=resp.content
soup=BeautifulSoup(text,'lxml')
lcy=soup.find('div',class_="192011 content")
for tds in lcy:
    tds=lcy.find_all("td")[]
    print(tds)
