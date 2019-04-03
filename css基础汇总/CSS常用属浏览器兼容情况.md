# css常用属浏览器兼容情况

#### 盒模型属性

```css
(全兼容)
	width  height  margin
	border  border-width  border-color  border-style

(IE6-不支持)
	min-width  max-width  min-height  max-height
```

#### 布局类属性

```css
(全兼容)
	display  float  clear
	position  left  right  top  bottom  z-index
	overflow overflow-x overflow-y clip visibility

(注意)
	IE7-浏览器不支持table类属性值
	IE6-不支持固定定位position:fixed
	IE不支持resize	
```

#### 文本类属性

```css
(全兼容)
	font  font-family  font-size  font-style  font-variant  font- 		weight  line-height  @font-face
	text-indent  text-align  vertical-align  text-transform  text-		decoration  text-overflow
	word-spacing  letter-spacing  white-space  	

(注意)
	IE7-浏览器中vertical-align的百分比值不支持小数行高	
```

#### 修饰类属性

```css
(全兼容)
	background  background-color  background-image  background-repeat
	background-position
	color  cursor
	命名颜色  16进制  RGB
	
(IE8-不支持)
	background-attachment  background-clip  background-size
	opacity  RGBA	
```

#### 其他类属性

```css
(全兼容)
	通配选择器  *  ;  元素选择器  div  ; 类选择器     .box  ;
	ID选择器   #box  ;  后代选择器   div a  ;  分组选择器   h1,p


(IE6-不支持)
	属性选择器    h1[class]
	子元素选择器  ul > li
	相邻兄弟选择器 div + p
(IE7-不支持)
	通用兄弟选择器 div ~ p
	
伪元素
	(只有当选择器部分和左大括号之间有空格时，IE6-浏览器才支持)
	:first-letter
	:first-line

(IE7-不支持)
	:before
	:after
(IE8-不支持)
	::selection
	
伪类
	(全兼容)
	:link
	:visited

(IE6-不支持给<a>以外的其他元素设置伪类)
	:hover
	:active  
	
单位
(全兼容)
	px  in  cm  mm  q  pt  pc  em  ex  ch
	
(IE8-不支持)
	rem
```

