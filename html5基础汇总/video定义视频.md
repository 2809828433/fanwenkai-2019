# video定义视频

```html
 <video src="movie.ogg" controls>Video元素</video> 
```

### 属性

  controls属性：如果出现该属性，则向用户显示控件，比如播放按钮。

  autoplay属性：如果出现该属性，则视频在就绪后马上播放。

  loop属性：重复播放属性。

  muted属性：静音属性。

  preload属性：页面加载时进行加载，并预备播放

  auto - 当页面加载后载入整个视频(全部预加载)

  metadata - 当页面加载后只载入元数据(部分预加载,（包括尺寸，第一帧，持续时间等等）

  none - 当页面加载后不载入视频(页面制作者认为用户不期望此视频，或者减少HTTP请求)

  poster属性：规定视频正在下载时显示的图像，直到用户点击播放按钮。

```html
<source   src=”路径”  type=”video/视频格式”> 标签为媒介元素（比如 <video> 和 <audio>）定义媒介资源。
Type属性值：
  用于视频：video/ogg   video/mp4     video/webm
```

### 代码举例



```html
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>Index</title>
</head>
<body>
	<!-- 多媒体标签 -->
	<video controls autoplay loop muted>
		<!-- autoplay自动播放过程中需要配置muted属性 -->
		<source src="视频/3theB.mp4" type="video/mp4">
	</video>
	<audio  controls autoplay muted>
		<source src="视频/蔡健雅 - 被驯服的象.mp3" type="audio/mp3">
	</audio>
</body>
</html>
```

# audio定义音频（行内块元素）

```html
<audio src="">Audio元素</audio>
<source   src=”路径”  type=”video/视频格式”> 标签为媒介元素（比如 <video> 和 <audio>）定义媒介资源。
<source   src=”路径”  type=”audio/音频格式”>
Type属性值：
	用于音频：audio/ogg   audio/mpeg  (mp3)   wav
```

### 属性

  controls属性：如果出现该属性，则向用户显示控件，比如播放按钮。

  autoplay属性：如果出现该属性，则视频在就绪后马上播放。

  loop属性：重复播放属性。

  muted属性：静音属性。

### 兼容性

视频支持的格式 

![1553689830160](C:\Users\ADMINI~1\AppData\Local\Temp\1553689830160.png)

音频支持的格式

![1553689875631](C:\Users\ADMINI~1\AppData\Local\Temp\1553689875631.png)

