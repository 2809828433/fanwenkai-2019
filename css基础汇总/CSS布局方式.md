# css布局方式

- 标准文档流以及特性

- 盒子模型

- 浮动（ 清除浮动带来的影响）

- 定位

- 宽高自适应（自适应网页效果）

- 元素居中（元素居中的不同情况）

- 弹性盒子模型

- 响应式布局

- 分栏布局（多列布局）

  

# css定位

**css定位是为了显示层级关系，主要有相对定位、绝对定位、固定定位、粘性定位**

**top / bottom / left / right**

## 1、position:relative  相对定位

 *元素会根据自己原来的位置进行位移，并且不会脱离标准文档流。*

> **作用： **
>
> - 微调元素位置
> - 作为绝对定位的参考点。

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>定位</title>
	<style>
			.d1 {
				width: 200px;
				height: 200px;
				background-color: orange;
				margin: 100px 0 0 100px;
				position: relative; 
				top:10px;
				left: 400px;
				/*right:20px;*/
				/*bottom: 20px;*/
			}
			.d2 {
				width: 300px;
				height: 100px;
				background-color: pink;
				margin-left:100px;
				margin-top: 100px;
			}
	</style>
</head>
<body>
	<div class="d1"></div>
	<div class="d2"></div>
</body>
</html>
```

## 2、position：absolute  绝对定位

​    **绝对定位元素脱离标准文档流**

#### 绝对定位的参考点

> 某个元素设置了绝对定位，需要参考点，分成下面的几种情况：
>
> 1. 没有父元素：
>    top 为首屏屏幕的左上角作为参考
>    bottom就是浏览器窗口，首屏窗口尺寸页面的左下角
> 2. 存在父元素：
>         浏览器会从当前使用绝对定位的元素开始向上一层一层的去找，父元素没有就找祖先元素，直到找到 某个祖先元素的身上具有相对定位或者绝对定位的属性，那么就以这个祖先元素为参考点进行位移；如果没有找到，那么就以网页为参考点进行位移。

**子元素使用绝对定位  父元素最好使用相对定位  子绝父相，保持结构的稳定性**

*tip：子绝父相（经常使用），也可以子绝父绝（比较少使用）*

​       绝对定位的子元素，如果作为参考元素的父元素设置了padding，除非子元素没有设置一些位移的参数，例如top、left等，那么就会被padding影响，可是一旦子元素设置了位置参数，将不会受到影响。

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>绝对定位</title>
	<style>
		.header {
			margin-top: 200px;
			margin-left: 200px;
			width: 600px;
			height: 600px;
			border:3px solid orange;
			position: relative;
		}
		.d1 {
			width: 200px;
			height: 200px;
			border:2px solid red;
			background-color: blue;
			position: absolute;
			top: 10px;
			left: 10px;
		}
	</style>
</head>
<body>
    <div class="header">
		<div>
			<div class="d1"></div>
		</div>
	</div>
</body>
</html>
```



#### 绝对定位的元素如何居中?

- left=50%；

- margin-left=-宽度的一半

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
  	<meta charset="UTF-8">
  	<title></title>
  	<style>
  		.d1 {
  			width: 200px;
  			height: 200px;
  			background-color: red;
  			/*绝对定位的盒子居中，需要left=50% ,margin-left=- 宽度的一半*/
  			position: absolute;
  			left: 50%;
  			margin-left: -100px;
  		}
  	</style>
  </head>
  <body>
  	<div class="d1"></div>
  </body>
  </html>
  ```

  

## 3、position：fixed   固定定位

**固定定位元素脱离标准文档流**

**固定定位针对的是浏览器窗口，以浏览器窗口为参考进行位移。**

*常见的功能，例如返回顶部，窗口广告....*

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>固定定位</title>
	<style>
		.d1 {
			width: 200px;
			height: 200px;
			background-color: red;
			position: fixed;/*固定定位*/
			right:20px;
			bottom:100px;
		}
		.s1 {
			font-size: 20px;
			cursor: pointer;
		}
	</style>
</head>
<body>
    Lorem ipsum dolor sit amet, consectetur adipisicing ...........
    
	<div class="d1">
		lorem
		五秒钟之后不可能关闭 
        <span class="s1"id="s1"onclick="show()">x</span>
	</div>
</body>
<script>
function show() {
	window.open("http://www.baidu.com");
}
</script>
</html>
```

## 4、position：sticky    粘性定位

**粘性定位是相对定位和固定定位的结合体**

> ​       当元素处于屏幕范围之内，元素的定位就相当于是相对定位，而元素一旦脱离了屏幕范围，那么元素的定位属性就会类似于固定定位。

## 5、position ：static  默认值

> ​       元素框正常生成。块级元素生成一个矩形框，作为文档流的一部分，行内元素则会创建一个或多个行框，置于其父元素中。 

## 6、z-index  层级关系

**必须要有定位才能使用，设置元素的层级关系**

> 分两种情况：
>
> > - 如果单纯的比较两个发生位置冲突的标签，那么谁的z-index值大，谁就在上面
> > - 如果发生位置冲突的是两个子元素，那么最应该看的是父元素的层级关系，父元素的层级也就是z-index值小，那么子级层级再高也没有办法改变。
> > - 两个父元素比较层级的时候，如果其中一个父元素的层级z-index没有设置，那么子级是可以通过z-index盖过与之发生冲突的另外一个元素。

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>位置冲突</title>
	<style>
		.d1 {
			width: 200px;
			height: 200px;
			background-color: red;
			position: relative;
			 /*层级关系*/
			 top: 30px;
			 z-index: 2;
		}
		.d2 {
			width: 300px;
			height: 300px;
			background-color: blue;
			position: relative;
			z-index: 1;
			
		}
		.s1 {
			width: 100px;
			height: 100px;
			background-color: pink;
			position: absolute;
			left: 100px;
			top: 190px;
		}
		.s2 {
			width: 100px;
			height: 100px;
			background-color: orange;
			position: absolute;
			left: 125px;
			top: 100px;
			z-index: 10000;
		}
	</style>
</head>
<body>
	<div class="d1">
		<div class="s1"></div>
	</div>
	<div class="d2">
		<div class="s2"></div>
	</div>
</body>
</html>
```

