# Weibo-data
## 环境安装
### 安装python
[下载页面](https://www.python.org/downloads/)
### 安装pip
python3.4+ 以上版本都自带pip工具
### 下载Chrome Driver
如果没有Google Chrome就装一个，装完以后再下载对应版本的[Chrome Driver](https://npm.taobao.org/mirrors/chromedriver/)并将Chrome Driver放到Python安装目录下  
![](https://github.com/SylvesterLi/CCYLDataTools/blob/master/NoteImage/1.png)
### 安装Selenium
输入 `pip install selenium` 通过pip安装Selenium(抓阅读量用)  
### 安装lxml
输入 `pip install lxml` (抓内容、转评赞用)  
(如果还缺啥那就`pip install` 安装就完事儿了)
### 接着开始跑用例
在PowerShell或者其他Terminal中输入`py 程序名儿.py` 就可以运行程序了
* 用例weiboSpider.py（可扒取发布时间、机型、地点、博文、转评赞数量）
* 用例 TestUnit01.py 是我自己写来扒阅读量的，最后会生成一个.xls文件
### TestUnit01_py
这个用来抓阅读量。  
运行之后，扫描二维码。然后全自动抓下来，生成Excel表格。  
要抓哪一页就改`pageIndex`然后看到Terminal有个`<<<<< done >>>>` 就去文件夹下找到名为**微博数据-2019xxxx**的Excel文件。  
### weiboSpider_py
这个用来抓大部分的内容，最后会生成一个csv，也可以用Excel打开，然后手动合并一下数据。  
你需要修改weiboSpider.py中几项参数。  
1.cookie
2.user_id
3.filter
先登录[https://passport.weibo.cn/signin/login](https://passport.weibo.cn/signin/login),然后在地址栏输入[https://weibo.cn](https://weibo.cn)。  
![](https://camo.githubusercontent.com/b8b6b65d36b22bea1a6b081104d8b9726a258921/68747470733a2f2f706963747572652e636f676e697a652e6d652f636f676e697a652f6769746875622f776569626f7370696465722f636f6f6b6965322e706e67)
F12点击"Headers"，其中"Request Headers"下，"Cookie"后的值即为我们要找的cookie值取出cookie。  
![](https://camo.githubusercontent.com/86c82d03633c1884f0f3b954f94b5b13b35e676e/68747470733a2f2f706963747572652e636f676e697a652e6d652f636f676e697a652f6769746875622f776569626f7370696465722f636f6f6b6965332e706e67)
具体操作见[原作者GitHub](https://github.com/dataabc/weibospider)
