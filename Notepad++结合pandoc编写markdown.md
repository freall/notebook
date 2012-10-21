<title>用Notepad++结合Pandoc编写Markdown</title>
<link href='markdown.css' rel='stylesheet'>

# 用Notepad++结合Pandoc编写Markdown

*2012.10.21*
  
之前一直使用MarkdownPad，一直觉得此软件设计的不错，也确实不错。  
今天突然发现两点让我非常不爽。

1. MarkdownPad*自动加上Css代码*，直接加到每一html文件中，让HTML变得很臃肿，不是很适合我。
2. 当然，你可以把它禁用掉，就是定义空的自定义css文件，但是声称的html头是：  
    `<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">`  
这个让我十分不高兴，虽然这个可以运行。

费劲周折，终于找到比较合适的一种在Windows下编辑Markdown的方案了。
就是**用Notepad++结合Pandoc的方式**。

1. Notepad++ 是我非常喜欢的编辑器。
2. Pandoc 功能很强大，也很方便。
3. Pandoc 转换出来的html很干净，我很喜欢。

下面简述下方法。

1. 安装 Notepad++。
2. 安装 Pandoc。
3. 在 Notepad++ 中点“运行”->“运行...”。选择到Pandoc安装目录里面的pandoc.exe。
4. 在命令行后面加上参数：  
`"$(FULL_CURRENT_PATH)" -o "$(CURRENT_DIRECTORY)\$(NAME_PART).html"`
5. 保存。
6. 需要的话可以保存一个快捷键，更方便。

这样编辑完Markdown文件后，运行这个命令，就会在当前文件相同目录下产生一个同名的html文件了，很方便。

---
备注1.Pandoc的简单命令：  
<pre>
pandoc pandoc  in.tex -o out.doc
pandoc -f markdown -t html in.txt -o out.html
</pre>

备注2.Notepad++的变量：  
<pre>
FULL_CURRENT_PATH
    the fully qualified path to the current document.
CURRENT_DIRECTORY
    The directory the current document resides in.
FILE_NAME
    The filename of the document, without the directory.
NAME_PART
    The filename without the extension.
EXT_PART
    The extension of the current document.
NPP_DIRECTORY
    The directory that contains the notepad++.exe executable that is currently running.`
CURRENT_WORD
    The currently selected text in the document.
CURRENT_LINE
    The current line number that is selected in the document (0 based index, the first line is 0).
CURRENT_COLUMN
    The current column the cursor resides in (0 based index, the first position on the line is 0).
</pre>

	  

