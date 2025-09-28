---
title: 🎉 这是我的第一篇hugo博客！
summary: 随便写写搭建个人主页的感想
date: 2025-09-24

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: '图片注解'

authors:
  - admin
  

tags:
  - Daily Life
  - Hugo Blox
  - Markdown

content_meta:
  trending: true
---

你们好 👋

真的是很遗憾，在大四才开始搭建自己的个人主页。契机是，在学习后端开发的知识时，听redisson的课程听到茫然，脑海中突然神游出来一个想法：我是不是可以搭建一个个人主页呢？想到这里，说干就干，好奇心真的是驱使一个人前进的最好引擎。在B站上我搜索到一个up主的视频，指路👉[*天天向上的宇同学*](https://www.bilibili.com/video/BV1Gz4y1f7Qj/?p=1),借此接触到了hugo。可惜这个视频已经是2020年的，视频里的许多内容，比如hugo的网址已经不能对应搜索到了。建议大家去B站直接搜索：**hugo**（有两个2小时的视频，感觉讲的很基础，适合没有**前端知识**的纯小白）；或者简单看看上面那个视频，然后直接去[*官方github*](https://github.com/HugoBlox/theme-academic-cv)上读文档。
{{< toc mobile_only=true is_open=true >}}

### 配置要求

1. 这篇博客适合有一定前端知识，会使用VSCode、cmd命令窗，以及有自己Github账号的人观看。
2. 有些地方可能说的不够详细，建议大家百度关键词，或者去问问GPT，应该都可以解决。


[//]: # '[![The template is mobile first with a responsive design to ensure that your site looks stunning on every device.](https://raw.githubusercontent.com/HugoBlox/hugo-blox-builder/main/starters/academic-cv/preview.png)](https://hugoblox.com)'

### 安装
#### 安装Hugo
去Github安装[**Hugo**](https://github.com/gohugoio/hugo/releases)，我全程用的是windows11，所以下载版本：*hugo_extended_withdeploy_0.150.0_windows-amd64.zip*。然后解压到本地，添加系统环境变量就完成啦！

参考文档：[hugo搭建个人博客(一)-本地部署](https://blog.csdn.net/weixin_44356673/article/details/105827107)
>[!TIP] :memo: 注: 安装hugo是为了能够本地浏览个人网页的样式，进行及时调整，避免一次次上传到Github部署后才能显示样式。

#### 选择个人主页模版
👉 [**用hugo搭建一个属于你的个人主页**](https://hugoblox.com/templates/)

之后，我们点击上面的这个链接，进入到官方网站，选择“浏览免费模版”，然后按照自己的需求选择一个模版，选好之后，网站会申请你的Github账号进行授权。然后，网站会自动生成一个Github仓库。这个**仓库**就是你的个人主页的代码，后续，我们也只需要维护这个仓库就好了。建议先重命名这个仓库为：**xxxx.github.io**，xxxx为你账号的ID。

这样，当我们的个人网站部署好之后，搜索：*xxxx.github.io*，就可以看到你的个人主页了。

### 本地部署
#### 仓库部署到本地
我们在本地新建一个文件夹，然后把仓库git clone到这个地址中。或者，**建议**大家直接在vscode中打开这个文件夹，点击左侧功能栏中的**源代码管理**，利用vscode的git功能，将仓库clone到本地。这样，后续上传我们修改好的文件，就可以直接利用这个功能，而不是再去命令行窗口中配置git push的内容。

参考文档：[GIt——怎样克隆远程仓库到本地（敲详细）](https://blog.csdn.net/hanhanwanghaha/article/details/108616911)
>[!TIP] :memo: 注: 后续上传文件到Github时，可能会出现因为网络波动等等各种原因造成失败。需要大家耐心的多次尝试，或者一步到位科学上网。

#### 预览个人主页
好了，那么现在终于进入了我们的正题，那就是看看我们的主页跑起来之后到底是个什么效果。这里我提供两种方法，一种使用本地的cmd窗口，一种使用vscode的npm脚本。
- **使用cmd窗口**

  我们在主页所在的本地文件夹下，点击上面的地址栏，输入cmd，回车，即可在当前文件夹所在地址唤醒命令行窗口，然后输入命令
  ```cmd
  hugo server -D
  ```
  如果发现报错信息，可以喂给GPT，对应地解决报错。报Warn的话，大家不用担心，可能是模版里自带的一些视频资源加载不了或者无法访问之类的。我这里在第一次运行的时候，就报Error提示我少安装了一个模块，重新安装后，就可以正常启动。最后会告诉我们：“Web Server is available at http://localhost:1313/”。我们直接在浏览器中输入这个地址，就可以看到预览效果了。

- **使用vscode的npm脚本**

  这个npm脚本具体位置实在vscode左侧资源管理器那一竖列中，在下面会有一个折叠的npm脚本菜单。如果没有显示的话，可以点击上面资源管理器的三个点，然后勾选npm脚本，就会显示在下方了。我们找到dev这个功能，然后点击左侧的扳手，进入到package.json文件，修改代码中scripts部分变成如下这个样子：
  ```json
  "scripts": {
      "dev": "hugo server -D",
      "build": "hugo --minify"
    },
  ```
  保存之后，点击dev右侧的三角形运行，测试一下看看有没有成功，还是如上一个方法所示，进入到1313端口，就可以看到我们的主页了。
>[!TIP] :memo: 注: 如果大家使用命令行方法运行，在运行成功后不要关掉窗口，否则，浏览器上的页面会失效。此外，本地运行网页的好处就是，当我们这边对应修改了文件中的内容，保存之后，网页上的信息就会自动更改，实现实时预览。

#### 修改个人主页
那么，下面我们开始修改我们的主页。模版的修改逻辑大致相通，建议大家参考[官方文档](https://docs.hugoblox.com/)。唯一美中不足的是，文档没有实现完全的汉化，阅读起来稍微麻烦一点。我这里简单举例：**如何修改个人主页的图标：**

我们先在网页上找好我们喜欢的图标，推荐[阿里巴巴矢量库](https://www.iconfont.cn/)。下载到本地后，重命名为**icon.png**，并调整尺寸为**512x512**，将其保存到地址**assets/media**下。理论上，保存好之后，刷新网页，大家就能看到对应的标签栏上的网页图标了。

  参考文档：[官方教程](https://docs.hugoblox.com/getting-started/customize/#website-icon)

参考官方文档，大家就可以修改各种布局，文字样式，添加背景图，写个人博客等等。所以这里不多赘述，给大家推荐一些可能会用到的资源网站，大家自取。
- [阿里巴巴矢量图标库](https://www.iconfont.cn/)
- [markdown语法教程](https://markdown.com.cn/)
- [一个找emoji的网站](https://emojifinder.com/)

#### 上传到Github
当主页的内容修改好了之后，我们就可以把这些改好的内容利用vscode的git功能上传到Github。我们还是点击功能栏中的**源代码管理**，可以看到在更改那一栏中显示了所有修改的内容。接着，在最上面的提交按钮上面填写这次修改的消息，方便提示自己这次提交了什么内容，再点击**提交**、**同步更改**，耐心等待上传完成。还是那句话，如果上传失败，可以对应问GPT报错信息怎么解决，如果是网络问题，只能多次耐心尝试。

### 在Github部署网站
在完成上传的步骤后，距离网站正式运行只差一步。我们登录Github，找到个人主页的仓库，点击上面功能栏里的**actions**，两次选择**Run workflow**。可以看到我们刚刚上传内容的自己设置的提示消息正在变黄。我们点击进去，可以看到deply.yml那一栏中有build的流程，耐心等待，等**build和deply**都变成绿色的完成状态后，就可以点击deply下面的那一个链接。这就是我们已经部署好的个人网页，这里展示我的主页的链接：[我的主页](https://xiaozhexz246.github.io/)。

参考文档：[官方教程](https://docs.hugoblox.com/tutorial/blog/step-6/)

### 结语
恭喜你，看到这里，说明你已经大致了解了个人主页的搭建过程。那么现在就去动手实践一下，搭建属于你的个人主页吧！

### License

Copyright 2016-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/HugoBlox/hugo-blox-builder/blob/main/LICENSE.md) license.
