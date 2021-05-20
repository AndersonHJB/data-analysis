> 课程开始前，先简单讲一讲Markdown。
>
> Markdown语法不必一下全都记住，可以边用边查。

## 一、技术组是干什么的

学习倾向实战的技术

学校承办的各类acm比赛时，做技术负责、环境配置

帮助你找到感兴趣的方向，并让你在学习时少走弯路

在技术组内讨论与分享自己所学

另外，算法的学习需要伴随技术学习的始终

## 二、说一说周报的收取

开始时间

格式

上传至Github仓库

请假

## 三、Git入门

https://www.bilibili.com/video/BV1KD4y1S7FL

> 建议使用GitKraken：到官网下载 https://www.gitkraken.com/
>
> 第一次启动会提示登录
>
> 然后填写签名信息（随便填，不一定要真实）
>
> 然后创建代码仓库（Repository）：点左上角的文件夹 ->Init

#### 配置基本用户信息

`git config --global user.name <你的用户名>`

`git config --global user.email <你的邮箱地址>`

#### 创建一个新仓库

`git init`

#### 关联远程仓库

`git remote add <自定义仓库名> <远程仓库地址>`

#### 从远程服务器克隆一个仓库

`git clone <远程仓库的url>`

#### 显示当前工作目录下的提交状态（类似于GitKraken中右边的窗口）

`git status`

#### 将指定文件Stage（标记为将要被提交的文件）

`git add <文件路径>`

#### 将指定文件Unstage（取消标记）

`git reset <文件路径>`

#### 创建一个提交并附上提交信息

`git commit -m "提交信息"`

#### 显示提交历史（类似GitKraken中间的窗口）

`git log`

按q退出

#### 向远程仓库推送（Push）

`git push`

#### 从远程仓库拉取（Pull）

`git pull`

#### 分支（branch）

master是主分支（默认），分支在不合并的情况下是相互独立的

`git branch` 查看所有分支

`git branch <分支名字>` 新建分支

`git checkout <分支名字>` 切换分支

`git branch -m <旧名字> <新名字>` 修改分支名

`git branch -d <分支名字>` 删除分支

#### 签出（check out）

`git checkout <提交的hash>`

> 还有很多其他操作，以后再说

---

下面是上传周报的具体步骤：

1. 先Fork我们的总仓库
2. 将Fork后的仓库（你的） clone到本地
3. 然后在你的目录下新建一个.md文件，写好周报内容，然后push到你的远程仓库
4. 然后pull request

之后学长会对你们的pr进行审核，没问题的话就能在总仓库看到了。

---

如果觉得上面难度太高的话，还可以直接在网页上操作，具体的看录课内容。

周报收集仓库地址：https://github.com/JooKS-me/NEUQ-ACMClub2020-Jishu-weekly

## 四、目前流行的一些开发岗位

前端、后端、安卓、大数据开发、算法、游戏开发、客户端开发。。。

## 五、为什么推荐学习web开发
① 门槛低，上手快，学习相对简单，特别是前端，所见即所得，很容易培养起兴趣，很快就能干活了。

② 掌握web相关知识对于数据分析和挖掘有一定帮助，如果学到一半发现对web不感兴趣也不算白学。

③ 后路多，学了java后端转安卓、大数据都比较方便，因为前期技术栈非常类似。学了前端，对于爬虫的理解会有帮助。而且你们年轻，早点尝试，找到喜欢的方向，针不戳。

## 六、什么是前端？
大前端时代：前端已无所不能。

## 七、什么是后端？
主要语言：Java/Golang/C++/Python/PHP  语言只是一个工具

高层次：Data/Cloud/DevOps

## 八、粗略讲完html+css+js

>  推荐一个Web IDE ：Hbuilder https://www.dcloud.io/hbuilderx.html
>
> 用vscode或WebStorm也行，看个人喜好。

### HTML

`<!DOCTYPE html>` html5标准网页声明，是命令，不是标签

下面是一些非常常见的标签

`<html>` 根标签

`<head>` 头标签，描述了文档的各种属性和信息

`<body>` 定义网页正文，构成显示的主要内容

`<h1> <h2> <h3> <h4> <h5> <h6>` 标题标签，跟word里面的标题差不多，由1到6字体依次减小

`<p>` 段落标签，表示一个段落，段与段间有空行，可通过align属性设置对齐方式

`<br>` 换行标签

`<hr/>` 画一条水平线，有width、size、color等属性

`<div>` 块标签，表面上没什么用，其实大大方便了布局

`<font>` 字体标签，定义标签内的字体，有size、color、face等属性。

`<img />` 图片标签，有src(图片地址)、width、height、align等属性

 `<a>` 链接标签，有href(后跟跳转地址，若是其他网址需带协议)、target(\_blank表示新窗口打开，\_self表示原窗口打开，默认为新窗口打开)等属性

此外，还有可设置加粗、删除线等文字格式化标签（内容很多），列表标签等，感兴趣可深入学习。

**下面是个人认为及其重要的标签**

`<table> <tr> <th> <td>` table是表格的根标签，tr定义行，th定义列名，td定义列内容

