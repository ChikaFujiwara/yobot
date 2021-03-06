# Windows 运行包（新手推荐）

## 准备服务器

选项 1：租一个服务器，[服务器选择参考](https://yobot.xyz/p/9/)

选项 2：在自己电脑运行

## 安装酷Q机器人

### 下载

#### Windows 使用

yobot 三代基于酷Q机器人和 httpapi 插件实现
如果你第一次使用酷Q机器人，可以直接下载[酷Q-httpapi 整合包](https://ybdown.zimingdh.com/CoolQ_With_Httpapi.7z)

如果你已经使用过酷Q机器人，可以下载[httpapi 插件](https://ybdown.zimingdh.com/Packed_httpapi.7z)

如果你已经使用过 httpapi 插件，或者想额外开启一个 httpapi 插件，可以下载[httpapi 插件分身版](https://ybdown.zimingdh.com/mirror_of_httpapi.7z)

### 环境搭建

参考：[httpapi插件文档](https://cqhttp.cc/docs/)

如果你的windows不是最新版，可能无法启动httpapi插件，请安装Visual C++ 可再发行软件包（[点击下载](https://aka.ms/vs/16/release/vc_redist.x86.exe)）。如果你的系统是 Windows 7 或 Windows Server 2008、或者安装 Visual C++ 可再发行软件包之后仍然加载失败，则还需要安装通用 C 运行库更新（[点击进入官网](https://support.microsoft.com/zh-cn/help/3118401/update-for-universal-c-runtime-in-windows)，选择你系统对应的版本下载安装）

### 配置

参考：[httpapi插件文档配置说明](https://cqhttp.cc/docs/#/Configuration)

由于新装的 httpapi 启动时有时候会重置配置文件，所以如果 httpapi 启动后与下图不符请手动配置一下文件

配置文件位于：`<酷Q运行目录>data\app\io.github.richardchien.coolqhttpapi\config\general.json`或 *QQ号.json* ，将其修改为[这里](https://gitee.com/yobot/codes/9wae4oc8str13huky7g2j56)的配置。

配置正确后，启动 httpapi 插件后会反复出现如下的提示

![配置正确图片](../imgs/8ba6b840bab3ac25.jpg)

## 运行yobot服务

### Windows系统运行包

[点击下载运行包](https://yuudi.github.io/yobot/v3/download-latest.html)

下载yobot运行包，创建一个文件夹解压，启动 yobot.exe 即可。如需更改端口，请启动一次后修改 yobot_config.json 中的 port 字段并重启。

![windows下正确启动图](../imgs/aaf38d1a5cbc1c87.jpg)

![windows下正确yobot与httpapi成功通信](../imgs/8179fdd1e46690b2.jpg)

## 常见问题

### 如何修改运行的端口号

需要修改服务程序的端口号和httpapi的配置文件

服务程序的配置文件在yobot\yobot_config.json，port字段就是端口号，默认值为9222，可以修改为8000至65535之间的数。

httpapi的配置文件如[配置小节](#配置)所示，请将文件中默认端口9222(三处)改为与服务程序相同的端口号。

### 酷Q的日志显示了发送，实际却没有发送

这种情况一般是消息被腾讯屏蔽，常常发生在异地登陆时

解决方法：

* 关闭所有插件，机器人挂机一段时间
* 在远程主机上登录电脑版QQ发一些消息
* 在远程主机上登录QQ网页服务（比如QQ邮箱、QQ安全中心等）
* 在远程主机上玩一玩腾讯的游戏
* 下载QQ安全中心，确认异地登录

## 注意事项

* **请不要使用重要的QQ号作为机器人**
* 系统至少要windows 7或者windows server 2008
* 机器人的数据都是分群存储的，一个机器人可以服务多个群
* 本机器人不包含“签到”、“宠物”等通用功能，如果需要可以在[酷Q插件社区](https://cqp.cc/b/app)搜索下载。
* 发送图片，发送语音等功能必须购买高级版才能使用，yobot三代所有功能均可用文字实现，不需要高级版

容易引起封号的行为：

* 异地登录后立刻修改昵称头像（可以先修改再异地登录）
* 新注册的号在机房ip登录（ip真人鉴别有很多，比如[这个](https://ip.rtbasia.com/)）
* 机器人大量地发长消息（尤其是抽卡，条件允许可以改用图片抽卡）
* 机器人24小时不停发消息（如果真的有需求可以让两个账号轮班）
* 账号在短时间内加了大量的群（可以慢慢加，最好不超过10个群）
* 大量高危账号在同一个ip登录（可以慢慢加，一台服务器最好不超过5个账号）

如果文中下载链接失效，可以使用[备用网盘](https://www.lanzous.com/b00n6dnqh)

## 感谢

* 感谢 **@Ice咖啡丨福** 在技术上的帮助
* 感谢 **@ヒカリ** 提供的竞技场数据
* 感谢 **@超威懒猫** 提供的活动日程数据
* 感谢 **@黑白君** 提供的酷Q Pro账户
* 感谢 **@sana** 对beta版本的测试与bug报告

### 开源软件许可

* HoshinoBot: [https://github.com/Ice-Cirno/HoshinoBot](https://github.com/Ice-Cirno/HoshinoBot)
* aiocqhttp: [https://github.com/richardchien/python-aiocqhttp](https://github.com/richardchien/python-aiocqhttp)
* requests: [https://pypi.org/project/requests](https://pypi.org/project/requests)
* beautifulsoup4: [http://www.crummy.com/software/BeautifulSoup/](http://www.crummy.com/software/BeautifulSoup/)
* pillow: [http://python-pillow.org/](http://python-pillow.org/)
* json5: [https://github.com/json5/json5](https://github.com/json5/json5)
* opencc-python: [https://github.com/yichen0831/opencc-python](https://github.com/yichen0831/opencc-python)
* feedparser: [https://github.com/kurtmckee/feedparser](https://github.com/kurtmckee/feedparser)
* ics-python: [https://github.com/C4ptainCrunch/ics.py](https://github.com/C4ptainCrunch/ics.py)
