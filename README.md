# video_test
video_test
### http://www.jq22.com/jquery-info404
### https://kanoha.org/categories/opensource-projects/
### https://github.com/jabbany/ABPlayerHTML5
### https://github.com/videojs/videojs-youtube
### http://docs.videojs.com/docs/guides/options.html

## 选项

### 控制
* 对照选项设置玩家是否具有用户可以与之交互的控制。如果不控制，启动视频播放的唯一方法是使用自动播放属性或通过API。
* <video controls ...>
  or
  { "controls": true }

### 自动播放
* 如果自动播放为true，视频将尽快开始加载页面时播放（无需用户进行任何交互）。不支持的Apple iOS设备。苹果块，以保护它的客户从使用不情愿很多自己（往
往是昂贵的）的每月数据计划努力的自动播放功能。用户触摸/点击才能启动视频在这种情况下
* <video autoplay ...>
  or
  { "autoplay": true }

### 预紧(缓存)
* 预紧属性通知浏览器中的视频数据是否应该开始尽快视频代码被加载下载。选项有自动，元数据，并且没有。

  “自动”：立即开始加载视频（如果浏览器同意）。像iPhone和iPad某些移动设备将不能以保护其用户的带宽预先加载视频。这就是为什么值被称为“自动”，而不是更
  多的东西最终像“真”。

  “元数据”：只载入视频的元数据，其中包括像的持续时间和视频的尺寸信息。

  “无”：未预装任何视频数据。这将等待，直到用户点击播放开始下载。


