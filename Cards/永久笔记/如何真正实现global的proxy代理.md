---
date created: 2022-06-09
date modified: 2022-07-20
---

用 v2ray 进行翻墙，只会 proxy 部分走应用层的 app。终端执行的 python 脚本不经应用层，无法 proxy。需要使用 [[proxifier]] 进行全局代理，转发流量至 v2ray 的 sock5 端口
