# HTML+CSS系列教程04之溯本求源_01

![幻灯片3](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%873-f44ef2.png)

![幻灯片4](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%874-6b2774.png)

![幻灯片5](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%875-bf82b6.png)

HTML和XHTML的区别？

- XHTML的教学官网：https://www.w3school.com.cn/xhtml/index.asp
- DOCTYPE文档和编码

```html
<!-- html -->
<!DOCTYPE html>

<!-- xhtml -->
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="zh-CN">
```

- 元素的大小写

- - html:标签的大小写都行
  - xhtml：只能写小写的标签名

- 属性布尔值

- - html:      checked="checked"       ===>简化 checked
  - xhtml：      checked="checked"       ===>不能简化 

- 属性引号

- - html:      title="hello"  ===      title=hello
  - xhtml：      title="hello"  ===>不能省略引号

- 图片的alt属性

- - html:<img src="">
  - xhtml:<img      src="" alt="" / > alt不能省略

- 单标签的写法

- - html:<input type="text">
  - xhtml:<input type="text" / >

- 双标签的闭合

- - html:双标签写一半，浏览器自动识别补全，并不会产生错误
  - xhtml:双标签写一半,程序产生错误

![幻灯片6](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%876-966a0e.png)

strong和b、em和I

- 表现形式都是**文本加粗**和*文本斜体*

- 其实展现的形式都是相同的，但是strong 和 em     是具备语义化的，而 b 和 i 是不具备语义化的

- 应用场景

- - span的内联元素，简化了css选择器的使用

![幻灯片7](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%877-dec2d9.png)

引用标签

1. blockquote :      引用大段的段落解释
2. q :      引用小段的短语解释
3. abbr :      缩写或首字母缩略词
4. address :      引用文档地址信息
5. cite :      引用著作的标题

- 使用的目的：是方便浏览器的解析，让搜索引擎更方便的搜索到想要的信息内容，规范我们的代码规范程度
- abbr的展示
  - ![image-20240606233303743](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606233303743-daed14.png)

![幻灯片8](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%878-ab6820.png)

iframe嵌套页面

- 可以引入其他的html网页到当前的html中进行展示，通过属性来实现

- 应用场景：

- - 钓鱼网站(网址识别)

  - 数据传输

  - 共享代码

  - - 页面大部分都是相同的，部分修改-->直接嵌入

  - 局部刷新

  - 第三方广告介入

![幻灯片9](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%879-7d8bdb.png)

br和wbr

- br 标签表示换行操作

- wbr 标签表示软换行操作

- - 如果单词太长，或者您担心浏览器会在错误的位置换行，那么您可以使用 wbr       元素来添加 Word Break Opportunity（单词换行时机）
  - 软换行的实质：当一行中的空余空间不足以支撑单词的长度单词会将<wbr>后面的一部分先换到下一行显示      不是强制一个单词作为整体下调到下一行

![幻灯片10](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8710-01e25c.png)

pre 与 code

**实际上一个是代码的标签，一个是展示的，两者结合展示代码**

- pre 元素可定义预格式化的文本。被包围在 pre 元素中的文本通常会保留空格和换行符。

- code

- - 只应该在表示计算机程序源代码或者其他机器可以阅读的文本内容上使用      code 标签。虽然 code 标签通常只是把文本变成等宽字体，但它暗示着这段文本是源程序代码。

- pre和code的配合可以在网页上展示源代码

  - ![image-20240606233401539](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606233401539-fe5681.png)
  - ![image-20240606233409772](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606233409772-9ee1d3.png)

- 简单获取源代码的方法，我们可以使用md语法，生成的html语法其实在网页中已经完成了转义，直接从网页中拷贝出来即可复制到我们的代码中就行了

![幻灯片11](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8711-b8a1ac.png)

map和area

给特殊图形添加链接，area能添加的热区的形状：矩形，圆形，多边形

- map定义一个客户端**图像映射**。图像映射（image-map）指带有可点击区域的一幅图像。**area     元素永远嵌套在 map 元素内部**。**area 元素可定义图像映射中的区域**。
- area 元素的href属性定义区域的URL，shape属性来定义区域的形状，coords属性定义热区的坐标。
- ![image-20240606233445799](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606233445799-0fbccf.png)

