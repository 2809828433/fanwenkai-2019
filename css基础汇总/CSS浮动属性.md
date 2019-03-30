# CSS浮动属性

## 浮动的标准特性:

### 1.让元素脱离标准文档流

### 2. 浮动会让元素相互紧贴

### 3. 会存在字围效果

### 4. 收缩效果

## 浮动元素带来的影响解决方案:

​	1. 给父元素(必须是子元素发生了浮动)设置一个具体的高度
	2. 使用clear:both属性 

1. 使用:after :before(伪类)来实现。
   1. overflow:hidden
      1. display不为none
      2. 触发BFC

## *语法：float:none/left/right;*

浮动的**目的**：就是**让竖着的元素横着显示**

一个元素设置float：left/right;时，元素会脱离文档流（半脱离），不占空间；
有三个取值：

### left:元素向左浮动

### right:元素向右浮动

### none:默认值，不浮动。

![img](file:///C:/Users/Administrator/Desktop/%E8%80%81%E5%B8%88%E8%AF%BE%E4%BB%B6/%E4%B8%80%E9%98%B6%E6%AE%B5%E6%8E%88%E8%AF%BE/%E7%AC%AC%E4%B8%80%E5%91%A8%E5%86%85%E5%AE%B9/day03/%E8%B5%84%E6%96%99/%E7%AC%94%E8%AE%B0/float.jpg) 



*清除浮动可以理解为打破横向排列*。

### 清除浮动的属性是clear，

语法：**clear : none | left | right | both**

#### none

**none：默认值。**允许两边都可以有浮动对象

#### left

**left：清除左浮动**/不允许左边有浮动对象right

#### right

**right  :  清除右浮动**/不允许右边有浮动对象

#### both

**both  :  清除两端浮动**/不允许有浮动对象

有一点是要记住的那就是*

对于CSS的清除浮动(clear)，一定要牢记：这个规则**只能影响使用清除的元素本身，不能影响其他元素**