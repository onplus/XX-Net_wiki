# 隐私与匿名性说明

## GAE/GoAgent不是匿名工具

XX-Net和Goagent一样，是通过谷歌的GAE服务器实现的代理访问。因此，谷歌可以看到XX-Net代理的所有内容。    
此外，GAE服务器会将你所使用的Appid（以及你的浏览器传出的相关信息，包括 HTTP Headers 等）全文传递给目标服务器，因此XX-Net并不能达到匿名的效果。   
XX-Net，GoAgent，及其他类似的基于GAE的工具，都只是利用Google的大量服务器及免费资源，帮助大家访问墙外的网络而已。换句话说，他们是绕过中国政府封锁的工具，并不是匿名工具。  

## 关于隐私：
### 不会发生什么？
* XX-Net**不会**收集大家扫描的Google IP。因为全国网络环境各异，收集大家扫描的Google IP并**没有意义**。    
* 你的公司、学校或小区的网络管理员不会看到XX-Net所代理的流量，在代理流量到达GAE服务器之前，他们是被加密的。

### 可能会发生什么？
* 你的公司、学校或小区的网络管理员尽管不知道你访问的具体内容，但他们能看到有加密的流量在你的电脑和境外服务器之间来来往往。    
* 谷歌的GAE服务器能看到你上网流量中所有的内容，包括所有https请求。所以，如果你不信任Google，请不要用GoAgent、XX-Net等所有基于GAE进行浏览的工具。
* 当XX-Net自动升级时，当你使用公共appid时，有一些信息会不可避免地被收集。    
具体说明如下：    
+ 可能的隐私泄漏

  1. 你的IP地址
  当XX-Net自动检查升级时，服务器会记录你的IP地址。  
  解决方案：[[关闭自动检查升级|Auto update]]。  

  2. UUID  
  为了控制灰度升级，使用UUID是随机生成的，不会暴露用户信息，但能跟踪是否同一个用户。  
  解决方案：[[关闭自动检查升级|Auto update]]。  

  3. 公共appid  
  从原理上说，你所使用的appid的所有者，有能力看到你的访问内容。    
  因此，本项目的尽量使用作者自己申请的appid供大家公用。  
  通过限制视频请求，一方面能节约公共appid的流量配额，另一方面也鼓励用户[[部署自己的appid|how to create my appids]]，用得更放心。  

特别解释：  
+ XX-Net不愿意搜集任何个人信息

  我们无法保证搜集到的信息，会某一天被黑客拿走。  
  因此我们尽可能地**避免**收集用户的信息。  

## 如何匿名？
对于有匿名需要的用户，请使用Tor软件包:   
https://www.torproject.org/projects/torbrowser.html

匿名不是一个工具就能解决的，请参考：
[[编程随想的博客：“如何隐藏你的踪迹，避免跨省追捕”系列博文|http://program-think.blogspot.com/2010/04/howto-cover-your-tracks-0.html]]

## 总结
+ 如果传输、浏览特别敏感的信息，请使用Tor，并学习如何匿名
+ 普通用户，只需要[[部署自己的appid|how to create my appids]]就足够了