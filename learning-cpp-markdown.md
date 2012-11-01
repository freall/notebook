<title>学习cpp-markdown</title>
<link href='markdown.css' rel='stylesheet'>

# 学习cpp-markdown

*2012.11.01*

前一段时间一直在寻找windows下的markdown解释器，使用了MarkdownPad和MEditor，感觉非常不爽。
而且有些解释是错的。

于是后来就有了[Notepad++结合pandoc编写markdown](Notepad++结合pandoc编写markdown.html )，
用起来还是很满意的。但是毕竟还是要装pandoc，做一些设置。而且pandoc实际上功能非常强大，
包含很多标记语言的解释器，这样太大材小用了。

于是想自己找一个Markdown解释器的源码看看能不能自己弄个Notepad++的插件，
或者自己搞个带界面。于是就找到了
github上的[cpp-markdown](https://github.com/sevenjay/cpp-markdown)，
或者sourceforge上的[cpp-markdown](http://sourceforge.net/projects/cpp-markdown)。

作者在README里面说还没有加wchar_t的宽字符的支持，运行之后也发现中文的md文件，
解释出来在命令窗口显示一堆乱码。于是就想着改一下源码，让支持下wchar_t，多个晚上，
诸般尝试，均以失败告终。

不过今晚，在试一个Demo的时候发现，可能是显示虽然是乱码，用流输出到文件中就不一定了，
想到这里立马就将cpp-markdown里面main.cpp里面的输出改到了一个文件，果然，输出一切正常。

太给力了，以后考虑将用这个源码写一个Notepad++的插件，如果心情好的话，放心，这不是一个承诺。


<br />
<br />  
  
<!-- UY BEGIN -->
<div id="uyan_frame"></div>
<script type="text/javascript" id="UYScript" src="http://v1.uyan.cc/js/iframe.js?UYUserId=1698680" async=""></script>
<!-- UY END -->