# 远卓私有云盘：提供私密文件下载服务！
###您可以通过以下方案快速下载云盘文件：
 -github（需代理，高优先级更新）：<a href="https://github.com/zhuyuanzhuo/Cloud/releases">点击跳转</a>（需要代理！）
 -

###遇到问题？
<p>下载速度慢？<a href="https://gh.api.99988866.xyz/">下载加速网站</a>，<a href="https://cloud.tencent.com/developer/article/2213558">下载攻略</a>
<p>需要帮助？点击网页右下角的小蓝标就可以跟客服对话了！
<p>图片云盘（第三方）：<a href="https://smms.app/">中国访问</a>，<a href="https://sm.ms/">代理访问</a>
<p><a href="https://sm.ms/image/FY4KeLNUQrItnuP" target="_blank"><img src="https://s2.loli.net/2023/10/05/FY4KeLNUQrItnuP.jpg" /></a>



# 个人博客技术选型

[![GitHub stars](https://img.shields.io/github/stars/Zephery/newblog.svg)](https://github.com/Zephery/newblog/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/Zephery/newblog.svg)](https://github.com/Zephery/newblog/network)
[![GitHub issues](https://img.shields.io/github/issues/Zephery/newblog.svg)](https://github.com/Zephery/newblog/issues)
[![Twitter](https://img.shields.io/twitter/url/https/github.com/Zephery/newblog.svg?style=social)](https://twitter.com/intent/tweet?text=Wow:&url=https%3A%2F%2Fgithub.com%2FZephery%2Fnewblog)

**网站站点**：[http://www.wenzhihuai.com/](http://www.wenzhihuai.com/)

**Java后端框架**：Spring、Spring MVC、Mybatis、WebSocket（实时推送）、Lucene（搜索系统）、JMX  
**前端框架**：Bootstrap、Jquery、Highcharts、Echarts、WaterFall（瀑布流）、WowSlider（图片切换）  
**分布式相关**：Redisson(分布式锁)、dubbo  
**缓存**：Redis（日志系统等）  
**数据库**：MySQL  
**部署**：Tomcat、Nginx、阿里云服务器、七牛云CDN  
**Python相关**：百度统计的获取、Flask提供文本分析API  
**其他**：MongoDB（目前只用来记录数据库启动）、RabbitMQ（目前只用来记录请求）、畅言

### 注意

**本网站只是前台，还有个[博客管理系统](https://github.com/Zephery/newblogback)，由于是个人使用，没怎么整，有兴趣可以看看**

**此项目涉及到的依赖（例如：百度统计账号、文本分析API等）实在太多，不能直接copy。自己折腾吧，加油，建站（特别是自己的网站）是个锻炼自己的好机会。如果有疑问，可以联系我哦**

**BTW，如果可以，希望给个star或者fork奖励**

### 相关博客文章：<br/>

1. [建站故事与网站架构](https://github.com/Zephery/newblog/blob/master/doc/1.%E5%8E%86%E5%8F%B2%E4%B8%8E%E6%9E%B6%E6%9E%84.md)<br/>
2. [lucene搜索的使用](https://github.com/Zephery/newblog/blob/master/doc/2.Lucene%E7%9A%84%E4%BD%BF%E7%94%A8.md)<br/>
3. [使用quartz来定时备份数据库](https://github.com/Zephery/newblog/blob/master/doc/3.%E5%AE%9A%E6%97%B6%E4%BB%BB%E5%8A%A1.md)<br/>
4. [使用百度统计api做日志系统](https://github.com/Zephery/baidutongji/blob/master/README.md)<br/>
5. [Nginx小集群的搭建](https://github.com/Zephery/newblog/blob/master/doc/6.%E5%B0%8F%E9%9B%86%E7%BE%A4%E9%83%A8%E7%BD%B2.md)<br/>
6. [数据库备份](https://github.com/Zephery/newblog/blob/master/doc/7.%E6%95%B0%E6%8D%AE%E5%BA%93%E5%A4%87%E4%BB%BD.md)<br/>
7. [那些牛逼的插件]()
8. 使用机器学习对微博进行分析<br/>
9. 网站性能优化<br/>
10. SEO优化<br/>

### 网站首页

首页耗了很多时间在里面，包括加载速度，毕竟影响用户的体验。一直都想做的炫酷一点，不过代价是速度越来越慢，光是初次加载到看到页面就需要7秒，加载完需要30秒。这种速度实在不能忍，直到现在全部换成了CDN，去掉了不能访问的链接（谷歌服务）等，不能说特别快，但是至少不会让用户等7秒了。
<div align="center">

![](http://image.wenzhihuai.com/home.png?imageView2/2/w/600)

</div>

### 技术架构图如下(已过时，有空再更新)

一直想在选型上采用点新技术，有些用上确实是完美，但是有些却不知用来干什么好，比如RabbitMQ和MongoDB，毕竟个人网站没有这些业务，有网友说没必要用，毕竟没必要为了业务而业务，等以后有需求了再优化这些技术在博客中的嵌入吧。↖(
^ω^)↗
<div align="center">

![](http://image.wenzhihuai.com/awfawefwefwef.png)

</div>

### 缓存架构如下

起先访问速度实在是太慢了，即使开启了Mybatis的一二级缓存，后来慢慢的加入Ehcache，速度好多了，不过为了模仿大型网站中的多级缓存的概念，还是继续引入Redis作为二级缓存，很好很开心，哈哈哈，不过偶尔网速不好，服务器有点卡的时候，首页的访问还是不能达到满意，后来看开涛的《亿级流量》，感觉把首页每个一段时间抓取，存成静态页面，写到redis，然后每次访问的时候，直接在nginx使用lua访问redis读取然后返回给客户端，奇思妙想还真成了。
<div align="center">

![](https://upyuncdn.wenzhihuai.com/201803170219421253122648.png)

</div>

### 日志系统架构如下

[日志系统](http://www.wenzhihuai.com/log.html)曾经尝试采用过ELK，实时监控实在是让人不能不称赞，本地也跑起来了，但是一到服务器，卡卡卡，毕竟（1Ghz
CPU、1G内存），只能放弃ELK，采用百度统计。百度统计提供了Tongji
API供开发者使用，只是有次数限制，2000/日，实时的话实在有点低，只能统计前几天的PV、UV等开放出来。其实这个存放在mysql也行，不过这些零碎的数据还是放在redis中，方便管理。
除了日志系统，自己对服务器的一些使用率也是挺关心的，毕竟服务器配置太低，于是利用了使用了tomcat的JMX来对CPU和jvm使用情况进行监控，这两个都是实时的。出了这两个，对内存的分配做了监控，Eden、Survivor、Tenured的使用情况。
<div align="center">

![](https://upyuncdn.wenzhihuai.com/201803170304371892629314.png)

</div>

### 文本分类

本人大学里的毕业设计就是基于AdaBoost算法的情感分类，学到的东西还是要经常拿出来看看，要不然真的浪费了我这么久努力做的毕业设计啊。构建了一个基本的情感分类小系统，每天抓取微博进行分类存储在MySql上，并使用flask提供Restful
API给java调用，可以点击[这里](http://www.wenzhihuai.com/weibonlp.html)尝试（请忽略Google的图片）。目前分类效果不是很明显，准确率大概只有百分之70%，因为训练样本只有500条（找不到训练样本），机器学习真的太依赖样本的标注。这个，只能请教各位路人大神指导指导了。
<div align="center">

![](http://image.wenzhihuai.com/QQ%E6%88%AA%E5%9B%BE20170825141127.png)













<script>  
 art()
   function art() {
   var a =""
   var b=""
   while (b != "202245") { //改为你自己的密码！
     a = prompt("请输入“远卓私有云盘”的访问密码！")
   if(a=="202245")
   {
     b=a
   return 0
  }
  if(a !="202245" && a!="")
 {
   if(a == null)
   {
     window.history.back();
     location.reload();//强制刷新
 
     window.location.go(-1); //强制跳转上一界面
   }
   else{
   alert("密码错误，请询问管理员！")
   }
 }
 }
 
   }
</script>  


<script type="text/javascript">window.$crisp=[];window.CRISP_WEBSITE_ID="17d5aae8-6af8-4782-a916-efd31142e0d4";(function(){d=document;s=d.createElement("script");s.src="https://client.crisp.chat/l.js";s.async=1;d.getElementsByTagName("head")[0].appendChild(s);})();</script>
