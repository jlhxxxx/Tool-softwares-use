# Markdown 语法
***
# 区块元素 
## 1. 段落和换行
一个 Markdown 段落是由一个或多个连续的文本行组成，它的前后要有一个以上的空行（空行的定义是显示上看起来像是空的，便会被视为空行。比方说，若某一行只包含空格和制表符，则该行也会被视为空行）。普通段落不该用空格或制表符来缩进。  
*两个空格加回车等于换行*
## 2. 标题
两种形式
This is an H1
=============

This is an H2
-------------
或
#     这是 H1

## 这是 H2

###### 这是 H6 #（可在行尾加任意#闭合，只为美观）
## 3. 区块引用
> 这里是引用
> > 引用中的引用  
> 
> * 第一行
> * 第二行
> ### HAHA
## 4. 列表
Markdown支持有序列表和无序列表。无序列表使用星号、加号或是减号作为列表标记：

*   Red
*   Green
+   Red
+   Green
-   Red
-   Green 

有序列表则使用数字接着一个英文句点：

1.  one
2.  two
6.  three（前面序号无所谓目前来说）    
	fell(先用tab) 
	> good  
	
		代码区块（tab两次）
	
1986\. what is up?(避免生成列表用\)   
## 5. 代码区块
	tab一次就够了
	<p>Here is an example of AppleScript:</p>

	<pre><code>tell application "Foo"
		beep
	end tell
	</code></pre>
## 6. 分割线
你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。
* * *

***

*****

- - -

---------------------------------------
# 区段元素
## 1. 链接
Markdown 支持两种形式的链接语法： 行内式和参考式两种形式。不管是哪一种，链接文字都是用 [方括号] 来标记。  
要建立一个行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可  
This is [an example](http://example.com/ "Title") inline link.  
参考式的链接是在链接文字的括号后面再接上另一个方括号，而在第二个方括号里面要填入用以辨识链接的标记，在文件的任意处，你可以把这个标记的链接内容定义出来：  
This is [an example][id] reference-style link.

[id]: http://example.com/  "Optional Title Here"
I get 10 times more traffic from [Google][] than from
[Yahoo][] or [MSN][]（隐式链接）.

  [google]: http://google.com/        "Google"
  [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
  [msn]:    http://search.msn.com/    "MSN Search"
## 2. 强调
Markdown 使用星号（*）和底线（_）作为标记强调字词的符号，被 * 或 _ 包围的字词会被转成用斜体签包围，用两个 * 或 _ 包起来的话，则会被转成加粗

*single asterisks*  

_single underscores_
  
**Pdouble asterisksP**

__*double underscores*__

\*this text is surrounded by literal asterisks\*
## 3. 代码
如果要标记一小段行内代码，你可以用反引号把它包起来（`）

Use the `printf()` function.  

如果要在代码区段内插入反引号，你可以用多个反引号来开启和结束代码区段：

``There is a literal backtick (`) here.``
## 4. 图片
Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种样式： 行内式和参考式。
行内式的图片语法看起来像是：  
![Alt text](https://pic4.zhimg.com/d5422732754a69792853b6028f2a75df_b.png "Optional title")

参考式的图片语法则长得像这样：  
![Alt text][id]  
[id]: url/to/image  "Optional title attribute"
# 其他
## 1. 反斜杠
Markdown 可以利用反斜杠来插入一些在语法中有其它意义的符号，例如：如果你想要用星号加在文字旁边的方式来做出强调效果（但不用 斜体 标签），你可以在星号的前面加上反斜杠，Markdown 支持以下这些符号前面加上反斜杠来帮助插入普通的符号：

	\   反斜线
	`   反引号
	*   星号
	_   底线
	{}  花括号
	[]  方括号
	()  括弧
	#   井字号
	+   加号
	-   减号
	.   英文句点
	!   惊叹号
## 2. 自动链接
Markdown 支持以比较简短的自动链接形式来处理网址和电子邮件信箱，只要是用尖括号包起来， Markdown 就会自动把它转成链接。一般网址的链接文字就和链接地址一样：<http://example.com/>

参考资料：[Markdown 语法说明(简体中文版)][1] <http://wowubuntu.com/markdown/>
[1]:http://wowubuntu.com/markdown/ "lalala"