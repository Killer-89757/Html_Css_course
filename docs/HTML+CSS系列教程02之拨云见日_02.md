## HTML+CSS系列教程02之拨云见日_02

![幻灯片2](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%872-024ad5.png)

CSS背景样式

- background-color:     red;   背景颜色  

- background-image:     url(img/购物车.png);  背景图片

- - 背景图片平铺方式

  - - 默认情况下是x,y轴都进行平铺

    - - background-repeat:no-repeat;   不平铺
      - background-repeat:repeat;      x,y轴平铺
      - background-repeat:repeat-x;    x轴平铺
      - background-repeat:repeat-y;     y轴平铺

    - 当背景图片没有区域大的时候，图片会选择进行平铺

    - 当背景图片比区域大的时候，图片只显示区域的大小

- background-position:     right bottom;

- - x:left、right、center

  - y:top、center、bottom

  - x,y---->number(px,%)      | 单词

  - - background-position:       right bottom;
    - background-position:       -100px 100px; 
    - background-position: 50% 50%; 

- background-attachmen 背景图片随滚动条的移动方式

- - background-attachment:      fixed;  固定不动，直到容器上移进入背景图片大小

  - - 背景位置是按照浏览器进行偏移的
    - ![image-20240606224504225](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606224504225-a5cae4.png)
    - background-attachment:     scroll;随着滚动条的移动而移动
    - 默认值：背景位置是按照当前元素进行偏移的
    - ![image-20240606224537108](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606224537108-a96384.png)

![幻灯片3](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%873-231376.png)

边框样式

- border

- - border-style 边框的样式

  - - solid 实线
    - dashed 虚线
    - dotted 点线

  - border-width 边框的大小 

  - border-color  边框的颜色

- border-方向

- - 只针对边框的某一边进行设置
  - border-left/top/bottom/right

- 边框做三角形的原理就是，两条线的拼接实际上是斜边拼接的方式

- ![image-20240606224558782](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606224558782-9398c2.png)

- 当我们将border的边设置为0我们就能得到四个拼接的三角形

- ![image-20240606224648446](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606224648446-0cd516.png)

- 隐藏掉不需要的，就是将不需要的边框的颜色设置成透明即可

- - 颜色：透明颜色,transparent

  - - 设置成透明的颜色不用关心背景色如何更改
    - ![image-20240606224706422](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606224706422-bf4eba.png)

![幻灯片4](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%874-489f67.png)

**font-family**

div{font-family:"Arial","宋体","微软雅黑"}

**字体的识别与否是根据自己的电脑里是否存在这个字体相关的**

- 存在相应的字体，则成功应用
- 不存在，则在找font-family中的后续字体
- 如果font-family中都不能匹配，就采用自己电脑的默认字体进行显示

**引号的问题**

- 当我们设置的字体中存在空格的情况下，我们需要加上引号，否则不用

**fon****t-size**

- 默认的大小 16px

- 写法：像素值px | (small、large、medium)不推荐

- 字体大小一般设置为偶数

- - 是因为我们一般会设置文字进行对齐，对齐一般是字体大小的一半的位置为中轴线，偶数/2=整数，但是奇数/2=小数，对齐可能出现莫名的问题

- **font-weight**

- - 模式：正常(normal) | 加粗(bold)
  - 写法：单词(normal、bold)|数值(100~500(nornal)      600~900(bold))

- **font-style**

- - 模式：正常(normal)  斜体(italic)

  - 写法：单词(normal、italic)

  - 注：oblique也表示的是斜体，一般用的比较少

  - - 区别：

    - - italic 所有带有倾斜字体的可以设置倾斜操作
      - oblique 即使不带有倾斜字体的也可以设置倾斜操作

- **color**

- - 字体的颜色

![幻灯片5](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%875-d6a2f7.png)

![幻灯片6](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%876-88635f.png)

![幻灯片7](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%877-a3c3c5.png)

![幻灯片8](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%878-feba75.png)

段落样式

- test-decoration 文本修饰

- - 下划线 underline

  - 上划线 overline

  - 删除线 line-through

  - 不添加任何装饰 none

  - 可以添加多个 空格隔开

  - - text-decoration: overline       underline line-through;

- text-transform

- - 文本的大小写

  - - uppercase  全部大写
    - capitalize  首字母大写
    - lowercase  全部小写

