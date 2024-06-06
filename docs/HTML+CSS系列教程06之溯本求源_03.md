# HTML+CSS系列教程06之溯本求源_03

![幻灯片2](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%872-5eba00.png)

text-shadow文字的阴影

- 阴影的默认的颜色和文字的颜色相同

- - x 左右的偏移 正：右 负：左

  - y 上下的偏移 正：下 负：上

  - blur 模糊程度

  - color 颜色

  - 多阴影 多个阴影

  - - 通过逗号的方式进行分割，可以设置多阴影
    - text-shadow: 10px 10px 7px       blue, -10px -10px 7px green;

  - 效果

    - ![image-20240607005916672](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607005916672-1e42cd.png)

  - 别人做好的火焰效果文字

- ```css
  div{
      font-size:60px; text-shadow:0 0 4px white,0 -5px 4px #ff3,2px -10px 6px #fd3,-2px -15px 11px #f80,2px -25px 18px #f20;
  }
  ```

![幻灯片3](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%873-990040.png)

box-shadow盒子的阴影

- 阴影的默认的颜色是黑色

- - x 左右的偏移 正：右 负：左

  - y 上下的偏移 正：下 负：上

  - blur 模糊程度

  - spread 扩散 其实就是边缘虚化

    - ![image-20240607010013260](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010013260-0c35d1.png)

  - color 颜色

  - inset 设置变成内阴影/不设置就是外阴影，默认外阴影

    - ![image-20240607010031986](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010031986-49a7fe.png)

  - 多阴影 多个阴影

  - - 通过逗号的方式进行分割，可以设置多阴影
    - box-shadow: 10px 10px 10px 5px      blue ,-10px -10px 10px 5px green;
    - ![image-20240607010049114](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010049114-a02d23.png)

![幻灯片4](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%874-c363da.png)

mask遮罩

- 遮罩目前还没有标准化，所以需要加上浏览器前缀

- 在chrome浏览器中没有效果，但是在360极速浏览器中可以生效

  - ![image-20240607010117226](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010117226-53fd76.png)

- 效果

  - ![image-20240607010139054](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010139054-54bac6.png)

- 参数

- - 默认沿着水平和竖直两个方向平铺

  - 设置宽高和距离之间需要使用/进行分隔开

  - - -webkit-mask:       url(./img/love.png) no-repeat 200px 100px / 300px 300px;

  - url

  - repert

  - x 左右的偏移 正：右 负：左

  - y 上下的偏移 正：下 负：上

  - w

  - h

  - 多遮罩 多个遮罩

  - - 通过逗号的方式进行分割，可以设置多遮罩
    - -webkit-mask:       url(./img/love.png) no-repeat 200px 100px / 300px 300px，url(./img/car.png) no-repeat left top / 300px 300px

![幻灯片5](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F幻灯片5-d6c9a5.png)

box-reflect倒影

- -webkit-box-reflect:     right 20px url(./img/love.png); 遮罩的效果

- above、below、left、right 倒影的方向

  - ![image-20240607010220817](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010220817-8d19db.png)

- 距离 两个图之间的间隔

  - ![image-20240607010337528](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010337528-df61dd.png)

- 遮罩 | 渐变

  - ![image-20240607010346866](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010346866-2cb71a.png)
  - 渐变：只是支持对透明度的渐变，不能支持颜色的渐变

  ```css
  .box{width: 300px;height: 300px;-webkit-box-reflect: right 20px linear-gradient(rgba(255,255,255,0),rgba(255,255,255,1));}
  ```

  - ![image-20240607010313723](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010313723-48e3ed.png)

- scale = -1 倒影效果

- - .box{width: 300px;height:      300px;transform: scale(-1);}

![幻灯片6](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%876-7cf03d.png)

模糊和计算

- blur

- - filter:blur(1px)  像素数值越大，越模糊
  - ![image-20240607010416835](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010416835-9a24c5.png)

- calc计算

- - 四则运算
  - calc(100% - 100px)
  - 实现比例值和像素之间的换算

![幻灯片7](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%877-911396.png)

分栏布局

- 属性

- - column-count比column-width的优先级更高，设置了column-count分栏数量按column-count计算，最好只设置其中一个

  - column-count : 分栏的个数

  - column-width : 分栏的宽度

  - - 600的宽，column-width为100，我们能看到5栏，因为栏与栏之间还有距离

  - column-gap : 分栏的间距

  - column-rule : 分栏的边线

  - column-span : 合并分栏

  - - 使用all可以将所有栏合并

- 效果

  - ![image-20240607010500801](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010500801-c3332c.png)
  - ![image-20240607010510595](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010510595-1ca8d5.png)

![幻灯片8](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%878-0ec976.png)

伪类和伪元素

- 在CSS2.1中对伪类和伪元素的区别比较模糊。CSS3中对这两个概念做了相对较清晰地解释，并且在语法上也做了很明显的区分。

- CSS3中规定**伪类由一个冒号开始**，然后为伪类的名称；**伪元素由两个冒泡开始**，然后为伪元素的名称。

- 伪类本质上是为了弥补常规CSS选择器的不足，以便获取到更多信息。通常表示获取不存在与DOM树中的信息，或获取不能被常规CSS选择器获取的信息。

