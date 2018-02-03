# deepfakes
[那个NB-AV换头术视频作者的书面教程](https://www.deepfakes.club/tutorial/)

## 1.前言

原理我一个也不懂,仅仅想看一下效果怎么样.部署反正是没问题.

我是搞java的,早想用Python来写爬虫了,但是spring又搞出了SpringBoot.

鉴于我一个都没用过的原理,我还是体验一下最基本的`换头术`这个东西吧.

严格遵守少先队员,热爱人民,热爱祖国的原则的誓言.不要给党在推行社会主义现代化小康社会的道路上添堵.

先放成果

![](http://dl.russellcloud.com/lovemoganna/project/face_swap/task/1960e79278f143e7b1c1e571a48fe3c8/output/477320132.jpg)

原图的结合

![tom](http://dl.russellcloud.com/lovemoganna/project/face_swap/1/img/102668242.jpg)
![jack](http://dl.russellcloud.com/lovemoganna/project/face_swap/1/img/115597135.jpg)

二者结合就成了上面的情况

虽说PS比这个效果好,但是谁不想自动化哪.

如果抱着玩一玩的心态,还是看看吧.

## 2.使用russellCloud

你要先注册,这不行的,要先申请邀请码.所谓邀请码,就是你填上你的个人信息.名字最好和注册的名字一致.我反正是成功了.写全点,毕竟是用人家免费提供的`环境`.

完毕了以后.

可以瞅瞅这个[官方文档](http://docs.russellcloud.com/project/create.html)

不愿意瞅,就看看下面.

### 1.安装Russell-cli
官方有说明是:
````
pip install -U russell-cli
````
我是从docs窗口下安装的,直接复制,粘贴就可以的.

如果你需要看高级用法:`russell --help`

### 2.克隆项目

具体项目地址:

````
$ git clone https://github.com/RussellCloud/deepfakes_faceswap
````

### 3.终端登录

这个登录牛的不行...

图片展示吧:

![](http://upload-images.jianshu.io/upload_images/7505161-8b57f5e1e0b0cdad.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
* 1. 输入命令`russell login`
* 2. 你输入n以后确保你登录的情况下,往下拉,就会有对应的token.把token粘贴进doc窗口,不会显示的,跟你登录centos一样,Token不会显示的.比如:SSO登录核心就是Token.

### 4.新建项目

来到RussellCloud主页，进入控制台，新建一个项目。项目名随便起一个，默认容器环境一定要选择：tensorflow-1.4 。

图示:

![](https://pic1.zhimg.com/80/v2-bd5fda6b032d044bc215de081f7764e4_hd.jpg)


### 5.初始化项目

这个东西在你的项目里面其实有:
`$ russell init --id <project_id>`

或者官方说的
```
#绑定项目（也可以用 init --id <project_id>）
russell init --name tf-mnist

#运行启动指令
russell run "python mnist_cnn.py"
```

run之后的是 run 返回的任务ID。任务ID不同于项目ID。


### 6.启动项目

````
russell run --data f3fadfadf6ac417e9f20813603187344:data "python run.py"
````

任务Id就是下面的划线部分:

![](http://upload-images.jianshu.io/upload_images/7505161-d3dba3556de245fa.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 7.停止项目

````
stop russell 任务ID
````

### 8.看看日志

````
Russell log 任务Id
````


### 9.最终输出的目录
![](http://upload-images.jianshu.io/upload_images/7505161-daf4ff5c5ff70ade.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

上面就是我之前展示成果的目录下的,一张比较融合完整的一张图片了...

## 3.结语

多试试,也挺好的.

## 4.参考文章

[实验对象](https://zhuanlan.zhihu.com/p/33424270)


