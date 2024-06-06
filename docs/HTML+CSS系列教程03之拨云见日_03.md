# HTML+CSS系列教程03之拨云见日_03

![幻灯片2](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%872-45834f.png)

- 压缩格式

- - gif

  - - 支持动画
    - 只有全透明和不透明两种模式
    - 只有256种颜色

  - **png**(使用最广)

  - - 采用无损压缩算法
    - 体积也相对较小

  - - **支持背景透明**

  - - 不支持动画

  - jpg = jpeg

  - - 采用有损压缩算法
    - 体积较小
    - 不支持透明
    - 不支持动画

  - svg

  - - 无论怎样放大都不会失真
    - 只是保留了图片的形状和颜色（相对简单，计算机可以重新计算）

  - psd是设计稿的原生设计图

  - - photoshop的原始文件

![幻灯片3](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%873-d86664.png)

![幻灯片4](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%874-fb0f6d.png)

photoshop psd切图的流程：psd自动切图流程

![幻灯片5](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%875-0b239e.png)

企业级切图的流程：

蓝湖工具：https://lanhuapp.com/

蓝湖配合ps快速开发：企业级开发--蓝湖

![幻灯片6](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%876-6264ba.png)

![幻灯片7](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%877-bd05ac.png)

![幻灯片8](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%878-805764.png)

float浮动

- 文档流

- - 文档流是文档中可显示对象在排列时所占用的位置

- float特性

- - 加浮动的元素，会脱离文档流，会延着**父容器**靠左或靠右排列，如果之前**已经有浮动的元素，会挨着浮动的元素进行排列**

  - ![image-20240606231653861](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606231653861-1cec23.png)

  - float的取值

  - - left
    - right
    - none(默认)

  - 特点解析

    - ![image-20240606231855500](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606231855500-f4832d.png)
    - ![image-20240606231903236](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606231903236-0c5ebc.png)

- 注意事项

- - 浮动只会影响下面的文档流，对上面的元素无影响

  - 文字不会被浮动元素遮蔽，楼层半层，环绕可见

    - ![image-20240606231923926](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606231923926-6fe81e.png)

  - 浮动之前的元素宽不设置和父容器相同，设置浮动之后，**浮动元素部分的宽度由内容决定**

    - ![image-20240606231944935](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606231944935-ba159c.png)
    - ![image-20240606231953616](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606231953616-0e5311.png)

  - 多个浮动元素一行排不下，会怎样进行布局

    - 折行显示
      - 浮动元素在排列时候，只参考前一个元素的位置即可
      - ![image-20240606231843727](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606231843727-5eb4ee.png)
      - 具体的折行显示规则：浮动排列，折行显示规则

  - 浮动主要是给块元素添加的，但是也可以给内联元素添加

  - - 块完成的就是**布局**

- 清除浮动

- - 上下排列：clear属性，表示清除浮动的 取值：left，right，both

    - ![image-20240606232143697](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232143697-9dd14f.png)

  - 清除浮动的时候注意要统一，上面用的是右浮动，就去清理右浮动

  - - 不一致的清除，不会有效果

  - 嵌套-清除浮动

    - 问题：

      - ![image-20240606232155974](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232155974-6c1e6d.png)

    - 解决办法

    - - 固定宽高  :       不推荐 , 不能把高度固定死，不适合做自适应的效果。

      - 父元素浮动 : 不推荐 , 因为父容器浮动也会影响到后面的元素。

      - - 我们看到aaa应该出现在下方，现在布局中出现在右侧
        - ![image-20240606232208550](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232208550-a4eb18.png)

    - - overflow : hidden (BFC规范) ,     如果有子元素想溢出，那么会受到影响。

      - display : inline-block (BFC规范)，不推荐，父容器会影响到后面的元素。

        - ![image-20240606232216530](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232216530-dffcf1.png)

      - **设置空标签** : 不推荐 , 会多添加一个标签。

      - **after伪类** : 推荐，是空标签的加强版，目前各大公司的做法

      - -  ( clear属性只会操作块标签，对内联标签不起作用 )
        - 设置空标签和:after伪类的方式实际上就是在浮动元素下方增加一个看不见的东西，然后添加clear,将父元素的区域撑开，这样就可以解决由嵌套浮动引起的布局混乱问题了

