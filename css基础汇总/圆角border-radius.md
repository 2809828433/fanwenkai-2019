# 圆角border-radius

​	boder-top-left-radius: 左上
	border-top-right-radius:右上
	border-bottom-right-radius:右下
	border-bottom-left-riadus:左下	

border-radius：可以设置一个值到四个值。
	顺序：
		1个值：四个角
		2个值: 左上右下 	右上左下
		三个值:  左上	  	右上左下  	右下 	
		四个值: 左上		 右上	  右下	  左下 	

如何通过border-radius做一个圆

border-radius=50%（盒子宽高一样），其中的50%是以盒子的宽高为参考的

# border-image 边框图片

​	目前IE11以上才支持	

border-image 是一个简写值，分别有以下属性值,

​	**border-image-source	图片地址**

​	**border-image-slice   图片切片**

值：number  | 百分比  {1,4}
	Tip：{1,4} 表示最少一个值，最多四个值指定边框图像顶部，右侧，底部，左侧内偏移量。没有具体的单位值，px em rem都不可以。只可以用数字或者百分比。

​		**border-image-width  图片宽度**

值：lenghth | number | 百分比 {1,4}

​		**border-image-outset  图片外凸**
		**border-image-repeat  图片重复**

值：round平铺占满，位置不够把原来放大一部分，但不会放半个。

​	repeat平铺占满，位置不够放半个

​	stretch不平铺，拉伸或缩小图片 