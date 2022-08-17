---
date created: 2022-06-15
date modified: 2022-07-14
---

在 V2Ray 的安卓、苹果、Windows 等手机和电脑客户端中，路由设置的域名解析策略有三项选择，分别是 **“AsIs”、”IPIfNonMatch”、”IPOnDemand”**。

它们有什么区别？选择哪个最好？

## “AsIs”、”IPIfNonMatch”、”IPOnDemand”三个域名解析策略是什么意思，有什么区别？

**“AsIs”：**  
只使用域名进行路由选择。快速解析，不精确分流。默认值。

**“IPIfNonMatch”：**  
当域名没有匹配任何规则时，将域名解析成 IP（A 记录或 AAAA 记录）再次进行匹配；  
当一个域名有多个 A 记录时，会尝试匹配所有的 A 记录，直到其中一个与某个规则匹配为止；  
解析后的 IP 仅在路由选择时起作用，转发的数据包中依然使用原始域名；  
理论上解析比”AsIs”稍慢，但使用中通常不会觉察到。

**“IPOnDemand”：**  
当匹配时碰到任何基于 IP 的规则，将域名立即解析为 IP 进行匹配。解析最精确，也最慢。

## V2Ray 域名策略解析选择哪个更好？

虽然 V2Ray 官方解释”AsIs”是默认值，但是实际上，在几款**主流客户端中，有的默认值是”AsIs”，有的是”IPIfNonMatch”**。

因此，选择”AsIs”或”IPIfNonMatch”都可以。

但是，如果在自定义路由设置规则时，添加了匹配 IP 的路由代理规则，比如 geoip:cn、geoip:private，或者直接添加的 IP 地址规则，那么，白云居丨 baiyunju.cc 建议您**必须选择位于中间的”IPIfNonMatch”，不然，匹配 IP 地址的路由规则不会生效。**

参考文章：[《V2Ray手机/电脑客户端自定义路由设置规则的写法》](https://baiyunju.cc/7246)　<<<<https://baiyunju.cc/7246>>>>

因此，在 V2Ray 客户端的域名解析策略中，最好选择”IPIfNonMatch”。

更多 V2Ray 教程文章：[《V2Ray客户端使用、配置教程专栏》](https://baiyunju.cc/tag/v2ray) <<<<https://baiyunju.cc/tag/v2ray>>>>

禁止转载丨原文链接：<<<<https://baiyunju.cc/7256>>>>
