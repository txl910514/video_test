# video_test
video_test
### http://www.jq22.com/jquery-info404
### https://kanoha.org/categories/opensource-projects/
### https://github.com/jabbany/ABPlayerHTML5
### https://github.com/videojs/videojs-youtube
### http://docs.videojs.com/docs/guides/options.html

## 选项

### 设置选项
* 该的Video.js嵌入代码是一个简单的HTML5视频标签，因此对于很多的选项，你可以使用标准的标签属性来设置选项。
    <video controls autoplay preload="auto" ...>
* 另外，您也可以使用数据设置属性提供的选项JSON格式。这也是你将如何设置是不标准的视频标签选项。
    <video data-setup='{ "controls": true, "autoplay": false, "preload": "auto" }'...>
* 最后，如果你不使用的数据设置属性触发播放器的设置，你可以与球员选项中的JavaScript功能设置第二个参数传递一个对象。
    videojs("example_video_1", { "controls": true, "autoplay": false, "preload": "auto" });

## 个人选项
### 注意在视频标签属性
* 随着HTML5视频标签的属性只能是真或假（布尔），您只需包含属性（没有等号），将其打开，或排除将其关闭。例如，要打开的控制上：
* 错误
    <video controls="true" ...>
* 对
    <video controls ...>
* 最大的问题的人碰上正试图将这些值设置为false，利用虚假的值（例如控制=“假”），这实际上刚好相反，并将其值设置为true，因为属性仍包含。如果你需要的属
性，包括XHTML验证一个等号，你可以将属性的值设置为与它的名字（例如控制=“控制”）。

### 控制
* 对照选项设置玩家是否具有用户可以与之交互的控制。如果不控制，启动视频播放的唯一方法是使用自动播放属性或通过API。
    <video controls ...>
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

  “auto”：立即开始加载视频（如果浏览器同意）。像iPhone和iPad某些移动设备将不能以保护其用户的带宽预先加载视频。这就是为什么值被称为“自动”，而不是更
  多的东西最终像“真”。

  “metadata”：只载入视频的元数据，其中包括像的持续时间和视频的尺寸信息。

  “none”：未预装任何视频数据。这将等待，直到用户点击播放开始下载。
    <video preload ...>
    or
    { "preload": "auto" }

### 海报
* 海报属性设置显示视频开始播放前的图像。这通常是视频或自定义标题画面的帧。一旦用户点击播放图像将消失。
    <video poster="myPoster.jpg" ...>
    or
    { "poster": "myPoster.jpg" }

### 循环
* loop属性使视频，因为它结束后立即开始。这可用于如云的背景的视觉效果。
    <video loop ...>
    or
    { "loop": true }

### 宽度
* width属性设置视频的显示宽度。
    <video width="640" ...>
    or
    { "width": 640 }

### 高度
* height属性设置视频的显示高度。
    <video height="480" ...>
    or
    { "height": 480 }

### 组件选项
* 您可以为任何一个播放器组件的选项。举例来说，如果你想删除的muteToggle按钮，这是一个孩子controlBar，你可以设置该组件为false：
    var player = videojs('video-id', {
        controlBar: {
            muteToggle: false
        }
    });
* 这也适用于使用了data-setup视频元素的属性，只记得选择需要使用适当的JSON符号。
    <video ... data-setup='{ "controlBar": { "muteToggle": false } }'></video>

