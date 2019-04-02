# css权重问题的比较

## 1、权重的比较

> 有没有选中目标元素:
>
> > - 选中目标元素
> >
> >   > - 比较权重
> >   >   - 不同：听权重高的
> >   >   - 相同：谁在后面听谁的
> >
> > - 没有选中目标元素
> >
> >   > - 看谁离目标元素更近一些，谁近听谁的
> >   >
> >   >   > 一样近
> >   >   >
> >   >   > > - 比较权重，权重一样，谁在后面听谁的



```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>猜猜看字体颜色</title>
	<style>
	/* id class html标签 */
	/* 1     1    1  第一个选择器 */
	/* 1     0    3 第二个选择器*/
	/* 0     3    4  */
	/* 100   10    1    */
		/*如果同时选中目标元素，谁的权重高听谁的*/
		/*#box1 .d2 p {
			color: red;
		}
		div div #box3 p {
			color: blue;
		}
		div.d1 div.d2 div.d3 p {
			color: pink;
		}*/
        
		/*如果同时选中目标元素，权重一样 ，那么谁在后面听谁的*/
		/*#box2 .d3   {
			color:red;
		}
		#box1 .d2 p {
			color: blue;
		}*/

		/*如果说选择器没有直接选中目标元素，而是通过继承去影响，那么权重为0*/
		/*div div div p {
			color: blue;
		}*/
	/*	#box1 #box2 #box3 {
			color: pink;
		}
		.d1 .d2 .d3 {
			color: red;
		}*/
        
		/*如果多个选择器都是通过继承去影响的，改咋办?*/
		/*如果都是通过继承去影响，那么谁离目标元素近就听谁的*/
		/*.d1 .d2 {
			color: red;
		}
		div div div {
			color: blue;
		}*/

		/*如果都没有选中目标元素，权重一样，谁在后面听谁的*/
		#box2 .d3 {
			color: blue;
		}
		#box1 .d3 {
			color: red;
		}
	</style>
</head>
<body>
	<div class="d1" id="box1">
		<div class="d2" id="box2">
			<div class="d3" id="box3">
				<p>猜猜我是啥颜色?</p>
			</div>
		</div>
	</div>
</body>
</html>
```

## 2、!important;

​	 !important;英文中的意思:重要的

> Tip:
>
> > 1. !important不能够随便使用，尽量减少使用频率
> > 2. !important 能够提升单独某个属性的权重，不能提高选择器的权重。
> > 3. !important 不影响就近原则 

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		.d1 {
			color:red;
			font-size: 100px;
		}
		div {
			color:blue !important;
			font-size: 80px;
		}
	</style>
</head>
<body>
	<div class="d1">
		hello,world	
	</div>
</body>
</html>
```