![幻灯片12](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8712-5f53b0.png)

embed与object

- embed和object都表示能够**嵌入一些多媒体**，如flash动画、插件等。基本使用没有太多区别，主要是为了兼容不同的浏览器而已.
- object 元素需要配合param 元素一起完成。

![幻灯片13](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8713-110f7a.png)

audio和video

- 引入音频和视频的标签，属于h5的新功能

- controls用于显示控件 loop当音频播放结束了从头开始播放，循环 autoplay 自动播放

- 多浏览器兼容问题/使用source对资源进行排版，先找第一个看一下浏览器是不是支持，不支持在浏览器中加载第二个，看支不支持，依此下推，最终都不支持，就不支持，如支持，资源加载进入浏览器即可

- - 代码

  - ```html
    <video controls>
        <source src="./ziyuan/Intermission-Walk-in.ogv"></source>
        <source src="./ziyuan/Intermission-Walk-in_512kb.mp4"></source>
    </video>
    ```

![幻灯片14](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8714-ce0c9b.png)

文字注解与文字方向

- ruby 标签定义 ruby 注释（中文注音或字符），rt     标签定义字符（中文注音或字符）的解释或发音。

- - 展示
  - ![image-20240606233626003](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606233626003-8ce749.png)

- 改变文字的方向
  - ![image-20240606233636082](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606233636082-0396c0.png)
  - ltr----left to right     从左到右
  - rtl----right to left 从右到左
- CSS的实现方式

```html
<style>
    span{direction: rtl;unicode-bidi: bidi-override;}
</style>
<span>爱神的剑我们都是好孩纸</span>
```

![幻灯片15](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8715-95e8af.png)

扩展link标签

- 引入CSS

- - `<link rel="stylesheet" type="text/css" href="theme.css">`

- head部分的图标的引入

- - `<link rel="icon" type="/image/x-icon" href="http://www.mobiletrain.org/favicon.ico">`
  - ![image-20240606233812329](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606233812329-b83cc7.png)

- dns的解析过程

- - `<link rel="dns-prefetch" href="//static.360buyimg.com"> `
  - 相当于提前将域名进行解析成IP,速度的提升
  - ![image-20240606233804862](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606233804862-eb6158.png)

![幻灯片16](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8716-266634.png)

meta扩展学习

- 描述信息，有利于搜索引擎的加载

- - `<meta name="description" content="大连美团网精选大连美食餐厅,酒店预订,电影票,旅游景点,外卖订餐,大连团购信息,您可查询商家评价店铺信息。大连生活,下载美团官方APP,吃喝玩乐1折起。">`
  - ![image-20240607014731292](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014731292-ae6f01.png)

- 浏览器内核渲染相关

- - `<meta name="renderer" content="webkit">`
  - ![image-20240607014802200](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014802200-da3ae4.png)

- `<meta http-equiv="X-UA-Compatible" content="ie=edge"> `

  - 针对ie的浏览器使用最高版本进行渲染
  - ![image-20240607014837230](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014837230-28a4d9.png)

- `<meta http-equiv="refresh" content="3" url="">`

- - 网址三秒后自动刷新，跳转到url指定的地址，但是演示的时候没有效果

- 在规定的时间内，有缓存使用缓存

- - `<meta http-equiv="expires" content="Wed, 20 Jun 2019 22:33:00 GMT">`

![幻灯片17](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8717-252ef4.png)

![幻灯片18](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8718-63a51f.png)

![幻灯片19](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8719-066bcd.png)

HTML新的语义化标签

下面的标签在一个网页中都是唯一的，只能出现一次

- header:页眉

  - ![image-20240607014102724](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014102724-b2ba8a.png)

- footer :页脚

  - ![image-20240607014119901](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014119901-c5920b.png)

- main:主体

  - ![image-20240607014139181](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014139181-ceed3b.png)

