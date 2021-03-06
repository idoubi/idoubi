---
title: QQ空间魔力日志制作教程
tags:
  - Qzone
  - 魔力日志
id: 1
categories:
  - 开发笔记
date: 2013-12-27 04:10:19
---

<div>相信朋友们经常会在自己的QQ空间看到好友转发的诸如此类的日志图片</div>

![](http://blogcdn.idoustudio.com/2013/12/0-2.jpg)

![](http://blogcdn.idoustudio.com/2013/12/0-1.jpg)

![](http://blogcdn.idoustudio.com/2013/12/0-3.jpg)

看着日志图片上显示着自己的 QQ 头像、QQ 昵称、QQ 号码
是不是觉得很不可思议呢？是不是很想知道这些神奇的图片是怎么做出来的？
那么接下来我就结合自己的经验给大家讲一讲这种魔力日志制作的原理和方法。

制作原理：

![](http://blogcdn.idoustudio.com/2013/12/0-4.jpg)
关于魔力日志的制作原理我就不详细说了，相信学过 php 的朋友都懂，上面的截图是网上给的解释，大家可以简单了解一下。看不懂也不要紧，没 php 基础也无所谓，请重点关注接下来的制作步骤。

制作步骤：

1、准备一张希望让别人看到的图片，可根据自己的创意自由发挥。例如：

![](http://blogcdn.idoustudio.com/2013/12/0-5.jpg)

做好图片之后那么接下来要做的就是怎么样把看到这张图片的人的 QQ 信息显示在这张图片上了。

2、下载源代码

源代码里面包含了上面的那张百度搜索的图片，命名为 qq.png，如果大家想制作其他的版本只要重新制作一张 qq.png 图片即可。

源代码下载地址：[http://url.cn/WbjBGF](http://url.cn/WbjBGF)

源代码目录结构：
ip 文件夹：获取浏览者主机 ip，用于空间定位。
font 文件夹：字体包
do.php：关键文件，用于获取浏览者的信息，包括 QQ 昵称，QQ 头像，QQ 号，登录地址等信息。
content.php：内容文件，存放向浏览器输出的内容。
no.png：默认图片，即日志内容页里面的图片（别人点进去才会看到）。
qq.png：目标图片，即想要让别人看到的图片。

3、申请虚拟空间
要把做好的魔力日志图片发到空间让所有人看到，必须有一个虚拟空间，只有把代码和图片上传到空间，才能做出魔力日志。申请虚拟空间的方式有很多，有条件的朋友可以自己在网上买一个 php 空间，或者在网上找一个免费的 php 空间。这里推荐的是百度开发者空间。百度开发者空间申请流程：

[http://jingyan.baidu.com/article/ceb9fb10ebf3f68cad2ba012.html
](http://jingyan.baidu.com/article/ceb9fb10ebf3f68cad2ba012.html)

4、测试服务器

按照第三步给的链接教程将代码上传到百度开发者空间之后，在浏览器输入网址[http://1.idoubi.duapp.com/do.php](http://1.idoubi.duapp.com/do.php)即可看到上传代码中的 no.png 图片，注意网址不要输错，1 是你按照教程填写的版本号，我这里是 1，第三步中的教程里面写的是 0。idoubi 是我自己填的域名，每个人按照自己填的域名和版本号来输入网址。

![](http://blogcdn.idoustudio.com/2013/12/no.png)

如果能看到这张默认图片的话，证明服务器配置正确，接下来就可以去空间写日志了。

5、发表魔力日志

复制地址[http://1.idoubi.duapp.com/do.php](http://1.idoubi.duapp.com/do.php)，在腾讯微博粘贴并广播（网上说可以直接用这个地址，但是我试了不行），生成短地址[http://url.cn/Uy8PZJ](http://url.cn/Uy8PZJ)。复制短地址。

![](http://blogcdn.idoustudio.com/2013/12/0-6.jpg)

进入自己的 QQ 空间写日志，插入图片，选择插入网络图片，输入在腾讯微博生成的短地址，添加，即可插入 no.png 这张网络图片。点击发表，魔力日志制作成功。
![](http://blogcdn.idoustudio.com/2013/12/0-7.jpg)

返回个人中心查看，即可看到根据浏览者对象生成的图片，形式为浏览者的 QQ 信息与 qq.png 图片组合（在源代码未修改情况下，qq.png 不起作用，这里的背景图是白色的）而成的一张图片。（由于浏览器缓存问题，发表日志后立刻回个人中心查看可能看到的还是 no.png 那张图片。这种情况下可以换个 QQ 进入空间看看效果。）

这是我用我的 QQ 空间看到的效果。不知道为什么这里没有显示我的 Qzone 图像，昨天还能显示的，好吧请忽略这个 bug。

![](http://blogcdn.idoustudio.com/2013/12/0-8.jpg)

到这一步魔力日志的制作已经完成了，在空间生成的是源代码默认的显示方式。即没有背景图片，只由浏览者的 QQ 号、QQ 昵称和源代码自定的内容组成的一张图片。那么下面就说一下怎么样制作自己想要的图片表现样式。

6、修改样式
在生成的网站版本处点编辑，进入代码编辑页面。

![](http://blogcdn.idoustudio.com/2013/12/0-9.jpg)打开 do.php 页面，将第 26、27 行代码前面加双斜杠注释掉，27 行后面回车，添加 28 行所示代码。

![](http://blogcdn.idoustudio.com/2013/12/0-10.jpg)
回到个人中心刷新查看，可以看到图片变成了这个样子。
![](http://blogcdn.idoustudio.com/2013/12/0-11.jpg)
按照目标图片的要求，我们只需要保留浏览者的 QQ 昵称和 QQ 号即可。于是我们将 44 至 51 行代码注释掉。

![](http://blogcdn.idoustudio.com/2013/12/psb.png)

刷新之后看到的图片是这个样子的。
![](http://blogcdn.idoustudio.com/2013/12/0-12.jpg)
基本上符合我们的制作要求了，那么接下来就是对 QQ 昵称和 QQ 号调整位置的问题了。在浏览器输入网址[http://1.idoubi.duapp.com/qq.png](http://1.idoubi.duapp.com/qq.png)，可以预览我们的目标图片，用 QQ 截图工具从左上角开始拉一个矩形，截图框显示的数据就是右下角的坐标（左上角为原点），我测出来的坐标是 159x130.于是我们找到 42 行代码，将数据改为 14,0,159,130.

![](http://blogcdn.idoustudio.com/2013/12/psb-1.png)

第一个参数是字体的大小，第二个参数是字体所在行与水平线的夹角，第三、第四个参数分别是信息所处的坐标值。

修改完代码后保存，回到 QQ 空间刷新即可看到修改后的效果。
![](http://blogcdn.idoustudio.com/2013/12/0-13.jpg)

根据信息所处的位置对第三第四个参数做适当的调整，本实例中的最终改的参数为 14,0.159,128.到这一步基本上算完工了。

接下来就是对用户信息的颜色样式进行调整了。根据实际搜索情况我们知道用户信息显示的颜色应该是红色，为了获得红色的 RGB 值，我们还是用 QQ 截图工具，在目标字体上一拉即可获得所需的 RGB 值为 204,0，0.
默认情况下，我们看到 42 行代码的颜色参数是 pink，我们将其改为 red。并在 34 行将 red 的 RGB 值改为 204,0,0.

回到 QQ 空间刷新即可看到最终效果。

![](http://blogcdn.idoustudio.com/2013/12/0-14.jpg)

经过上述步骤，我们就做成了一个简单版本的魔力日志，这样的话发到自己的空间就能让好友们大开眼界了，说不定还会疯狂转载哦。大家还可以根据自己的创意 P 一些有趣的图片，然后按照上述的步骤做成你想要的效果。本文提供的源代码可以获取的用户信息有：QQ 昵称、QQ 号码、Qzone 头像、登陆地址。合理利用的话肯定能够给周围的朋友带来欢乐。赶紧去试一试吧~

备注：
1、本教程是作者艾逗笔参考网上已有的一些教程，根据自己的制作经验原创而成，讲解详细，步骤清晰，力求阅读者能够看懂并能做出自己期望的魔力日志。如有不当之处还请各位看官批评指正
2、通过本教程制作出来的魔力日志存在以下的不足：
1）直接用虚拟空间的网址作为网络图片地址插入后，制作的魔力日志不成功，必须用腾讯微博生成的短地址才能达到预期的效果。
2）不能获取 QQ 签名
3）得到的头像是 QQ 空间头像而不是 QQ 头像.
4）魔力日志发表后分享不产生动态
5）手机空间预览不显示预期效果。
欢迎懂相关技术的朋友针对以上问题与本人交流。
3、如果觉得本教程写的还不错，对你有帮助，就请动动手指分享给你的好友吧。
4、感谢各位支持。
