# clash
经过我多年的折腾，确认这是翻墙首选，跨全平台，学习成本最低，最稳定。
# 下载预编译好的二进制文件
## GUI版本
[Clash for Windows](https://downloads.clash.wiki/clash_for_windows_pkg)  
[Clash for iOS](https://apps.apple.com/app/stash/id1596063349)(Stash)  
[Clash for Android](https://downloads.clash.wiki/ClashForAndroid)  
[Clash for macOS](https://stash.ws/)(Stash)  
[ClashX Pro(macOS)](https://install.appcenter.ms/users/clashx/apps/clashx-pro/distribution_groups/public)  
[Clash for OpenWrt](https://github.com/vernesong/OpenClash/releases)  
参考来源：https://clash.wiki/
## 非GUI版本
从这里下载：https://downloads.clash.wiki/ClashPremium/
# 生成配置文件
在$HOME目录下创建配置clash的配置目录：$HOME/.config/clash  
在配置目录中需要生成一个config.yaml文件, 它描述了代理节点的位置信息，通常是从机场购买的服务，可以阅读本项目中的.config/clash/config.yaml文件内容以了解购买机场服务的大致过程  
另外clash还需要Country.mmdb来进行启动，.config/clash/Country.mmdb在本工程中已经提前下载好了，你也可以从[release页面](https://github.com/Dreamacro/maxmind-geoip/releases/)下载最新版本或者历史版本  
配置好.config/clash/config.yaml后，将.config/clash/移动至$HOME下即完成配置。
# 使用
启动clash正常输出：
~~~bash
$ ./clash
14:09:59 INF [Config] initial compatible provider name=🇯🇵 日本节点
14:09:59 INF [Config] initial compatible provider name=🇨🇳 台湾节点
14:09:59 INF [Config] initial compatible provider name=🇭🇰 香港节点
14:09:59 INF [Config] initial compatible provider name=♻️ 自动选择
14:09:59 INF [Config] initial compatible provider name=🌏 国内媒体
14:09:59 INF [Config] initial compatible provider name=🌍 国外媒体
14:09:59 INF [Config] initial compatible provider name=🚀 Nexitally
14:09:59 INF [Config] initial compatible provider name=Ⓜ️ 微软云盘
14:09:59 INF [Config] initial compatible provider name=📹 油管视频
14:09:59 INF [Config] initial compatible provider name=🛑 广告拦截
14:09:59 INF [Config] initial compatible provider name=🇰🇷 韩国节点
14:09:59 INF [Config] initial compatible provider name=🎯 全球直连
14:09:59 INF [Config] initial compatible provider name=📲 电报消息
14:09:59 INF [Config] initial compatible provider name=🚀 手动切换
14:09:59 INF [Config] initial compatible provider name=🍃 应用净化
14:09:59 INF [Config] initial compatible provider name=🌍 其他地区
14:09:59 INF [Config] initial compatible provider name=🐟 漏网之鱼
14:09:59 INF [Config] initial compatible provider name=📢 谷歌FCM
14:09:59 INF [Config] initial compatible provider name=🇺🇲 美国节点
14:09:59 INF [Config] initial compatible provider name=🍎 苹果服务
14:09:59 INF [Config] initial compatible provider name=💬 OpenAi
14:09:59 INF [Config] initial compatible provider name=Ⓜ️ 微软服务
14:09:59 INF [Config] initial compatible provider name=🎶 网易音乐
14:09:59 INF [Config] initial compatible provider name=🇸🇬 狮城节点
14:09:59 INF [Config] initial compatible provider name=🎥 奈飞视频
14:09:59 INF [Config] initial compatible provider name=📺 哔哩哔哩
14:09:59 INF [Config] initial compatible provider name=📺 巴哈姆特
14:09:59 INF [Config] initial compatible provider name=🎮 游戏平台
14:09:59 INF [API] listening addr=0.0.0.0:9090
14:09:59 INF inbound create success inbound=http addr=:1079 network=tcp
14:09:59 INF inbound create success inbound=socks addr=:1080 network=tcp
14:09:59 INF inbound create success inbound=socks addr=:1080 network=udp
~~~
确保clash运行后，在terminal的session中开启代理：
~~~bash
$ export all_proxy=socks://127.0.0.1:1080
$ export https_proxy=http://127.0.0.1:1079
$ export http_proxy=http://127.0.0.1:1079
$ curl google.com
<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="http://www.google.com/">here</A>.
</BODY></HTML>
~~~
# 免责声明
你不应该在任何受限的且未经授权的网络环境中使用翻墙技术（中国境内/公司内网/特殊局域网等）🐶
