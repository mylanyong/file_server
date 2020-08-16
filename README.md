﻿# 设计初衷:
上机实验课的时候不想带电脑去机房, 但是在机房又可能需要使用到自己电脑里的文件, 再加上机房电脑没有安装网盘等应用, 每次上机都要下载登录比较麻烦, 所以用Node.js搭建了这个文件服务器。


# 技术栈：
jQuery + Node.js + formidable


# 该文件服务器有以下好处:
1.方便在机房、网吧等临时使用的电脑上快速下载需要的文件, 只要打开浏览器就可以下载事先上传好的文件

2.方便手机和电脑在不安装其他应用的情况下传输文件, 因为手机和电脑都内置了浏览器

3.方便和别人共享文件, 不用担心限速

4.能在大部分情况下取代U盘, 带着U盘怕掉, 用的时候还要占用一个USB接口



# 该文件服务器的主要功能:
## 1. 上传文件：  
多文件上传  
文件上传大小限制  
控制是否覆盖同名文件  
上传等待提示  


## 2. 显示文件：
显示文件总数

显示文件名、文件大小、修改时间

可以按照文件名、文件大小、修改时间对文件排序显示



## 3. 下载文件
## 4. 删除文件
## 5. 身份验证
## 6. 权限控制：
身份验证失败或没有验证只能得到public目录下的文件, 即使有下载地址也无法下载文件

## 7. 视频、音乐在线播放
## 8. 图片在线查看、文本在线编辑
## 9. 登录信息（包含IP地址）保存到日志文件


# 文件服务器第二版新增功能:
文件夹上传/文件夹下载/查看文件夹内容
上传文件时以百分比显示文件的上传进度
移动文件/新建文件/新建文件夹
更友好的弹窗提示(layer.js)
保存和查看登录记录
不在cookie中记录账号密码, 而是使用随机生成的字符串当做每次请求的验证信息
可以开放一个公共文件夹用来分享文件给任意人查看下载
显示根目录到当前文件夹的路径信息, 点击路径中的文件夹可以跳转到该文件夹


# 效果图 
## 身份验证页面：
![](https://user-gold-cdn.xitu.io/2020/7/6/173240a9e9ddbb94?w=339&h=223&f=png&s=6792)

## 首页：
![](https://user-gold-cdn.xitu.io/2020/7/6/17323ff3a7ae3a08?w=740&h=496&f=png&s=46795)




## 按文件大小从大到小排序显示：

![](https://user-gold-cdn.xitu.io/2020/7/6/1732400ebb964cad?w=758&h=337&f=png&s=34756)

## 点击“v.mp4”观看视频：

![](https://user-gold-cdn.xitu.io/2020/7/6/17324023d58103ee?w=1287&h=638&f=png&s=325300)


## 点击“游鸿明 - 21个人.mp3”播放音乐：

![](https://user-gold-cdn.xitu.io/2020/7/6/173240532753a3e2?w=611&h=165&f=png&s=21973)


## 点击“文本文件.txt”在线编辑文件：


![](https://user-gold-cdn.xitu.io/2020/7/6/1732408158c9a166?w=1154&h=503&f=png&s=42923)



# 项目目录结构：

```
文件服务器
|-- config
    |-- config.js
|-- control
    |-- control.js
|-- log
    |-- login_info.log
|-- node_modules
|-- public
    |-- css
        |-- index.css
    |-- js
        |-- jq.js
    |-- editText.html
    |-- playMusic.html
    |-- playVideo.html
    |-- verify.html
|-- uploads
|-- app.js
|-- index.html
|-- package.json
```
