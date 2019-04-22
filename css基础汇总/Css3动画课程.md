# Css3动画课程

## Transition过渡效果

**兼容性**

主流浏览器都支持：`ie10`、`谷歌`、`欧朋`、`火狐`、`safair`，*ie10以下不能用*

**相关属性**

### transition简写属性

#### 1、transition-property：规定用于参与css过渡的具体属性

> ​        transition-property 设置的是具体属性，如果没有在本条属性中设置某个属性参与过渡，那么没有参与的属性就不会具有过渡效果。
>
> > > ​	如果没有设置transition-property 属性，那么标签的所有属性默认都会参与到过渡效果中来。
> > >
> > > ​	如果在设置transition-property属性的时候，想要让所有的属性都参与过渡，可以设置为all。
> > >
> > > ​	如果在设置的时候，不想让任何属性参与进过渡效果，但是还必须设置这个属性，那么就可以将属性值设置为none。

​	**语法**：

​	transition-property:none    没有过渡效果；

​	transition-property:all   全部属性参与过渡；

​	transition-property:property  具体属性值， 每个属性值之间用逗号分隔。

**示例**	

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        p {
            width: 100px;
            height: 100px;
            background-color: lightseagreen;
            transition-property: all;
            transition-duration: 1s;
        }
        p:hover {
            width: 3000px;
            height: 4000px;
            background-color: pink;
        }
    </style>
</head>
<body>
    <p>

    </p>
</body>
</html>
```



#### 2、transition-duration ：过渡时间/过渡需要使用的具体时间 秒|毫秒  s||ms



#### 3、transition-timing-function:规定过渡效果的时间曲线

- cubic-bezier 后面设置的是具体的贝塞尔曲线的值

- linear： 规定以相同的速度从开始到结束 (等于 cubic-bezier(0,0,1,1)) --匀速

- ease*默认值*  ：规定慢速开始，然后加快，最后慢速结束（cubic-bezier(0.25,0.1,0.25,1)）

- ease-in ： 规定以慢速开始的过渡效果（等于 cubic-bezier(0.42,0,1,1)） -- 加速

- ease-out ：慢速结束过渡效果 等于 cubic-bezier(0,0,0.58,1)  -- 减速

- ease-in-out  规定以慢速开始和结束的过渡效果（等于 cubic-bezier(0.42,0,0.58,1)）

  **示例**

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <style>
          p {
              width: 100px;
              height: 100px;
              background-color: lightseagreen;
              transition-property: all;
              transition-duration: 10s;
              /*transition-timing-function: cubic-bezier(.17,.67,.87,.11);*/
              /*transition-timing-function: linear;*/
              /*transition-timing-function: ease;*/
              transition-timing-function: ease-in;
          }
          p:hover {
              width: 300px;
              height: 400px;
              background-color: pink;
          }
      </style>
  </head>
  <body>
      <p>
          
      </p>
  </body>
  </html>
  ```



#### 4、transition-delay  延迟  单位:s|ms

​	**作用:在指定的时间之后再来执行变化效果。**

​	在实际设置延迟的时候，也可以给具体的某个属性设置延迟。

​	**示例**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        p {
            width: 100px;
            height: 100px;
            background-color: lightpink;
            transition:1s width 2s,2s height ,3s background-color;
        }
        p:hover {
            width: 300px;
            height: 300px;
            background-color: red;
        }
    </style>
</head>
<body>
    <p>

    </p>
</body>
</html>
```



#### 5、简写  transition: property duration timing-function delay;

```
> 如果使用简写的话，不去设置的具体属性都会采用默认值的形式。
```

过渡示例:

**手风琴**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>手风琴</title>
    <style>
        body {
            margin:0;
            padding:0;
            background-color: #f7f7f7;
        }
        h3 {
            margin:0;
            padding:0;
        }
        .box {
            width: 500px;
            margin:0 auto;
        }

        .list h3 {
            height: 35px;
            line-height:35px;
            padding-left: 30px;
            border-bottom:2px solid #690;
            font-size:14px;
            color: #fff;
            background-color: #369;
            transition: all 0.3s ease 0s;
        }
        .list .pictxt {
            height: 0;
            background-color: lightblue;
            transition: all 0.3s ease 0s;
        }
        .list:hover  h3 {
            background-color: #036;
        }
        .list:hover .pictxt{
            height: 150px;
        }
    </style>
</head>
<body>
    <div class="box">
        <div class="list">
            <h3>今日新闻</h3>
            <div class="pictxt"></div>
        </div>
        <div class="list">
            <h3>昨日新闻</h3>
            <div class="pictxt"></div>
        </div>
        <div class="list">
            <h3>前日新闻</h3>
            <div class="pictxt"></div>
        </div>
        <div class="list">
            <h3>去年新闻</h3>
            <div class="pictxt"></div>
        </div>
    </div>
</body>
</html>
```

