Flask-Moive
-------
项目简介：
-------
Flask-Moive是基于python3.6+Flask1.1.1+requests+Beautifulsoup4开发的抓取电影天堂影片展示项目。

使用方法：
-------
1.安装Python3.6环境
-------
2.下载代码到本地并解压
-------
3.cmd到根目录下安装相关依赖包
-------
```
pip install -r requirements.txt
```
4.安装mysql数据库，进入config/local_setting.py配置数据库连接
-------

```
SQLALCHEMY_DATABASE_URI = "mysql://root:111111@127.0.0.1/movie_cat"
SQLALCHEMY_TRACK_MODIFICATIONS= True
SECRET_KEY = "imooc123456"
```
5.cmd到根目录下，生成数据库表
-------
```
python manager.py create_all
```

6.抓取电影天堂影片
-------
```
python manager.py runjob -m movie -a list
```
7.运行启动flask服务
-------
```
python manage.py runserver 
```
8.访问127.0.0.1:5001进入影片主页
-------
首页：

![](https://github.com/PyGuojun/Flask-Moive/blob/master/cover/index.png)

影片详情：

![](https://github.com/PyGuojun/Flask-Moive/blob/master/cover/info.png)