- text-indent

- - 文本首行缩进

  - text-indent:      32px;  默认字体大小16px 这个是首行两个字的位置

  - em 是读取该行文字的大小作为一个单位，是相对的

  - - 这样我们不用计算像素值，直接首行缩进两个字

    - - text-indent: 2em;

- test-align

- - 文本对齐方式

  - - text-align: right; 右对齐
    - text-align: center; 居中对齐
    - text-align: left; 左对齐(默认)
    - text-align:       justify; 两端点对齐

- line-height:行高

- - 什么是行高，一行文字的高度，上边距和下边距是等价关系。

  - 默认的行高，不是固定的值，而是变化的，根据当前字体的值的大小在不断的变化

  - ![image-20240606224752336](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606224752336-d6a54b.png)

  - 取值：

  - - number (px)
    - scale(比例值，跟文字的大小成比例 1=文字大小，2=文字大小两倍)

- - letter-spacing:字之间的间距

  - - 汉字中的每一个字
    - 英文中的每一个字母

  - word-spacing:词之间的间距

  - - 汉字(不起作用)
    - 英文中的每一个单词

  -  折行(针对英文，数字)

  - ![image-20240606224813583](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606224813583-df0ba8.png)

  - word-break:break-all(非常强烈的折行)

  - ![image-20240606224830128](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606224830128-ba781f.png)

  - word-wrap:break-world(不是那么强烈的折行)

  - ![image-20240606224857340](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606224857340-fe8b7c.png)

![幻灯片9](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%879-d13379.png)

![幻灯片10](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8710-c72d8a.png)

![幻灯片11](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8711-906cfc.png)

![幻灯片12](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8712-1e2ba3.png)

CSS复合样式

- 复合的写法，是通过空格实现的

- background,border顺序不用考虑，程序会自行判断

- font 需要按照顺序进行书写

- - 最少要有两个值 size、family 顺序
  - weight style size      family 正确
  - style weight size      family 正确
  - weight style      size/line-height family 正确

```html
/*background,border顺序不用考虑，程序会自行判断*/
background: red url(img/购物车.png) no-repeat center center;
border: 10px black solid;
/* border-right: 10px black solid; */
font:24px 华文彩云;
```

- 尽量不要混写，如果非要混写，那么一定要先写复合样式在写单一样式

- - 原因是先写了单一样式，应用了之后，然后在应用复合样式的时候，复合样式中没有之前指定的单一样式，这样的话，系统默认这个单一样式被复合样式中的样式(无设置)覆盖掉，也就是没有设置，最终导致单一样式的设置没有效果

![幻灯片13](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8713-afc7f8.png)

CSS选择器

```html
常用的CSS命名规则   

1.注释的写法:   
/* Footer */   
内容区    
/* End Footer */

2. id的命名:  
(1)页面结构   
容器: container 
页头：header    
内容：content/container   
页面主体：main   
页尾：footer   
导航：nav   
侧栏：sidebar   
栏目：column    
页面外围控制整体布局宽度：wrapper   
左右中：left right center   

(2)导航   
导航：nav    
主导航：mainbav   
子导航：subnav   
顶导航：topnav   
边导航：sidebar   
左导航：leftsidebar   
右导航：rightsidebar   
菜单：menu    
子菜单：submenu   
标题: title    
摘要: summary   

(3)功能   
标志：logo   
广告：banner   
登陆：login    
登录条：loginbar   
注册：regsiter   
搜索：search   
功能区：shop 
标题：title    
加入：joinus   
状态：status   
按钮：btn   
滚动：scroll   
标签页：tab   
文章列表：list   
提示信息：msg   
当前的: current   
小技巧：tips   
图标: icon   
注释：note   
指南：guild   
服务：service   
热点：hot 
新闻：news   
下载：download   
投票：vote    
合作伙伴：partner   
友情链接：link   
版权：copyright   

3.class的命名:    
(1)颜色:使用颜色的名称或者16进制代码,如   
.red { color: red; }   
.f60 { color: #f60; }   
.ff8600 { color: #ff8600; }    

(2)字体大小,直接使用”font+字体大小”作为名称,如  
.font12px { font-size: 12px; }   
.font9pt {font-size: 9pt; }   

(3)对齐样式,使用对齐目标的英文名称,如   
.left { float:left; }    
.bottom { float:bottom; }    

(4)标题栏样式,使用”类别+功能”的方式命名,如   
.barnews { }   
.barproduct { }   


主要的 master.css   
模块 module.css   
基本共用 base.css   
布局，版面 layout.css   
主题 themes.css   
专栏 columns.css   
文字 font.css   
表单 forms.css   
补丁 mend.css   
打印 print.css
```

