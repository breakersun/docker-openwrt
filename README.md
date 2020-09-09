# docker-openwrt



实验性项目，紧跟大雕的代码以及PI群最新好用的固件。





## 使用方法



```
docker pull breakersun/openwrt:20200909

docker run --restart always -d --network macnet --privileged breakersun/openwrt:20200909 /sbin/init
```



## tag: 20200910

- openclash-beta





## tag : 20200909

包含如下插件的最新版（截至20200909）：

- ssr plus（lean自带）
- [openclash](https://github.com/vernesong/OpenClash)
- [helloworld](https://github.com/jerrykuku/luci-app-vssr)
- [theme-aragon](https://github.com/jerrykuku/luci-theme-argon)
- [jd-daily-bonus](https://github.com/jerrykuku/luci-app-jd-dailybonus)





## 20191215



pigroup更新最新公测版本，hello world增加新的实用/显示feature.



## 20191212 二更：



感谢群友指点。

- 修复了刚才提到的DNS小问题，现在不需要手动设置任何东西了
- 修复了群主提到的快速切换节点，导致socks5 server断开的问题

Enjoy.



## 20191212

- 增加了PI Group的最新固件，tag:pigroup

### 遇到小问题：
docker部署后，DNS不生效，ping始终返回bad address

- 修复方式（重启失效）：
  vi /etc/resolv.conf
  将默认的127.0.0.11修改为127.0.0.1

- 或者将如下内容，加入开机启动项（重启不失效）：

```
cat > /etc/resolv.conf <<EOF
search lan
nameserver 127.0.0.1
options ndots:0
EOF
```

- 原因不明



## 20191208:

- 更新lean源码以及lieonol仓库源码


## 20191125：

- 更新Lieonol passwall插件，带魔改主题


## 20191122:

- 更新大雕源码
- 更新Lieonol packages源码





## 20191110：

- 增加了https://github.com/Lienol/openwrt-package.git 里面的passwall插件
- 更新lean代码到最新
- 移除了ssr plus添加的按钮，感觉效果不太好，缺少很多过场UI提示



## 新增：

1. 增加frpc，增加nps-client
2. 精简容量，删除多余主题，建议使用默认bootstrap主题
3. 修改ssr plus，在server list页面，增加一个Apply按钮，点击后即时切换到目标节点，并启动ssr

