<title>Nginx+Tornado+Supervisord搭建服务器</title>
<link href='markdown.css' rel='stylesheet'>

# Nginx+Tornado+Supervisord搭建服务器

*2012.12.02*

之前用wep.py+fastcgi+nginx搭建服务器，感觉非常不爽。
今天在偶然翻起Tornado，赶脚不错，之后发现其部署写是相当简单，
于是学习了下。

Tornado本身就是高性能的Server，用Nginx处理静态，同时反向代理到
Tornado做动态，再合适不过了，官方的部署介绍也是这么说的。

余下的Supervisord用于监控进程，可以起多个Tornado线程用Nginx做负载均衡。
非常合适。

参考网页：

* [http://www.tornadoweb.cn/documentation]()
* [http://serholiu.com/]()


<br />
<br />    

<!-- UY BEGIN -->
<div id="uyan_frame"></div>
<script type="text/javascript" id="UYScript" src="http://v1.uyan.cc/js/iframe.js?UYUserId=1698680" async=""></script>
<!-- UY END -->