- hgroup:标题组合

  - ![image-20240607014209924](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014209924-810ffc.png)

- nav:导航

  - ![image-20240607014204643](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014204643-de6cbe.png)

- article:独立的内容

  - ![image-20240607014230844](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014230844-d2cbe7.png)

- aside:辅助信息的内容

  - ![image-20240607014250079](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014250079-3fa2f1.png)

- section:区域

- - 和article的区别：article是独立的部分，section是用来划分区域的

  - - 列表中很多的li都是一个一个的区域section，组合成的独立的部分就是article

- 视频和图像

- - figure:描述图像或视频
  - figcaption:描述图像或视频的标题部分
    - ![image-20240607014315311](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014315311-1d4984.png)

- datalist:选项列表

  - ![image-20240607014341732](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014341732-6c2b07.png)
  - 带有筛选功能
    - ![image-20240607014359079](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014359079-8b892e.png)

- details / summary :文档细节 / 文档标题

  - ![image-20240607014426478](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014426478-80fdd9.png)
  - ![image-20240607014434253](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014434253-d48d10.png)

- progress / meter:定义进度条 / 定义度量范围

  - progress

    - ![image-20240607014500808](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014500808-49fc11.png)

  - meter

    - ![image-20240607014517752](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014517752-6d8beb.png)

    - 颜色变化

    - - low/height
      - ![image-20240607014535530](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014535530-1a8c5e.png)

- time:定义日期或时间

- mark:带有记号的文本

  - ![image-20240607014604426](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014604426-3d744e.png)

![幻灯片20](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8720-d1f711.png)

表格扩展

- 添加单线:border-collapse : collapse

  - ![image-20240607013845164](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013845164-9ec2a9.png)

- 隐藏空单元:empty-cells : **hide**

  - ![image-20240607013907476](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013907476-9635b3.png)

- 斜线分类:border  /      rotate

- - 这个代码

  - ```css
    /* 实现斜线分割单元格 */
    table .line{border-top: 50px solid red;border-left: 150px solid blue;position: relative;color: white;}
    table .line em{position:absolute;left: -50px;top:-50px;}
    table .line span{position:absolute;left: -120px;top:-30px;}
    ```

  - 这个再调整

  - ![image-20240607013953153](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013953153-ff1975.png)

- 列分组:colgroup / col
  - ![image-20240607014013283](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607014013283-52e97e.png)

![幻灯片21](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8721-75325e.png)

![幻灯片22](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8722-4a5c34.png)

![幻灯片23](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8723-bc4c2a.png)

![幻灯片24](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8724-5fb13f.png)

表单的扩展

- 使用label的方式进行优化

- - 美化复选框

  - ```css
    label input{display: none;}
    label input:checked+div{background-position: 0 0;}
    label div{width: 28px;height: 28px;background: url(./ziyuan/checkbox.png) no-repeat 0 -28px;}
    ```

  - 美化上传按钮

  - ```css
    label input{display: none;}
    label div{width: 86px;height: 34px;;background: url(./ziyuan/upload.png) no-repeat 0 0;}
    ```

- 使用透明度和定位优化

  - ![image-20240607013028022](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013028022-bf5625.png)

  - ```css
    .upload{width: 86px;height: 34px;position: relative;}
    .upload input{width: 100%;height: 100%;position: absolute;left: 0;top:0;opacity: 0;}
    .upload div{width: 100%;height: 100%;background: url(./ziyuan/upload.png);}
    ```

- email : 电子邮件地址输入框

  - ![image-20240607013113893](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013113893-0864f8.png)

- url : 网址输入框

  - ![image-20240607013132442](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013132442-287c90.png)

- number : 数值输入框

  - ![image-20240607013214612](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013214612-99b4ca.png)
  - ![image-20240607013223144](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013223144-989aed.png)

- range :      滑动条

  - ![image-20240607013241376](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013241376-746ef8.png)

  - 控制最小值/最大值/当前值

  - ```css
    <input type="range" min="0" max="20" value="17">
    ```