---

`<form> <input>` 表单标签，form主要需要设置action、method、enctype属性

> \<form> 的属性
>
> action属性定义了表单上传的地址
>
> method属性定义了上传方法，有get和post两种，get效率高但不安全、请求大小有限，post安全、请求大小无限但效率低。
>
> enctype属性定义了表单的提交类型，默认值是application/x-www-form-urlencoded（普通表单），当需要上传文件时会用multipart/form-data（多部分表单）。（目前了解即可）

> \<input> 的属性
>
> 主要是type属性，定义了~~emmmm控件的类型？~~，看演示吧

form+table经常用到

---

### CSS

CSS全称Cascading Style Sheets层叠样式表。

可以对HTML标签进行修饰，美化html页面

外部CSS文件可以提高代码复用性，让html内容与样式分离，便于后期维护。

下面简单介绍一下

用法一：内嵌进html标签

```html
<div style="color:blue;font-size:50px">H e l l o</div>
```

用法二：在head中加样式表

```html
<head>
	balabala...
	<style type="text/css">
		div{color:red;font-size:50px}
	</style>
	balabala...
</head>
```

用法三：CSS另存一个文件，head中引用

```html
<link rel="stylesheet" type="text/css" href="div.css" />
```

用法四：@import

```html
<style type="text/css">
	@import url("div.css");
</style>
```

---

### JavaScript

一种脚本语言，功能强大。

浏览器内置JavaScript引擎

简单例子：

```html
<body>
	balabala...
	<script type="text/javascript">
		var a = 1, b = 5;
		document.write(a*b);
		alert("你好");
	</script>
	balabala...
</body>
```

前端需要精通，需要很大精力投入。

---

以上就是前端三剑客，学后端了解即可，感兴趣可深入。

## 九、介绍http
> 网页访问过程：
>
> 在浏览器输入URL地址
>
> 浏览器连接到远程服务器上(IP+80端口)
>
> 请求下载一个HTML文件，放到本地临时文件夹
>
> 在浏览器显示出来

基于TCP/IP通信协议来传递数据

浏览器请求，发送请求报文

服务端响应，给浏览器返回响应报文，响应报文中含有html文本

常见状态码：200，404，500。。。

## 十、学习nginx
web服务器，代理静态资源时性能很强

反向代理，动静分离，负载均衡（了解）

看一看配置文件
## 十一、搭建Linux环境，安装nginx，部署第一个静态网页。
> 完成实名认证，试用云服务器（建议是这样）
>
> 套路云：https://free.aliyun.com/?spm=a2c6h.13066369.0.0.894740d1z70tDF
>
> 或良心云：https://cloud.tencent.com/act/free?from=11649
>
> 或者用虚拟机
>
> 或者直接买。。。

我的操作系统：Debian9

阿里云创建完小机之后需要进入控制台重置密码（腾讯云忘了），到安全组开放80和443端口

> 这里推荐使用Xshell进行ssh远程连接，使用WinSCP进行文件传输
>
> 安装包都已上传至群文件

```shell
apt update
apt install nginx
```
默认网页根目录在/var/www/html

## 十二、介绍一下mysql、php

mysql：数据库，增删改查

select * from xxxx



php：世界上最好的语言，但是不推荐想做后端的去学。。。

## 十三、安装mysql和php
```shell
apt install mysql-server mysql-client    #安装mysql(MariaDB)
mysql   #默认无密码，直接进入mysql命令行
UPDATE mysql.user SET authentication_string = PASSWORD('你的密码'), plugin = 'mysql_native_password' WHERE User = 'root' AND Host = 'localhost';
FLUSH PRIVILEGES;
exit    #退出mysql
service mysql restart   #重启mysql

# 因为Debian的阿里仓库里只有php7.0，下面添加sury软件源
# 四个命令
apt -y install software-properties-common apt-transport-https lsb-release ca-certificates
wget -O /etc/apt/trusted.gpg.d/php.gpg https://mirror.xtom.com.hk/sury/php/apt.gpg
sh -c 'echo "deb https://mirror.xtom.com.hk/sury/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list'   
apt-get update #更新软件源缓存
# 下面安装php7.3
apt install php7.3-fpm php7.3-mysql php7.3-curl php7.3-gd php7.3-mbstring php7.3-xml php7.3-xmlrpc php7.3-zip php7.3-opcache -y
sed -i 's/;cgi.fix_pathinfo=1/cgi.fix_pathinfo=0/' /etc/php/7.3/fpm/php.ini  #出于安全考虑
```
配置nginx：

注释掉默认的服务器配置，添加自定义内容：