- ID选择器

- - CSS:#elem{}   HTML: id="elem"

- - 在一个页面中，Id值是唯一的

- - 命名规范，字母 _ - 数字 (数字不能放在第一位)
  - 命名方式 ：驼峰式 aaaBbb() 下划线 短划线

- Class 选择器

- - CSS:.elem{}   HTML: calss="elem"
  - class选择器是可以复用的
  - 可以添加多个class样式
  - 多个标签的时候，样式的优先级根据CSS决定，而不是class属性中的顺序
  - 标签+类的写法
  - ![image-20240606225043465](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606225043465-e3f36f.png)

- 标签选择器(tag选择器)

- - CSS:div{}   HTML: <div></div>

  - 复杂的需求中使用较多，定位元素

  - - 去掉某些标签的默认的样式的时候
    - 复杂的选择器中，一般层次选择器中应用较多

- 群组选择器

- - CSS:div,p,span{}
  - 可以通过逗号的方式，给多个不同的选择器添加统一的CSS样式，来达到代码的复用
  - 注意：群组不是层次，这里div标签，p标签，span标签的元素都应用的CSS样式，并不是div下面的p下面的span标签(注意)

- 通用选择器

- - CSS:*{}

  - 给所有的标签都加上CSS样式

  - 注：尽量避免使用通配选择器，因为会给所有的标签添加样式，慎用

  - 使用场景：

  - - 去掉所有标签的默认标签时

- 层次选择器

- - 后代选择器

  - - M N{} 空格隔开

  - 父子选择器

  - - M>N{} 大于号隔开

  - 兄弟选择器

  - - M~N{} ~隔开
    - 选择当前找到的元素下面的兄弟，添加CSS样式，上面的兄弟忽略

  - 相邻选择器

  - - M+N{} +隔开
    - 与M相邻的第一个N 会被设置CSS样式 其他的不会

- 属性选择器

- - M[attr]的形式
  - M[attr=value]的形式，严格按照value进行匹配
  - M[attr*=value]通配的方式,值在其中出现过即可匹配
  - M[attr^=value]通配的方式,值在开头出现才能匹配
  - M[attr$=value]通配的方式,值在结尾出现才能匹配
  - M[attr][attr]多属性方式匹配,存在多个属性才能匹配

- 伪类选择器**1**

- - CSS伪类用于向某些元素添加特殊的效果。一般用于初始样式添加不上的时候，用伪类来添加

  - M:伪类{}

  - - ：link  访问前的样式        (只能添加给a标签)

    - - 这个地方我使用的是百度的网址，一直显示的都是访问后的样式这个其实是和缓存有关，清理掉缓存即可展现访问前的效果

      - - 一般选择清理过去一个小时的就行，如不成功，将高级中的所有的选项全部勾选即可

      - 清理缓存的快捷键ctrl+shift+del

      - ![image-20240606225116648](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606225116648-5572a6.png)

      - ：visited  访问后的样式 (只能添加给a标签)

      - ：hover  鼠标移入时的样式 (所有标签都适用)

      - ：active  鼠标按下时的样式 (所有标签都适用)

  - 可以在控制台上进行观察

    - ![image-20240606225207112](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606225207112-070dd5.png)
    - ![image-20240606225220576](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606225220576-980c20.png)
    - ::after 属于伪元素，之后在详细说明 

- - **:****b****efore**

  - - 在选中元素的前面添加

- 针对表单元素

- - **:checked**

- - - 复选框、当选中的时候才会发生变化
    - ![image-20240606225504220](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606225504220-28754a.png)

- **:disabled**

- - 复选框、当框不可用的时候才会发生变化
  - ![image-20240606225610594](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606225610594-091026.png)

- **:focus**

- - 输入框、当框中获取光标的时候才会发生变化
  - ![image-20240606225639296](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606225639296-8f1163.png)

- 结构性伪类选择器

