# Adult Video Scraper for JAV 日本AV(JAV)刮削整理
原作者暂停更新和修复bug。开此分支用于维护javsdt并且继续开发，接受pull request，欢迎提交新功能和修复bug。

为了维护及开发新功能，欢迎各位加入TG群https://t.me/javsdtool

Todo:
- [ ] 由于缺少相关背景，需要有会使用Emby API的大佬帮助整合进入Emby。(参考Javscraper: https://github.com/JavScraper/Emby.Plugins.JavScraper 和jellyfin-plugin-avdc：https://github.com/xjasonlyu/jellyfin-plugin-avdc）

## 源码使用方法，
1、先安装[Python3](https://www.python.org/downloads/)和[Node.js](https://nodejs.org/zh-cn/download/)最新版本。

2、进入[Release](https://github.com/fanza1/Fake_javsdt/releases)，下载最新版本源码

3、找到根目录下的requirements.txt，然后运行pip install安装执行环境
```
pip install -r .\requirements.txt
pip install -U cfscrape
```
4、然后进入javsdt目录执行CreateIni.py

5、接下来按需求执行如JavbusYouma.py

## 常见问题
* 注意，执行方法可以打开cmd或PowerShell使用命令行如
```
pip install -r .\requirements.txt
pip install -U cfscrape
python CreateIni.py
python JavbusYouma.py
```
对于windows用户也可以直接双击运行，选择python执行

* javlibrary免翻墙刮削出错建议更换网址，图书馆官方网址发布：http://www.javlibrary.com/cn/publictopic.php?id=13483

## Log 记录
- [x] 21.6.7 fix JavBus图片刮削
- [x] 21.2.25 fix JavBus有码无法刮削genre和tag
- [x] 21.3.4 fix JavBus无码无法刮削genre和tag
- [x] 21.4.2 fix javlibrary评分错乱的问题，移除作者瞎搞的评分算法，忠于图书馆的评分。修复由于cf造成的无法获取javlibrary网页的问题，但需要用户安装最新版node.js并且在命令行执行
```
pip install -U cfscrape
```
- [x] 21.4.2 new feature 增加避免小众高分影片霸榜的算法


# 以下为原repo的Readme
## jav-standard-tool 简称javsdt
## 作者为生活所迫，已经跑路...
简介：收集影视元数据，并规范本地文件（夹）的格式，收集演员头像，为emby、kodi、jellyfin、极影派等影片管理软件铺路。  

  
## 1、【一般用户】下载及群链接：  
目前2021年2月7日更新的1.1.5版本  推荐使用win10 64位  
[从蓝奏云下载](https://junerain.lanzous.com/ivp8Plg6wza) 或者 [从github下载](https://github.com/javsdt/javsdt/releases/tag/V1.1.5)
  
[前往下载演员头像](https://github.com/javsdt/javsdt/releases/tag/女优头像)   
  
[企鹅群](https://jq.qq.com/?_wv=1027&k=5CbWOpV)（需要付费1人民币扩群）  
[电报群](https://t.me/joinchat/PaHhgBaleu_qEgFy_NJlIA)（尽量进企鹅群，电报群真的没时间去了）   
  
## 2、[使用说明(还没写完)](https://github.com/javsdt/javsdt/wiki)  
[旧版的使用说明从蓝奏云下载](https://www.lanzous.com/ib0qozg)  

## 3、【其他开发者】运行环境：  
  python3.7.6 发行版是pyinstaller打包的exe  
    pip install requests==2.20.0（安装2.25.1报错ProxyError无法使用http代理）  
    pip install Pillow  
    pip install baidu-aip  
    pip install pysocks  
    pip install [cloudscraper](https://github.com/VeNoMouS/cloudscraper)（目前版本暂时不需要）  
    pip install xlrd==1.2.0（安装2.2.1无法读取xlsx）  
   几个jav的py都是独立执行的，加了很多很多注释，希望能理解其中踩过的坑。  
   
## 4、工作流程：  
    （1）用户选择文件夹，遍历路径下的所有文件。  
    （2）文件是jav，取车牌号，到javXXX网站搜索影片找到对应网页。  
    （3）获取网页源码找出“标题”“导演”“发行日期”等信息和DVD封面url。  
    （4）重命名影片文件。  
    （5）重命名文件夹或建立独立文件夹。  
    （6）保存信息写入nfo。   
    （7）下载封面url作fanart.jpg，裁剪右半边作poster.jpg。   
    （8）移动文件夹，完成归类。  
  
## 5、目标效果：  
效果图不放了
!=[image](https://github.com/javsdt/images/blob/master/jav/javsdt/readme/%E7%9B%AE%E6%A0%87%E6%95%88%E6%9E%9C1.png?raw=false)  
!=[image](https://github.com/javsdt/images/blob/master/jav/javsdt/readme/%E7%9B%AE%E6%A0%87%E6%95%88%E6%9E%9C2.png?raw=false)  
!=[image](https://github.com/javsdt/images/blob/master/jav/javsdt/readme/%E7%9B%AE%E6%A0%87%E6%95%88%E6%9E%9C3.jpg?raw=false)  
  
## 6、ini中的用户设置：  
![image](https://github.com/javsdt/images/blob/master/jav/javsdt/readme/ini%E8%AE%BE%E7%BD%AE.PNG?raw=false)  
  
## 7、其他说明：  
（1）不需要赞助；  
（2）允许对软件进行任何形式的转载；  
（3）代码及软件使用“MIT许可证”，他人可以修改代码、发布分支，允许闭源、商业化，但造成后果与本作者无关。  
