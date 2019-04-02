# css的样式

## 1、超链接的美化 a

> a:link {color: #FF0000}   /* 未访问的链接 */
> a:visited {color: #00FF00}  /* 已访问的链接 */
> a:hover {color: #FF00FF}  /* 鼠标移动到链接上 */
> a:active {color: #0000FF} /* 选定的链接 */

**tip：**

- 写的时候一定要按照顺序来写，但是可以省略某个状态。
- a:hover 可以单独使用，其余的不能单独使用。

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>超链接的美化</title>
	<style>
		a {
			color:red;
		}
		a:link {
			color: #ccc;
		}
		a:visited {
			color: purple;
		}
		a:hover {
			color: orange;
		}
		a:active {
			color: green;
		}
	</style>
</head>
<body>
		color: #ccc;
		}
		a:visited {
			color: purple;
		}*/
		a:hover {
			color: orange;
		}
		/*a:active {
			color: green;
		}*/
	</style>
</head>
<body>
    <a href="http://www.huawei.com" title="百度一下，未必知道" target="_blank">百度</a>
</body>
</html>
```

## 2、背景属性 background

> - **background-color 背景颜色**
>
>   > 英文单词（red）、十六进制（ #ccc）、rgb(23,23,23)
>   >
>   > 实际开发的时候最好全部使用十六进制
>
> - **background-image 背景图片 **
>
>   > background-image:url("图片的地址");  *image可以省略不写*
>   >
>   > 给一个标签设置背景图片必须给这个标签设置宽度和高度，否则图片出不来。
>
> - **background-repeat 背景图像是否重复/平铺**
>
>   > 属性值:   no-repeat 不重复/平铺
>   >
>   > ​      		repeat-x 横轴重复/平铺
>   >
>   > ​      		repeat-y 纵轴重复 /平铺
>
> - **background-position 图片位置**
>
>   > background-position:向右偏移量px    向下偏移量px;
>   >
>   >  偏移量可以为正也可以为负 
>   >
>   > 也可以：background-position:top  left / center  center  /  right  bottom；组合使用  
>   >
>   > **background-position属性可以应用于雪碧图(又称css精灵)，通过background-position位移显示出局部的位置，以减少向服务器发起的请求次数**
>
> - **background-attachment: fixed/scroll; 背景固定 **
>
>   > fixed：固定，一旦设置了这个属性，那么网页的背景就不会随着网页的滚动而滚动。
>   >
>   > scroll：随内容一块滚动。 

**简写**：

*background:url() no-repeat center top;*

*能使用简写的时候尽可能的使用简写*

***网页上常用的图片格式* **

> 1）jpg :有损压缩格式，靠损失图片本身的质量来减小图片的体积，适用于颜色丰富的图像;(像素点组成的，像素点越多会越清晰 )
>
>  2）gif：无损压缩格式，支持透明，支持动画，适用于颜色数量较少的图像; 
>
> 3）png:无损压缩格式，支持透明，不支持动画，(是fireworks的 源文件格式)，适用于颜色数量较少的图像.  

## 3、文本属性

> - **direction  设置文本方向**
>
>   > 属性值：ltr  从左向右        rtl   从右向左
>
> - **letter-spacing ：value 设置英文字母或汉字的字符间距 ，可以为负值**
>
> - **text-align 设置文本水平对齐方式**
>
>   > 属性值：left（左对齐）、center（居中）、
>   >
>   > ​		right（右对齐），justify（两边对齐）
>   >
>   > *tip：此属性对图片也是有效果的，但是图片不能是块级元素，不能产生浮动。*
>
> - **text-decoration 给文本添加修饰**
>
>   > 属性值：none 取消文本的默认样式        
>   >
>   > ​		underline  给文本添加一条下划线
>   >
>   > ​            	overline 给文本添加一条上划线     
>   >
>   > ​		line-through 穿过文本的一条线
>
> - **text-indent  缩进元素文本的首行**
>
>   > px是具体长度 ， 百分比是基于父元素宽度的百分比；
>   >
>   > text-indent可以取负值； 
>   >
>   > text-indent属性只对第一行起作用。 
>
> - **text-transform 控制元素中的字母大小写，设置字母的样式**
>
>   > 属性值：none  无转换
>   >
>   > ​		capitalize  每个字母的首字母大写
>   >
>   > ​		uppercase  每个字母都大写
>   >
>   > ​		lowercase  每个字母都小写
>
> - **word-spacing 控制英文单词词距**
>
> - **vertical-align 垂直对齐方式（基线为准）**
>
>   > 属性值 :  top（上）、middle（中）、
>   >
>   > ​		bottom（下）、baseline（默认状态）
>   >
>   > **tip:基线的产生来自内容，如果没有内容，则元素自动以底部为基线对齐**
>
> - **line-height  行高**
>
>   > - eg：line-height:20px; line-height:2em; (当行高的单位省略时，默认为em) 
>   >
>   > - 当行高等于容器（父元素）的高时，可以实现文本垂直居中（**只适用于单行文本**）
>   >
>   > - 当单行文本的行高小于容器的高时，可实现单行文本在容器中垂直中齐以上；
>   >
>   > - 当单行文本的行高大于容器的高时，可实现单行文本在容器中垂直中齐以下；
>   >
>   >   **多行文本垂直居中：**
>   >
>   >   - 第一步：padding-top=(高度-总行高)/2
>   >   - 第二步：盒子的高度-padding-top=盒子的新高度
>
> - **layout-flow 控制文本流**
>
>   > 属性值：horizontal（自左向右）
>   >
>   > ​		vertical-ideographic（自上而下）
>   >
>   > **tip：专门用于IE的一个属性**
>
> - **white-space 空余空间**
>
>   > 属性值：normal  默认值
>   >
>   > ​		nowrap  当前文本不会换行，直到有br标签，强制将文本放在一行上
>   >
>   > ​		pre  类似于<pre>标签，原样输出，保留空格符，但不换行
>   >
>   > ​		pre-wrap  保留空格符，但内容会正常换行
>   >
>   > ​		pre-line  不保留空格符，合并空白字符，但保留换行符
>   >
>   > ​		inherit  继承
>
> - **font-size 字体大小**
>
>   > 单位：px  rem   em   pt（磅）
>   >
>   > 系统默认字体大小为16px
>   >
>   > rem是以根元素（html）的font-size大小为参照物 
>   >
>   > ​	当html的font-size:100%时,1rem=16px
>   >
>   > em是以父级元素的font-size大小为参照物
>   >
>   >  pt（磅）  9pt=12px
>
> - **color  字体颜色**
>
>   > 三种表示颜色属性值：英文   十六进制   rgb
>
> - **font-family  字体样式/字体族科**
>
>   > - 当字体是中文字体时，需加双引号；
>   >
>   > - 当英文字体由多个单词组成时，需加双引号如（“Times New Roman”）
>   >
>   > - 当英文字体只有一个单词组成是不加双引号；如：（Arial）； 
>   >
>   > - Windows中文版本操作系统下，中文默认字体为宋体或者新宋体，英文字体默认为Arial.
>   >
>   >   **tip：若要同时设置不同的字体，英文字体必须在中文字体的前面，字体之间用逗号隔开**
>
> - **font-weight  字体粗细**
>
>   > 属性值：bold(字体变粗)、bolder(更粗)、normal（正常）
>   >
>   > ​		也可以设置值：100-900
>
> - **font-style 字体倾斜**
>
>   > 属性值：normal 取消倾斜，常规显示
>   >
>   > ​		italic(斜体字)
>   >
>   > ​		oblique(让现有字体发生倾斜)
>   >
>   > **tip：**
>   >
>   > ​      **italic和oblique都是倾斜的文字, 但区别在于italic是指     斜体字，而oblique是倾斜的文字，对于没有斜体的字体应该使用Oblique属性值来实现倾斜的文字效果. **
>
> - **text-overflow 省略号**
>
>   > clip不显示省略号/ellipsis显示省略号
>   >
>   > **要想让元素能够显示省略号，需要满足下面的条件:**
>   >
>   > - 元素要有具体的宽度
>   > - 元素要在一行上显示 white-space:nowrap
>   > - 溢出的元素要隐藏掉:overflow:hidden;
>   > - 设置text-overflow:ellipsis; 溢出内容显示为省略号。

## 4、列表属性

> - **list-style-type  列表样式)**  (type 可以省略）
>
>   > 属性值：none(去掉列表符号)  
>   >
>   > ​		disc(实心圆)
>   >
>   > ​		square(实心方块)
>   >
>   > ​		circle(空心圆)
>
> - **list-style-image：url(所使用图片的路径及全称)；将列表的样式替换成url引入的图片**
>
> - **list-style-position:outside(外边)/inside(里边)；** 
>
>   > outside(外边) 比如：无序列表的小黑点不在元素内
>   >
>   > inside(里边)    比如：无序列表的小黑点在元素内

## 5、边框属性

> - **border-width  边框宽度** 
>
> - **border-color  边框颜色 **
>
> - **border-style  边框样式 **
>
>   > solid(实线)、dashed(虚线)、dotted(点划线)、
>   >
>   > double(双线)、none(去掉边框) 
>
>   **简写：border:width  style  color; **
>
>   可单独设置一方向边框 ：
>
>   > border-top 、border-right 、 border-bottom  、border-left 
>
> - **border分为内边框和外边框**
>
>   > - 内边框(默认边框)：占有元素实际的宽度和高度
>   > - 外边框：不占用元素的宽度和高度

## 6、溢出隐藏

> **内容溢出 ： 文字 **
> 属性值：
>
> - visible:默认值。当容器内容溢出了容器时，不采取任何行动，任由内容溢出。
>
>   > - 包含子元素的父元素(包含块)在ie6-会出现延伸的情况，变成可以包裹住子元素的宽度。
>   > - 在ie7- 会存在另外一种情况，使用button 按钮 或者input type=button 这两种类型的按钮，都会出现按钮当中字越多，按钮两边的padding越大。
>
> - hidden : 隐藏，将溢出的内容隐藏。
>
> - scroll:滚动，如果存在溢出的内容，将以滚动条的形式展示。
>
>   auto:自动。	
>
>   > 在ie8+ 还有火狐浏览器 在解释overflow:scroll或者overflow:auto的时候会存在padding-bottom的缺失。
>
> - inherit：继承
>
>   > **overflow失效:**
>   > 当子元素处于绝对定位的状态，并且溢出了父元素。这个时候父元素的overflow:hidden或者其他属性都会失效。
>   > **解决方案:**
>   > 给需要溢出隐藏的包含块设置position:relative;
>
> - overflow-x:visible/hidden/auto/scroll    overflow-y:visible/hidden/auto/scroll 能够通过这两个属性单独的设置某一个方向的溢出。
>
>   **tip:overflow主要用来解决溢出的问题，溢出可以分两种，一种是文字溢出，一种是元素溢出。**

## 7、不透明度 opacity

> - opacity:value   0 - 1   会影响元素内的文字，也让其变成透明
> - rgba(0-255,0-255,0-255,0-1)  rgba(10,20,30,0.3)  则只负责图像，不会影响文字。
> - IE9以下浏览器写法：filter:alpha(opacity=value);取值范围 0-100

## 8、隐藏、消失

> - visibility:hidden   元素隐藏  ：元素隐藏了，但还占有空间 (会使对象不可见，但该对象在网页所占的空间没有改变，等于留出了一块空白区域)
> - display:none   元素消失 ：元素彻底消失了，不占有空间

## 9、flash动画

> 引入一个flash
>
> ​	<object>
> 		<embed width="300" height="300" wmode="transparent" src="./images/f001.swf"  ></embed>
> 	</object> 
> 字幕
>  <marquee 
> behavior（行为）="scroll(滚动)/alternate（晃动）"   direction（方向）="up(从下向上)/down（从上向下）/left（从右向左）/right（从左向右）" 
> scrollamount（滚动速度）="value"   height="value(上下滚动范围)"     width=""(左右滚动范围)>
> 内容