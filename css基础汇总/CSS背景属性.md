# CSS背景属性

## 背景颜色

{**background-color**:颜色值;}

## 背景图片的设置

 **background-image**：url(背景图片的路径及全称）；

## 背景图片平铺属

{**background-repeat**:no-repeat不平铺/repeat平铺/repeat-x  X轴平铺/repeat-y   Y轴平铺 }

## 背景图的位置

**{background-position:left/center/right/数值      top/center/bottom/数值;}**

### 水平方向上的对齐方式

**（left/center/right）或值** 

### 垂直方向上的对齐方式

**(top/center/bottom)或值** 

### background-position:值1 值2;

两个值 ：第一个值表示水平位置的值，第二个值：表示垂直的位置。 
当两个值都是center的时候写一个值就可以代表的是水平位置和垂直位置 ；

当元素小背景图大的时候，想显示右下方的背景图，通过负值来调整背景图的位置；

## 背景图的固定

### background-attachmen

{background-attachment:fixed固定/scroll滚动;}

### fixed

fixed 固定，不随内容一块滚动，根据可视窗口固定位置；

### scroll

scroll:随内容一块滚动。

#### *网页上常用的图片格式*

1）**jpg** :有损压缩格式，靠损失图片本身的质量来减小图片的体积，适用于颜色丰富的图像;(像素点组成的，像素点越多会越清晰 )
2）**gif**：无损压缩格式，支持透明，支持动画，适用于颜色数量较少的图像;
3）**png**:无损压缩格式，支持透明，不支持动画，(是fireworks的 源文件格式)，适用于颜色数量较少的图像; 