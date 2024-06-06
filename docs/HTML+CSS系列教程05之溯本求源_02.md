# HTML+CSS系列教程05之溯本求源_02

![幻灯片2](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%872-82153b.png)

浏览器前缀(了解即可)

- CSS3去兼容不同的浏览器，针对旧的浏览器去做兼容，新的浏览器基本不需要添加前缀

- 假设添加了-webkit-的前缀，所使用的效果只会在对应的浏览器上生效

- 前缀可能针对的是浏览器中的某些版本的小版本，而不是大的版本

- - -ms-针对的是IE-10的版本起作用，但是到了IE-9中就没有效果

![幻灯片3](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%873-12f426.png)

![幻灯片4](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%874-abdcd3.png)

transition过渡

- transition 是下面四种写法的复合写法

- - transition-property :       规定设置过渡效果的CSS属性的名称。

  - transition-duration :       规定完成过渡效果需要多少秒或毫秒。

  - transition-delay :       定义过渡效果何时开始。

  - transition-timing-function :       规定速度效果的速度曲线。

  - transition-timing-function

  - - linear  匀速

    - ease（默认值） 先快后慢 缓冲效果

    - ease-in    越来越快

    - ease-out  越来越慢

    - ease-in-out  先加速再减速

    - ![image-20240607012719990](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607012719990-d13416.png)

    - cubic-bezier 四个参数 模拟任何曲线变化

    - - (http://cubic-bezier.com) 现在网站上模拟好，直接带回参数即可
      - ![image-20240607012710826](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607012710826-1f608b.png)

  - transition的集合写法：1s 2s linear

  - - 1s-duration
    - 2s- delay
    - linear-transition-timing-function

- - 不能放在hover上

![幻灯片5](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%875-d79dda.png)

transform变形

- translate  位移  

- - transform:translate(100px,0)
  - 第一个数代表左右(正右负左)，第二个数代表上下(正下负上)
  - translateX 针对X轴位移 translateY 针对y轴位移
  - translateZ 针对z轴位移(3D见效果)

- scale 缩放 （比例值，正常的就是1）

- - 会以中心点完成缩放
  - scale第一个值 针对宽缩放 scale第二个值 针对高缩放
  - 第一个值=第二个值 简写transform:      scale(2) 
  - transform:      scale(2,0.5) 宽变成2倍，长变成一半
  - scaleX 针对宽缩放 scaleY       针对高缩放

- rotate 旋转 (旋转的值，单位是角度 deg/弧度)

- - rotateX（3D）
  - rotateY (3D)
  - rotateZ 平面旋转
  - 旋转默认就是 rotateZ 后面的值是**正值:顺时针** 后面的值是**负值:逆时针**
  - transform: rotateZ(45deg);

- skew 斜切

- - 单位也是角度，正值向左倾斜，负值向右倾斜

  - - transform: skew(45deg);
    - ![image-20240607012404049](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607012404049-34de60.png)

- - skewX 等价于skew

  - skewY

  - - transform: skew(-30deg,-30deg);
    - ![image-20240607012428380](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607012428380-b4487b.png)

- 复合写法和练习

- - 注意事项

  - - 变形操作不会影响到其他的元素

    - 变形只能添加给块元素

    - 旋转的基点transform-origin，默认都是中心点，可以修改

    - ```css
      .box1{width: 100px;height: 100px;background-color: red;transform-origin: 100px 100px;transition: 2s;}
      /* 改变形变的基点 */
      .box1:hover{transform: rotate(180deg);}
      ```

    - 复合写法，可以同时添加多个变形的操作

    - - 执行是有顺序的，先执行后面的操作，后执行前面的操作

      - - transform: translate(100px,0)       scale(0.5);
        - transform: scale(0.5)       translate(100px,0);
        - ![image-20240607012516007](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607012516007-ca39d2.png)

    - **作图理解过程**

      - ![image-20240607012544718](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607012544718-815b48.png)
      - 结果和分析的是一样的
        - ![image-20240607012605732](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607012605732-4014de.png)

![幻灯片6](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%876-1094e6.png)

![幻灯片7](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%877-fea8ae.png)

animation动画：

- **animation-name** : 设置动画的名字 (自定义的)

- - 名字(自由起名)需要和@keyframes进行对应

- **animation-duration** : 动画的持续时间

- **animation-delay** : 动画的延迟时间

- - 延迟的时间，可以为负，负数其实也是再运动，然后起始能看见的位置就是延迟了时间的位置

- **animation-iteration-count** : 动画的重复次数 ，默认值就是1 ，infinite无限次数

- **animation-timing-function** : 动画的运动形式

- 综合设置

- - animation: myBox 4s 2s infinite      linear;
  - 顺序：名字，持续时间，延迟时间，重复次数，运动形式

- **an****imation-fill-mode** :     规定动画播放之前或之后，其动画效果是否可见。

- - none (默认值) :      在运动结束之后回到初始位置，在延迟的情况下，让0%在延迟后生效
  - backwards :       在延迟的情况下，让0%在延迟前生效
  - forwards :       在运动结束的之后，停到结束位置
  - both :       backwards和forwards同时生效

- **an****imation-direction** :      属性定义是否应该轮流反向播放动画。

- - alternate :       一次正向(0%~100%)，一次反向(100%~0%)
  - reverse : 永远都是反向 , 从100%~0%
  - normal (默认值) : 永远都是正向 ,      从0%~100%

![幻灯片8](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%878-ce782a.png)

- 强大的CSS动画库

- - 官网地址：https://daneden.github.io/animate.css/
  - 使用方法：animation.css库的使用

![幻灯片9](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%879-3ecefa.png)

![幻灯片10](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8710-66150e.png)

**transform3D**

- **原理**

- - 3D的实际的原理      实际上就是通过在远处放置一个照相机，这样在照相机中会呈现3d的效果然后再转化成人眼视觉的方式呈现，然人看浏览器有3d的感觉

  - ![image-20240607012106422](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607012106422-2392ea.png)

  - rotateX() : 正值向上翻转

  - rotateY() : 正值向右翻转

  - translateZ() : 正值向前，负值向后

  - - 看起来好像是放大了，实际上并不是，而是物体靠近照相机的错觉，近大远小

  - scaleZ() : 立体元素的厚度

  - 实现一个立方体

- ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Document</title>
      <!-- 制作一个立方体并实现旋转效果 -->
      <style>
          *{margin:0;padding: 0;}
          ul{list-style: none;}
  
          .box{width: 300px;height:300px;border: 1px solid #000;}
          
          /* transform-style: preserve-3d; 前面这个是用3d的视角去看  transform-origin: center center -50px; 是当我们的物体是一个立方体的时候，我们的中心点需要写三个 */
          /* 但是z轴是没有center的格式的，所以我们需要使用像素变表示 */
          /* 实操时候注意我们需要用到是ul这个整体进行旋转操作 */
          .box ul{width: 100px;height:100px;margin:100px;position: relative;transition: 1s;transform-style: preserve-3d;transform-origin: center center -50px;}
          .box ul li{width: 100px;height: 100px;font-size: 30px;color: white;line-height: 100px;text-align: center;}
  
          /* 注意下面对于立方体的构建的过程，我们transform-origin: right;可以以边为轴，并不是一定以一个固定的点作为基点进行旋转，平移，缩放的操作 */
          .box ul li:nth-child(1){float: left;background: red;position: absolute;left: 0px;top:0px;}
          .box ul li:nth-child(2){float: left;background: blue;position: absolute;left: -100px;top:0px;transform-origin: right;transform: rotateY(-90deg);}
          .box ul li:nth-child(3){float: left;background: hotpink;position: absolute;left: 100px;top:0px;transform-origin: left;transform: rotateY(90deg);}
          .box ul li:nth-child(4){float: left;background: gray;position: absolute;left: 0px;top:-100px;transform-origin: bottom;;transform: rotatex(-90deg);}
          .box ul li:nth-child(5){float: left;background: green;position: absolute;left: 0px;top:100px;transform-origin: top;transform: rotatex(90deg);}
          .box ul li:nth-child(6){float: left;background: yellow;position: absolute;left: 0px;top:0px;transform: translateZ(-100px) rotateY(180deg);}
  
          .box:hover ul{transform: rotateY(1080deg);}
      </style>
  </head>
  <body>
      <div class="box">
          <ul>
              <li>1</li>
              <li>2</li>
              <li>3</li>
              <li>4</li>
              <li>5</li>
              <li>6</li>
          </ul>
      </div>
  </body>
  </html>
  
  ```

- perspective :     离屏幕多远的距离去观察元素，值越大幅度越小。

- perspective-origin :     景深-基点位置，观察元素的角度。

  - ![image-20240607012204617](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607012204617-4181aa.png)

- transform-origin : x y z

- - x,y都是可以写left,right,center的 但是z只能写像素值

- - transform-origin:      right;可以以边为轴，并不是一定以一个固定的点作为基点进行旋转，平移，缩放的操作

- transform-style : 3D空间

- - flat (默认值2d)
  - preserve-3d  (3d，产生一个三维空间)

- backface-visibility : 背面隐藏

- - hidden
  - visible (默认值)

3d的写法

- scale3d() : 三个值 x y z
- translate3d() : 三个值 x y z
- rotate3d() : 四个值     0|1(x轴是否添加旋转角度)      0|1(y轴是否添加旋转角度)      0|1(z轴是否添加旋转角度) deg

练习-照片旋转木马

- 原理：
  - ![image-20240607012240937](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607012240937-23bd63.png)

![幻灯片11](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8711-540385.png)

CSS3背景扩展

- background-size : 背景图的尺寸大小

- - background-size: 50px 200px;

  - - 背景图的尺寸大小，可以写两个像素 一般不用       拉伸后的效果特别丑

  - cover : 覆盖

    - ![image-20240607011943547](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011943547-d1783b.png)
    - 覆盖:等比放大到充满整个区域 多余部分被裁剪掉     max(width,length)

  - contain : 包含 

  - - 包含:等比放大到其中一个边到边界 剩余部分留白      min(width,length)

- background-origin :     背景图的填充位置(会对平铺产生影响)

- - padding-box (默认)

  - - 默认的情况是padding-box，默认填充到padding区域

  - border-box

  - - border-box填充到padding区域是bordr及border以内的区域

  - content-box

  - - content-box填充到padding区域是content区域

- background-clip : 背景图的裁切方式

- - 需要平铺看出效果

  - padding-box 

  - - padding-box，保留padding区域，以外部分裁切掉

  - border-box (默认) 

  - - 默认：border-box保留border及border内的区域，以外部分裁切掉

  - content-box 

  - - content-box保留content内的区域，以外部分裁切掉

- 以上三种可以写进background复合样式，位置在前，裁切在后面

- - background: url(img/1.png)      content-box padding-box;

![幻灯片12](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8712-c69f57.png)

CSS3渐变

- 线性渐变-linear-gradient     是值，需要添加到background-image属性上

- - `background-image:linear-gradient(red,blue,yellow,green);`

  - ![image-20240607011812950](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011812950-5778c3.png)

  - 指定渐变方向

  - - `background-image:linear-gradient(to top, red,blue,yellow,green);`
    - ![image-20240607011802018](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011802018-b20062.png)
    - `background-image:linear-gradient(to right bottom, red,blue,yellow,green);`
    - ![image-20240607011754348](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011754348-8d9b04.png)

- - 渐变的0度是在页面的下边，正值会按照顺时针进行旋转，负值会按照逆时针进行旋转

  - - `background-image:linear-gradient(70deg, red,blue,yellow,green);`

  - percentage 指定渐变的区域

  - - `background-image:linear-gradient(red 25%,blue 75%);`
    - ![image-20240607011747845](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011747845-97bab1.png)

- radial-gradient : 径向渐变 从中心点向四周进行渐变(用的不多)

- - point
  - color
  - percentage
    - ![image-20240607011738317](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011738317-7332a8.png)
    - `background-image: radial-gradient(red 25%,blue 50%,yellow 75%);`

![幻灯片13](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8713-8a751a.png)

字体图标

font-face是CSS3中的一个模块，他主要是把自己定义的Web字体嵌入到你的网页中。

![image-20240607011312458](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011312458-b8ea59.png)

- 好处：
  - **可以非常方便的改变大小和颜色**
    - font-size  color直接对其进行修改，图片大小容易改，但是颜色很难
  - **放大后不会失真**
  - **减少请求次数和提高加载速度**
  - **简化网页布局**
  - **减少设计师和前端工程师的工作量**
  - **可使用计算机没有提供的字体**
- **使用**

```css
@font-face{
        font-family:hello;
        src:url(https://at.alicdn.com/t/font_1401963178_8135476.eot);
        src:url(https://at.alicdn.com/t/font_1401963178_8135476.eot?#iefix) format('embedded-opentype'),url(https://at.alicdn.com/t/font_1401963178_8135476.woff) format('woff'),url(https://at.alicdn.com/t/font_1401963178_8135476.ttf) format('truetype'),url(https://at.alicdn.com/t/font_1401963178_8135476.svg#iconfont) format('svg')
}
```

上面的.woff和.tff等都是做兼容平台处理的

![image-20240607011512511](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607011512511-9f4aec.png)

- 阿里巴巴图标库的使用

- - 官网：https://www.iconfont.cn
  - 使用方法：[阿里巴巴的字体图标的使用](onenote:库.one#阿里巴巴的字体图标的使用&section-id={7249D97A-E96C-4E6D-A804-E99AFA1EC12E}&page-id={E622B720-88FC-4855-B572-8D7F6115176A}&end&base-path=https://d.docs.live.net/d208791e5d209aae/文档/2020_waws/代码能力/前端)

- 自定义字体图标

- - 网站：https://icomoon.io/app
  - 制作和使用方法：[自定义字体图标使用](onenote:库.one#自定义字体图标使用&section-id={7249D97A-E96C-4E6D-A804-E99AFA1EC12E}&page-id={61B21043-7CB7-4E14-88D5-4AB97EFCEF35}&end&base-path=https://d.docs.live.net/d208791e5d209aae/文档/2020_waws/代码能力/前端)

![幻灯片14](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8714-bec818.png)