- - nth-of-type

  - - li:nth-of-type(3){background-color:       red;}

    - - 角标是从1开始的，1表示第一项，2表示第二项 

    - li:nth-of-type(n){background-color:       red;}

    - - n值 表示从0到无穷大,所有符合条件的都应用样式

    - li:nth-of-type(2n){background-color:       red;}

    - - n值 表示从0到无穷大,所有符合条件**偶数项**的都应用样式

    - li:nth-of-type(2n+1){background-color:       red;}

    - - n值 表示从0到无穷大,所有符合条件**奇数项**的都应用样式

    - first-of-type   第一个起作用

    - last-of-type   最后一个起作用

    - only-of-type  只有一个的时候起作用

  - nth-child

  - - div:nth-child(2){background-color:       blue;}
    - :nth-child()这个需要知道前面的元素在大的集合中排在第几个，简单说就是第几个孩子,元素和孩子不对应也添加不上CSS效果

  - 区别

  - - type:**类型**
    - child:**孩子**

- 

![幻灯片14](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8714-b581f2.png)

![幻灯片15](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8715-47fd4b.png)

![幻灯片16](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8716-a88644.png)

![幻灯片17](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8717-bd16c9.png)

![幻灯片18](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8718-d33073.png)

![幻灯片19](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8719-f0eac4.png)

![幻灯片20](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8720-e06671.png)

![幻灯片21](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8721-67fa5b.png)

样式继承

- 文字相关的样式可以被继承

- 布局相关的样式是不能被继承

- - 默认是不能继承

  - 使用inherit值进行继承

  - ![image-20240606225803138](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606225803138-9fd04d.png)

  - ```html
    div{
        width: 300px;
        height: 300px;
        background-color: red;
        border: 3px solid black;
        font-size: 30px;
        color: blue;
    }
    p{
        border: inherit;
    }
    ```

  - ![image-20240606225825009](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606225825009-b3e4ad.png)

![幻灯片22](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8722-fe3e31.png)

CSS优先级

- 相同优先级

- - 当设置相同样式时，后面的优先级较高，但是不建议出现重复设置样式的情况

- 内部样式和外部样式

- - 内部样式和外部样式优先级相同，如果都设置了相同的样式，那么后写的引入方式的优先级高

- 单一样式优先级

- - style **行间** **> id > class > tag > \* >** **继承**
  - ![image-20240606225850913](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606225850913-060f79.png)

- !important

- - 提升样式优先级，不建议使用

  - - 已经存在很多的样式，更改较麻烦，我们可以使用这样的方式，调整优先级
    - 注意：继承的方式不能使用！important的方式提升优先级

- 标签+类 和 单类

- - 标签 + 类 的优先级 大于 单类 的优先级

- 群组优先级

- - 群组优先级与单一选择器的优先级相同，靠后写的优先级更高

- 层次优先级

- - 权重比较

  - - ul li .box p input{} 1+1 + 10+1+1
    - .hello span #elem 10 + 1 + 100
    - 这个部分假设写100 个tag 其实优先级也是没有id 选择器高的，这个权重比较就是一种快速比较的方法 

  - 约分比较

  - - 上下比较约掉相同级别的元素
    - ul li .box p       input{} ===》 ul p input{}
    - .hello span #elem{} ====》 #elem{}        

  - 总结：

  - - 避免写超级复杂的选择器，尽量控制在三层以内，使用快速定位的方式进行添加样式

![幻灯片23](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8723-ee700b.png)

![幻灯片24](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8724-221b03.png)

![幻灯片25](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8725-cb7474.png)

**盒子模型**

- **组成：content**     **-> padding ->border ->margin**

- 快递   物品     填充物     包装盒    盒子间距 

  - ![image-20240606225945014](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606225945014-402aff.png)

  - centent:内容区域，由width和height决定

  - padding:内边距(内填充)

  - - 还可以只针对一个或几个方向进行设置

    - padding-left/top/bottom/right

    - - 单一样式只能使用一个值
      - ![image-20240606230022933](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606230022933-658dbc.png)

  - padding:30px(上下左右)

  - padding:30px     40px(上下,左右)

  - padding:30px     40px 20px(上,左右,下)

  - padding:30px     40px 50px 60px(上,右,下,左)--顺时针

  - border：边框

  - margin:外边距

    - ![image-20240606230111908](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606230111908-601681.png)

    - 还可以只针对一个或几个方向进行设置

    - margin-left/top/bottom/right

    - - 单一样式只能使用一个值

    - margin:30px(上下左右)

    - margin:30px     40px(上下,左右)

    - margin:30px     40px 20px(上,左右,下)

    - margin:30px 40px 50px     60px(上,右,下,左)--顺时针

