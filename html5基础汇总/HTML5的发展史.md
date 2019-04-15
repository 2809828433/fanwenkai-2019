# HTML5的发展史

​	HTML5草案的前身名为 Web Applications 1.0，于2004年被WHATWG提出，于2007年被W3C接纳，并成立了新的 HTML 工作团队。    **HTML 5 的第一份正式草案已于2008年1月22日公布**。HTML5 仍处于完善之中。然而，大部分现代浏览器已经具备了某些 HTML5 支持。    2012年12月17日，万维网联盟（W3C）正式宣布凝结了大量网络工作者心血的HTML5规范已经正式定稿。根据W3C的发言稿称：“HTML5是开放的Web网络平台的奠基石。”    **2013年5月6日， HTML 5.1正式草案公布**。该规范定义了第五次重大版本，第一次要修订万维网的核心语言：超文本标记语言（HTML）。在这个版本中，新功能不断推出，以帮助Web应用程序的作者，努力提高新元素互操作性，本次草案的发布，从2012年12月27日至今，进行了多达近百项的修改，包括HTML和XHTML的标签，相关的API、Canvas等，同时HTML5的图像img标签及svg也进行了改进，性能得到进一步提升。 

```
### html5：广义来说是新一代的客户端后台解决方案，狭义来说是HTML第五代
```

### API：接口，功能对外开放的开关。

​	API（Application Programming Interface,[应用程序](http://baike.baidu.com/item/%E5%BA%94%E7%94%A8%E7%A8%8B%E5%BA%8F)编程接口）是一些预先定义的[函数](http://baike.baidu.com/item/%E5%87%BD%E6%95%B0)，目的是提供[应用程序](http://baike.baidu.com/item/%E5%BA%94%E7%94%A8%E7%A8%8B%E5%BA%8F)与开发人员基于某[软件](http://baike.baidu.com/item/%E8%BD%AF%E4%BB%B6)或硬件得以访问一组[例程](http://baike.baidu.com/item/%E4%BE%8B%E7%A8%8B)的能力，而又无需访问源码，或理解内部工作[机制](http://baike.baidu.com/item/%E6%9C%BA%E5%88%B6)的细节。

### 兼容性

​	**支持Html5的浏览器包括Firefox（火狐浏览器），IE9及其更高版本，Chrome（谷歌浏览器），Safari，Opera等；国内的 遨游浏览器（Maxthon），以及基于IE或Chromium（Chrome的工程版或称实验版）所推出的360浏览器、搜狗浏览器、QQ浏览器、猎豹浏览器等国产浏览器同样具备支持HTML5的能力。**

### HTML5 语法

内容类型（ContentType）

​	  HTML5的文件扩展符与内容类型保持不变，仍然为".html"或".htm"。

DOCTYPE声明

  	<!DOCTYPE html>不区分大小写

​	指定字符集编码

```html
 <meta charset="UTF-8">
```

可省略结束标记的元素

 		允许不写结束标记的元素：br、col、embed、hr、img、input、、link、meta    

​                可以省略结束标记的元素：li、dt、dd、p、option、colgroup、thead、tbody、tfoot、tr、td、th

 		可以省略全部标记的元素：html、head、body、colgroup、tbody

省略引号

​		属性值可以使用双引号，也可以使用单引号。

### HTML5  新增语义化标签

```html
section元素 
	表示页面中的一个内容区块
article元素 
	表示一块与上下文无关的独立的内容
aside元素
	是辅助article区域的内容。也可以理解为整个网页的辅助区域
header元素 
	表示页面中一个内容区块或整个页面的标题
footer元素 
	表示页面中一个内容区块或整个页面的脚注
nav元素 
	表示页面中导航链接部分
figure元素 
	表示一段独立的流内容，使用figcaption元素为其添加标题(第一个或最后一个子元素的位置)
 main元素 
	表示页面中的主要的内容(ie不兼容)
hgroup标题的一个分组
mark:标签定义带有记号的文本,在需要突出显示文本时使用 。兼容低版本浏览器：
	<script src=“html5.js”></script>
```

