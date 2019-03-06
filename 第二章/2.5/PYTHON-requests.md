<!--
author: maomao
date: 2018-01-28
title: python-requests模块
category: 语言学习
status: publish
summary: requests是一个很实用的Python HTTP客户端库，编写爬虫和测试服务器响应数据时经常会用到。可以说，Requests 完全满足如今网络的需求
-->

##一、基本请求

requests库提供了http所有的请求方法。比如get、post、delete、options、head。

使用方法如下：

>  r = requests.post("http://39.98.88.18/challenges")

>r = requests.put("http://39.98.88.18/challenges")

>r = requests.delete("http://39.98.88.18/challenges")

>r = requests.head("http://39.98.88.18/challenges")

>r = requests.options("http://39.98.88.18/challenges")

##二、添加参数

讲需要添加的参数写成字典，然后以parms参数传入。代码如下

```
import requests
 
payload = {'key1': 'value1', 'key2': 'value2'}
r = requests.get("http://httpbin.org/get", params=payload)
print r.url
```
##三、添加headers头

头部信息使用headers添加,具体方法同上。代码如下:
```
import requests 

payload = {'key1':  'valu1','key2':'value2'}
headers = {'cookie' : '123456'}
r=requests.get("http://39.98.88.18/changles",params=pyload,headers=headers)

```

##四、会话对象

在以上的请求中，每次请求其实都相当于发起了一个新的请求。也就是相当于我们每个请求都用了不同的浏览器单独打开的效果。也就是它并不是指的一个会话，即使请求的是同一个网址。有些情况下我们需要维持一个长久的会话，此时我们采用

>s=requests.Session()

代码如下：

```
import requests

s = requests.Session()
s.get('http://httpbin.org/cookies/set/sessioncookie/123456789')
r = s.get("http://httpbin.org/cookies")
print(r.text)

```

##五、超时配置

可以通过timeout来限制服务器的最大访问时间

>requests.get('http://github.com', timeout=0.001)

##六、Cookie设置

如果一个相应中包含cookie使用方法入戏

```
import requests
 
url = 'http://example.com'
r = requests.get(url)
print r.cookies
print r.cookies['example_cookie_name']
```
我们还可以使用cookie参数来获取，代码如下：

```
import requests

url = 'http://httpbin.org/cookies'
cookies = dict(cookies_are='working')
r = requests.get(url, cookies=cookies)
print r.text

get(url, cookies=cookies)
print r.text

```
##七、从头部信息中读取信息

代码如下：
``` 
    a = requests.session()
    b = a.get("http://47e65befd07e4e488e247bb0878a5fef981232f37d4d4d06.game.ichunqiu.com/")
    key1 = b.headers["flag"]
    print key1
```

结果如下：

> ZmxhZ19pc19oZXJlOiBPVEEwTWpJMw==


##八、资源推荐

>https://cuiqingcai.com/2556.html

>http://docs.python-requests.org/zh_CN/latest/user/quickstart.html