- 在控制台中进行观察

  - ![image-20240606230144096](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606230144096-715de0.png)
  - ![image-20240606230153690](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606230153690-4ea285.png)
  - ![image-20240606230203985](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606230203985-a5c43b.png)

- **注意**

- - 背景颜色会被填充到margin以内(包括边框)的区域，我们可以将边框的颜色设置成透明transparent进行验证

  - - 背景图也会对padding和border的位置进行填充

  - 文字在centent的区域进行添加

  - padding不能出现负值，但是margin可以

  - - 理解就是填充物不能进入物品内部，但是两个快递是可以叠加摆放(margin为负数)的
    - ![image-20240606230230035](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606230230035-59dd13.png)

- box-sizing

- - 盒尺寸，可以改变盒子模型的展示形态

  - 默认值 content-box

  - - width,height->       content

  - border-box

  - - width,height->       content,padding,border
    - ![image-20240606230249051](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606230249051-6708ca.png)

- 使用场景

- - 不用在去计算某些值

  - 解决%的宽度和高度显示的问题

  - - input{width:100%;padding:30px}       

    - - 宽度已经100%了，加上padding,宽度大于浏览器宽度，出现滚动条 ，设置border-box,宽度还是浏览器的尺寸

- 盒子模型的一些问题

- - margin叠加问题

  - - 出现在上下margin同时存在的情况下，会取上下值中较大的作为叠加的值
    - ![image-20240606230338881](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606230338881-b3656b.png)
    - ![image-20240606230349041](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606230349041-62fee0.png)

- 决方法：

- - 遵循BFC法则
  - 上下只设置一个margin,大小符合规定即可

- margin传递问题

- - margin传递问题只会出现在嵌套的结构中，且只有margin-top会有传递的问题，其他三个方向没有传递的问题
  - ![image-20240606230720043](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606230720043-9aeb06.png)

- 不设置width
  - ![image-20240606230741083](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606230741083-7a7d78.png)

![幻灯片26](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8726-6d598e.png)

![幻灯片27](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8727-f8335a.png)

![幻灯片28](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8728-3f3fec.png)

![幻灯片29](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8729-da6a2f.png)

![幻灯片30](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8730-3a37fc.png)

标签分类

- 按类型

- - block

  - - div、p、ul、li、h1……
    - 独占一行
    - 支持所有样式
    - 不写宽的时候和父容器相同
    - 所占的区域是一个矩形

  - inline

  - - span、a、em、strong、img……

    - 挨在一起，排在一行

    - 有些样式不支持(img特殊)，例如：width、height、margin、padding某些方向不支持

    - 不写宽的时候，由内容撑开，没有内容的时候，宽度为零

    - 所占的区域是不一定是矩形

    - 内联之间存在空隙，空隙是由我们在代码中对inline元素的换行引起的

    - - <span>哈哈</span> <span>呵呵</span>

      - - 显示 ：哈哈呵呵

      - <span>哈哈</span>换行<span>呵呵</span>

      - - 显示 ：哈哈 呵呵

    - 布局一般使用的是块，span用于修饰文字的样式

- - inline-block

  - - input、select……
    - 挨在一起，排在一行，支持设置宽高
    - 既有块的特性，又有内联的特性

  - 通过控制台进行查看

    - ![image-20240606230500959](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606230500959-0625b0.png)
    - ![image-20240606230549276](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606230549276-f47745.png)
    - ![image-20240606230605809](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606230605809-39eb8b.png)

- 按内容

- - Flow 流内容 浏览器能够感知到的部分
  - Metadata 元数据 基础信息 一部分感知不到
  - Sectioning 分区
  - Heading 标题 H1~H6
  - Phrasing 措辞 em、strong、I
  - Embedded 嵌入的  img audio
  - Interactive 互动的 input select
  - 详细的在：https://html.spec.whatwg.org/multipage/dom.html

- 按显示

