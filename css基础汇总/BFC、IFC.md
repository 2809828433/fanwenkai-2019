## 1、BFC

**BFC（block formating context ）：块级格式化上下文    bfc内部竖直排列  ** 

### 渲染规则

> - 内部的box会在垂直方向，一个接一个的放置
> - box垂直方向的距离由margin决定，属于同一个bfc的两个相邻box的margin会发生重叠
> - 每个元素的margin box的左边，与包含块border box的左边相接触（对于从左往右的格式化，否则相反）
> - bfc的区域不会与float box重叠
> - bfc就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素。反之也是如此
> - 计算bfc的高度时，浮动的元素也参与计算

### 生成bfc空间

> - 根元素 html是一个bfc（上下文，容器） 
> - float属性不为none（脱离文档流）
> - position为absolute或fixed
> - display为inline-block,table-cell,table-caption,flex,inine-flex
> - overflow不为visible

## 2、IFC(拓展)

**IFC：行内格式化上下文    ifc内部水平排列**   

> - ifc高度为最高的内容的高度，宽度为内容的宽度
> - 水平排列
> - 水平方向的margin，border，padding有效，竖直方向的margin，padding，border只有显示效果
> - text-align属性可以控制ifc中元素的对齐方式
> - inline-block垂直方向可以用vertical-align来调整对齐方式



- 