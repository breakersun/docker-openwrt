# docker-openwrt

bump to Lean 

实验性项目，紧跟大雕的代码

## 20191212

- 增加了PI Group的最新固件，tag:pigroup

遇到小问题：
docker部署后，DNS不生效，ping始终返回bad address

修复方式：
vi /etc/resolv.conf
将默认的127.0.0.11修改为127.0.0.1

原因不明

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