- - 替换元素

  - - 浏览器根据元素的标签和属性，来决定元素的具体显示内容

    - - img本身是没有显示的功能的，但是我们给属性src填上值之后，就有图片可以显示
      - input 按照type的值显示不同的东西，text、password、checkbox等

  - 非替换元素

  - - 将内容直接告诉浏览器，将其显示出来

    - - h1~h6 显示标题

![幻灯片31](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8731-4beef2.png)

![幻灯片32](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8732-c77063.png)

![幻灯片33](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8733-50aa3a.png)

显示框隐藏

- display:none;   不占空间的隐藏
- visibility:hidden  占空间的隐藏

![幻灯片34](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8734-497821.png)

标签嵌套规范

- 一些标准组合标签不能随意乱用

- - ul>li、ol>li
  - dl>dt>dd
  - table>tr>td

- 块标签可以嵌套内联标签

- - <div><span></span></div>
  - <div><a></a></div>

- 块标签中不一定能嵌套块标签

- - 可以的

  - - <div><div></div></div>

  - 不可以

  - - <p><div></div></p>

- 内联标签不能嵌套块标签

- - a标签是一个意外(将a加载完看成透明)

  - - <a href="">       <div></div></a>

![幻灯片35](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8735-74e7af.png)

溢出隐藏

- visible 默认

  - ![image-20240606231028549](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606231028549-89a49b.png)

- hidden 截断式隐藏

  - ![image-20240606231050781](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606231050781-0feb76.png)

- scroll 滚动隐藏

  - ![image-20240606231110502](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606231110502-a0afce.png)

- auto 自适应隐藏

  - ![image-20240606231122644](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606231122644-160038.png)

- auto和scroll的区别

- - 当内容较少时，auto会展示成截断式隐藏，不会出现滑动窗口
  - 当内容较少时，scroll会出现滑动窗口，但是不可滑动

- overflow-y,overflow-x针对两个轴分开设置

![幻灯片36](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8736-9cac36.png)

透明度和手势

- opacity 0(完全透明)~1(完全显示)

- - 0.5半透明
  - 即使完全透明还是占有空间
  - 注：所有的子内容都会透明处理

- rgba 

- - 专门针对背景进行操作
  - background-color:rgba(255,0,0,0.4); 

- cursor 手势

- - 默认箭头

  - pointer 手形

  - move 四角箭头

  - 自定义手势

  - - 准备图片 .cur .ico格式
    - cursor:       url(img/cursor.ico),auto;

![幻灯片37](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8737-b280e3.png)

最大、最小宽高

- 最小宽高

- - min-wight、min-height
  - 当我们的内容比较少的时候式固定的宽高，当内容较多的时候宽高随着内容的多少实现自适应

- 最大宽高

- - max-wight、max-height
  - 当我们的内容比较多的时候式固定的宽高，当内容较少的时候宽高随着内容的多少实现自适应

- %

- - 单位换算-->以父容器的大小进行计算(和祖先没有关系)
  - 一个容器怎么适应屏幕的高，容器加height:100%      body:100% html:100%

![幻灯片38](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8738-b49ad3.png)

默认样式

- 没有默认样式：div、span

- 有默认样式的

- - body ->margin:8px

  - h1 -> margin 上下 21.440px

  - - font-weight :bold

  - p -> margin 上下 16px

  - ul -> margin 上下16px padding-left 40

  - - list-style-type  disc

  - a -> text-decoration      underline;

![幻灯片39](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8739-ae2901.png)

重置样式

- *{margin:0;padding:0}

- - 优点：不用考虑哪些标签有默认的margin和padding
  - 缺点：稍微影响性能

- ul{list-style:none} 

- - 去除li前面的点

- 链接的下划线去掉

- - a{text-decoration:none;color:#666}

- 图片和边框有缝隙

- - 图片inline 对齐方式是和文字的基线对齐，并不是文字的底线对齐
  - ![image-20240606231303670](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606231303670-78cb4b.png)

- - img{vertical-align:baseline} 基线对齐 默认的方式
  - img{vertical-align:bottom} 底线对齐 解决空隙
  - img{display:block} 转成块解决空隙

- 写具体的页面的时候

- - 写结构
  - css重置样式
  - 写具体的样式

- 比较好的CSS的reset

- - https://blog.csdn.net/brain_bo/article/details/81560444