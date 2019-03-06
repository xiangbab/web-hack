#玄魂－CTF(HTML基础WP)

##HTML签到提

１．打开题目发现是一个百度的界面

![](photo/1.png)

２．通过链接可以判断这是一个假的

![](photo/2.png)

３．查看源码

４．ctrl+f，然后输入flag进行搜索，成功发现flag.

![](photo/3.png)

#html2

１．右键查看源码

２．发现在源码底部有一个js.flag

![](photo/4.png)

3.点击进去，成功发现flag

![](photo/5.png)

#jsjsjs

##方法一

1.进入以后发现限制输入长度为１位

２．按F12，找到控制长度的maxlength

![](photo/6.png)

3.双击它，然后将其修改为100

![](photo/7.png)

４.然后题目问的是你爱谁，看到上方的xuanhun，输入。验证成功

![](photo/８.png)

##方法二

１．题目为jsjs。故猜测此题与js有关。

２．因js文件也是传输到本地由浏览器执行。故右键，然后查看源码。

３．发现有一个js文件

![](photo/9.png)

４．点击查看，成功发现flag.

![](photo/10.png)


#小结

CTF（web和内网渗透系列教程）的清单请在“https://github.com/xuanhun/HackingResource” 查看，定时更新最新章节链接

答疑、辅导请加入玄魂工作室--安全圈，一起成长探讨更私密内容。微信扫码了解详情：

![](photo/00.jpeg)

及时获取更多消息，请关注微信订阅号

![](photo/0.jpg)