```nginx
server {
        listen       80 default_server;
        listen       [::]:80 default_server;
        # 这里是本机IP，也可以写你绑定的域名
        server_name  localhost;

        # 定义网站根目录
        root         /var/www;

        # Load configuration files for the default server block.
        include /etc/nginx/default.d/*.conf;

        location / {
            # 定义首页索引文件的名称
            index index.php index.html index.htm;
        }

        error_page 404 /404.html;
            location = /40x.html {
        }

        error_page 500 502 503 504 /50x.html;
            location = /50x.html {
        }

        # PHP 脚本请求全部转发到 FastCGI处理. 使用FastCGI协议默认配置.
        # Fastcgi服务器和程序(PHP,Python)沟通的协议.
        location ~ \.php$ {
            # 设置监听端口
            fastcgi_pass   127.0.0.1:9000;
            # 设置脚本文件请求的路径
            fastcgi_param  SCRIPT_FILENAME  $document_root$fastcgi_script_name;
            # 引入fastcgi的配置文件
            include        fastcgi_params;
        }
    }
```

上面设置好了fastcgi去监听9000端口的php内容，下面修改php的配置文件：

> 编辑/etc/php/7.3/fpm/pool.d目录下的www.conf文件
>
> 将listen = balabala 换成 listen = 127.0.0.1:9000

然后重新加载nginx配置文件：`nginx -s reload`

重新启动php-fpm：`service php7.3-fpm restart`

---

下面测试一下：

在nginx设置好的根目录/var/www下，新建一个php文件，内容是：`<?php phpinfo(); ?>`

到浏览器访问一下

---

这样LNMP环境就搭建好了

## 十四、安装typecho博客
到官网下载安装程序压缩包 http://typecho.org/download

上传到网页根目录（/var/www）

```shell
cd /var/www
tar -zxvf balabalba.tar.gz  #解压
```

然后先整理一下。。。`mv ./build/* ./`

浏览器访问根目录，开始安装 

> 发现问题：对不起，无法连接数据库，请先检查数据库配置再继续进行安装
>
> 解决：新建一个数据库，名字叫typecho

```mysql
mysql -uroot -p   #因为之前设好了密码，现在需要密码登录
create database typecho;
exit
```

然后继续安装，安装完后进入登录页面，输入密码。

> 再次发现问题：404，原因是还没设置伪静态
>
> 解决：修改nginx配置文件，加入伪静态规则。

```shell
# 在http->server->location / {}语境中加入
# typecho伪静态规则
			if (-f $request_filename/index.html) {
				rewrite (.*) $1/index.html break;
			}
			if (-f $request_filename/index.php) {
				rewrite (.*) $1/index.php;
			}
			if (!-f $request_filename) {
				rewrite (.*) /index.php;
			}
```

到了这里应该就没问题了

后面还可以添加主题、安装插件，感兴趣请自行百度、谷歌，主题插件一般都在GitHub上开源。

学不在入，在出。用好自己的博客。

---

华丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽丽的分界线

---

接下来都是在Windows上操作！

## 十五、介绍node.js
在服务端运行的JavaScript

>  安装包在群文件里有

```powershell
node -v  #检测node版本
npm -v  #检测npm版本
npm config set registry http://registry.npm.taobao.org   #更换淘宝源，切记，不然慢到你吐血
```

## 十六、搭建hexo博客

首先，注册一个Github或者Gitee账号。

```powershell
npm install -g hexo-cli   #安装hexo
hexo -v   #查看hexo版本

# 现在创建一个文件夹，比如blog，然后在命令行进入这个文件夹
hexo init myblog  # 这里的myblog是将要生成的文件夹名字，可以换成其他的  ！！！暂时先用下面的命令！！！
# ！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！
cd myblog
hexo generate  # 生成各种web资源
hexo server   # 启动本地服务
# 现在浏览器访问http://localhost:4000即可

hexo new "文章名"  # 新建文章
# 用编辑器编辑内容
hexo clean
hexo generate
hexo server

npm install --save hexo-deployer-git  # 安装hexo的git插件
# 设置_config.yml
	deploy:
  		type: git
  		repository: #替换成项目地址#
hexo deploy  # 部署
# 要是同步到Gitee仓库，需要更新；GitHub会自动更新
```

原理：利用Node.js在本地渲染以后，生成静态资源，上传至GitHub或者码云

另外，也可以换主题，一般都在GitHub上开源

```powershell
git clone https://github.com/litten/hexo-theme-yilia.git themes/yilia
# 修改一下_config.yml的theme
# 然后还是那几个命令
hexo clean
hexo generate
hexo server
```

---

！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！

> hexo init xxxx实际上是如下命令的集成：

```powershell
git clone https://github.com/hexojs/hexo-starter.git myblog
cd myblog
git submodule init
git submodule update
npm i
```

> 在我写这个文档的时候（2020.12.11）发现21小时前的一个更新hexo-starter的作者把themes下的文件清空了，导致了后面更换主题后执行任何hexo操作都会出现如下错误：
>
> ERROR {
>   err: [Error: EISDIR: illegal operation on a directory, read] {
>     errno: -4068,
>     code: 'EISDIR',
>     syscall: 'read'
>   }
> } Plugin load failed: %s hexo-theme-landscape
>
> **因此此处暂时先将hexo init xxxx替换成如下命令**（将原仓库替换成一个镜像仓库）：

```powershell
git clone https://gitee.com/weilining/hexo-starter.git myblog
cd myblog
git submodule init
git submodule update
npm i
```

---

---

# 然后过段时间缓一缓，就可以分流了！