![幻灯片9](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%879-08e3fe.png)

![幻灯片10](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8710-3e6cd9.png)

![幻灯片11](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8711-61f199.png)

![幻灯片12](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8712-55f664.png)

![幻灯片13](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8713-f5c662.png)

定位

- 浮动比较适合左右元素的布局，定位更适合做一个元素在另一个元素上展示的操作

- position特性

- - css position属性用于指定一个元素在文档中的定位方式。top/left/right/bottom属性决定了该元素的最终位置

  - 取值

  - - static(默认)

    - relative

    - - left 100px top 100px
        - ![image-20240606232811519](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232811519-75f184.png)
      - left 100px bottom 100px
        - ![image-20240606232823121](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232823121-8d932c.png)
      - 会出现遮盖现象
        - ![image-20240606232832593](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232832593-36ead0.png)

  - - absolute

    - - 使当前元素脱离文档流

        - ![image-20240606232843052](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232843052-a478db.png)

      - 内联元素支持宽高

        - ![image-20240606232851243](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232851243-feeab2.png)

      - 使块元素默认宽根据内容决定(让块具备内联的特性)

        - ![image-20240606232900680](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232900680-476742.png)

      - 如果有定位祖先元素相对于定位祖先元素发生偏移，没有定位祖先元素相对于整个文档发生偏移(绝对、相对、固定)  简言之：有父定位元素，偏移看父定位元素；否则看整个文档

      - - 父元素有其中一种定位方式都是按照父元素进行绝对定位
        - ![image-20240606232911607](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232911607-50b669.png)
        - ![image-20240606232922442](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232922442-57a73b.png)

    - fixed

    - - 使当前元素脱离文档流
        - ![image-20240606232932497](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232932497-461e33.png)
      - 内联元素支持宽高(和上面一样)
      - 使块元素默认宽根据内容决定(让块具备内联的特性)(和上面一样)
      - 相对于整个浏览器窗口进行偏移，不受到浏览器滚动条的影响

  - - sticky

    - - 在指定位置，进行粘性操作

      - - 单独使用没用

      - 需要配合top/bottom/left/right进行使用，假如是top=0,这样就是随着滚动条向下滑，当这个元素的位置达到top=0是就定在那不动了，相当于absolute+fixed的合体

  - - z-index

    - - 可以改变定位的层级

      - - 可以写0、正数、负数
        - ![image-20240606232945477](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232945477-2f6604.png)
        - ![image-20240606233003279](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606233003279-38d494.png)

    - - 嵌套的时候，只是比较同层元素的定位级别，和内嵌元素无关(即使优先等级比较高)

      - - parent z-index:-1 son      z-index:3  other:0  parent和other同级，o的位置级别高，在外边，虽然son的z-index高，但是没用

![幻灯片14](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8714-74dcf6.png)

多行省略号也能做，但是支持的不是很好，单行的展示的省略号的支持比较强大

![幻灯片15](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8715-c12081.png)

**CSS精灵的优势**

- 100张小图片的质量叠加和远超过1张图片上100个图的质量

- 多张图片就需要多次的向后台请求数据，这样的话加载比较慢，同时服务器压力比较大

- 去精灵图中左侧的图

- - background:      url(./img/sprite_icon.png) no-repeat left -596px;  直接使用left 找上方高度即可

- 去精灵图中右侧的图

- - background:      url(./img/sprite_icon.png) no-repeat right -520px;  直接使用right 找上方高度即可

![幻灯片16](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8716-86a022.png)

半角的效果图：

- ![image-20240606232254279](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232254279-8e56b2.png)

- 设置border-radius:50%

- - 直接形成一个圆
    - aaa

- 原理
  - ![image-20240606232326784](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606232326784-db106b.png)
- 半圆

```css
#box6{
    width: 200px;
    height: 100px;
    background: red;
    border-radius: 100px 100px 0 0;
}
```