- date / month / week : 日期控件 

  - ![image-20240607013318959](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013318959-f18728.png)
  - ![image-20240607013327753](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013327753-263474.png)
  - ![image-20240607013335645](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013335645-2b228a.png)

- search : 搜索框

  - ![image-20240607013352489](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013352489-8d7755.png)

- color :      颜色控件

  - ![image-20240607013410108](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013410108-79ef94.png)

- tel : 电话号码输入框

  - 在web端和text是没有区别的，但是到了手机端，会出现数字键盘

- time : 时间控件

  - ![image-20240607013442017](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013442017-aeec42.png)

- 新表单属性

- - autocomplete :       自动完成(默认on/off)

  - - 默认的输入框是记录之前输入过的值的
      - ![image-20240607013513144](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013513144-801377.png)
    - 使用autocomplete=off 清理曾经输入过的信息
      - ![image-20240607013529916](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013529916-08abb6.png)

- - autofocus :      获取焦点

  - - 光标自动在输入框中
      - ![image-20240607013552620](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013552620-a44434.png)

- - required :      不能为空
    - ![image-20240607013614114](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013614114-9b2deb.png)
  - pattern : 正则验证
    - ![image-20240607013630891](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013630891-beabde.png)

- 数据传输

- - method :       数据传输方式

  - - get

      - ![image-20240607013652356](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013652356-6ddf2d.png)

    - post

    - - formdata的形式存在

- - enctype :      数据传输类型

  - - 设置传输类型的
    - enctype="application/x-www-form-urlencoded" **默认**

  - - enctype="multipart/form-data" 文件/二进制数据流

  - name / value :      数据的键值对

- 扩展标签    

- - fieldset :       表单内元素分组 

  - - legend :        为fieldset元素定义标题
    - 配合使用效果
      - ![image-20240607013742221](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013742221-01f783.png)

- - optgroup : 定义选项组
    - ![image-20240607013806968](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607013806968-dd6db0.png)

![幻灯片25](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8725-1acc96.png)

![幻灯片26](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8726-9be99a.png)

![幻灯片27](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8727-aa7837.png)

BFC规范：

- 存在原因

- - 因为我们在使用块做元素的布局的时候，总是出现一些奇奇怪怪的问题，BFC规范其实就是帮助我们解决这样的莫名的错误
  - 触发BFC规范的元素，可以形成一个独立的容器，不受到外界的影响，从而解决一些布局的问题

- **触发条件**

- - 直接设置下面的值就行(但是有些会因为效果会出现偏差，理解使用)

  - - 浮动元素：float 除 none 以外的值
    - 绝对定位元素：position       (absolute、fixed) 
    - display 为       inline-block、table-cells、flex
    - overflow 除了 visible 以外的值       (hidden、auto、scroll)

- 解决的问题：

- - margin叠加问题

  - - 没有BFC的时候，我们仅仅为上下元素中的一个设置足够大的margin即可，另开一个不进行设置

  - margin的传递问题

  - - 没有BFC的时候，我们对其父元素设置overflow:hidden 消除传递问题

    - - 实际上上面我们对overflow:hidden的设置就是使父容器触发BFC规范，变成一个独立的盒子

  - 浮动问题

  - - 没有BFC的时候，使用的是给父元素增加一个after伪类的方式

    - - .clear::after{content:        "";display: block;clear: both;}

    - 使用BFC,直接在父元素上套上overflow:hidden 触发BFC,在父元素有高度的时候，可能出现影响布局的情况，我们可以将height变成min-height

  - 解决覆盖的问题overflow

  - - hidden,scroll,auto等

- 解决margin叠加问题的代码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box1{width: 100px;height: 100px;margin-bottom: 30px;background-color: black;}
        .box2{width: 200px;height: 200px;margin-top: 30px;background-color: red;}

        /* 触发BFC条件，变成一个独立的容器 */
        .box{overflow: hidden;}
    </style>
</head>
<body>
    <!-- BFC规范解决margin叠加的问题 -->
    <div class="box">
        <div class="box1"></div>
    </div>
    
    <div class="box"> 
        <div class="box2"></div>
    </div>
</body>
</html>

```