- - 整个的css选择器
  - ![image-20240607010549178](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010549178-419766.png)

- 伪元素本质上是创建了一个有内容的虚拟容器。这个容器不包含任何DOM元素，但是可以包含内容。另外，开发者还可以为伪元素定制样式。

- - 整个的css选择中的元素一部分
  - ![image-20240607010610069](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010610069-51ba3a.png)

![幻灯片9](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%879-d4dcd9.png)

![幻灯片10](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8710-9f39ad.png)

![幻灯片11](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8711-f165ab.png)

CSS Hack

- CSS Hack用来**解决浏览器的兼容性问题**，**为不同版本的浏览器定制编写不同的CSS效果**，使用每个浏览器单独识别的样式代码，控制浏览器的显示样式。

- Hack分类

- - CSS属性前缀法

  - - 在CSS样式属性名前加上一些只有特定浏览器才能识别的hack前缀，以达到预期的页面展现效果
    - IE6     _background:blue;
    - IE6、7  *background:blue; +background:blue;
    - IE6~9  background:blue\9;
    - IE8~11 background:blue\0;

  - 选择器前缀法

  - - 选择器前缀法是针对一些页面表现不一致或者需要特殊对待的浏览器，在CSS选择器前加上一些只有某些特定浏览器才能识别的前缀进行hack。
    - IE6  *html .box{}
    - IE7 *+html .box{}
    - IE9及高级浏览器  :root .box{}

  - IE条件注释法

  - - 是IE浏览器专有的Hack方式，微软官方推荐使用的hack方式。
    - 在htm的代码中以代码注释的方式，完成指定的IE版本指定

```css
<!--[if gte IE 7]>
<div class="box"></div>
<![endif]-->
```

![幻灯片12](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8712-bb4476.png)

![幻灯片13](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8713-5e580c.png)

![幻灯片14](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8714-6bd866.png)

![幻灯片15](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8715-f105e6.png)

IE低版本常见BUG

- 常见兼容问题

- - 透明度

  - - opacity IE8及以下版本不识别

    - 解决办法

    - - .box{ width:100px;        height:100px; background:red; opacity:0.5; filter:alpha(opacity=50);}

  - 双边距

  - - IE6下的双边距BUG

    - 解决办法

    - - .box{ float:left;        width:100px; height:100px; background:red; margin-left: 50px;        _display:inline;}

  - 最小高度

  - - IE6下的最小高度BUG , 最小高为19px

    - 解决办法

    - - .box{ width:300px;        height:3px; background:red; overflow: hidden;}

  - 图片边框

  - - IE9及低级浏览器图片边框

    - 解决办法

    - - img{ border:none;}

![幻灯片16](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8716-af6d95.png)

渐进增强和优雅降级

![image-20240607010840269](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010840269-ab00bc.png)

![幻灯片17](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8717-996422.png)

网页布局

- 等高布局

- - 当左右两测的浮动元素高度不一致的时候，会统一成等高的元素

  - 实际上我们是利用了margin-bottom和padding-bottom来控制模型的父区域的底边的位置

  - - 假设我们的margin-bottom是正值，父元素底边会在下面出现，加入我们的margin-bottom是负值，元素会向上移动，这个时候父元素的底边也会向上移动，当我们设置margin-bottom的负值超出父元素的高度，父元素回闭合，三种情况如图所示
      - ![image-20240607010926830](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010926830-e7d876.png)
      - ![image-20240607010936566](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010936566-36ca77.png)
      - ![image-20240607010946119](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607010946119-8252da.png)
    - 然后我们可以设置margin-bottom是一个很大的负值，padding-bottom是一个margin-bottom数值的绝对值，这样可以实现对冲，子元素区域很大，但是父元素并没有被撑开，当里面添加元素的时候，父元素因为里面有了高度，会被拉伸一定的高度，而对于的部分我们设置overflow：hidden隐藏掉就行了
      - ![image-20240607011016064](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011016064-604d6e.png)
      - ![image-20240607011026535](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011026535-5943ae.png)
    - 结果展示
      - ![image-20240607011044193](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011044193-b137cd.png)
      - ![image-20240607011057921](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011057921-66378c.png)
      - ![image-20240607011107657](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011107657-f6bb39.png)
    - 最终效果展示
      - ![image-20240607011124979](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011124979-2b7465.png)

- 双飞翼布局

- - 左边固定，右边固定，中间自适应

  - 方案

  - - BFC方式

    - 定位

    - 浮动(双飞翼布局)

    - - margin负值实现
      - 先写中间部分；然后让三元素都浮动，最后通过内容部分通过增加margin的方式实现中间定位
      - 第二层的浮动元素可以上到上一层浮动元素中：**margin****-left:-100%**

  - - **结果**
      - ![image-20240607011208015](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011208015-089335.png)

- 圣杯布局

- - 浮动(圣杯布局)

  - 效果和双飞翼布局是一样的，但是在布局的时候样式结构略有不同

  - - 不同1：不需要在content内部在设置标签，进行样式设置
    - 不同2：最后我们的left和right是通过相对定位的方式挂载，确定最终位置(对于left和right的结构略显复杂)