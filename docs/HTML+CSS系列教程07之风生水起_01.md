# HTML+CSS系列教程07之风生水起_01

![幻灯片3](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%873-07ebad.png)

![幻灯片4](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%874-cf8e0c.png)

**弹性盒模型加在父容器上的属性**

**flex-direction**

flex-direction用来控制子项的整体布局方向，是从右往左还是从左往右，是从上往下还是从下往上

- row默认左上
  - ![image-20240607003052904](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003052904-e7d00d.png)
- row-reverse
  - ![image-20240607003101929](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003101929-6f74e6.png)
- column
  - ![image-20240607003109169](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003109169-0ad00b.png)
- column-reverse
  - ![image-20240607003118020](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003118020-f4f709.png)

![幻灯片5](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%875-9f7850.png)

**flex-wrap**

用来控制子项整体单行显示还是换行显示

- 默认nowrap(不换行，宽度会自适应的调整,当行中元素的内容过多的时候，会发生溢出现象)
  - ![image-20240607003216084](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003216084-e68fb9.png)
- wrap(产生的空隙后面在解决)
  - ![image-20240607003209648](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003209648-4edea0.png)
- wrap-reverse
  - ![image-20240607003200077](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003200077-f9da28.png)

![幻灯片6](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%876-66e89c.png)

**flex-flow**

flex-flow属性是flex-direction和flex-wrap的缩写，表示flex布局的flow流动特性。**第一个值表示方向**，**第二个值表示换行，中间用空格隔开**。

![image-20240607003241790](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003241790-8b4705.png)

![幻灯片7](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%877-2b01f3.png)

**justify-content**

**主轴：row/column**

决定了主轴方向上子项的对齐和分布方式

-  flex-start

- - 默认值，表现为起始位置对齐。
  - ![image-20240607003426806](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003426806-a76787.png)

- flex-end

- - 表现为结束位置对齐。
  - ![image-20240607003433827](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003433827-b21fcc.png)

- center

- - 表现为居中对齐。
  - ![image-20240607003441724](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003441724-3eee21.png)

- space-between

- - 表现为两端对齐。between是中间的意思，意思是多余的空白间距只在元素中间区域分配。
  - ![image-20240607003448519](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003448519-233796.png)

- space-around

- - around是环绕的意思，意思是每个flex子项两侧都环绕互不干扰的等宽的空白间距，最终视觉上边缘两侧的空白只有中间空白宽度一半。
  - ![image-20240607003457454](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003457454-ab856f.png)

- space-evenly

- - evenly是匀称、平等的意思。也就是视觉上，每个flex子项两侧空白间距完全相等。
  - ![image-20240607003418678](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003418678-ca3046.png)

![幻灯片8](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%878-ef9202.png)

**align-items**

align-items中的items指的就是flex子项们，因此align-items指的就是flex子项们相对于flex容器在侧轴方向上的对齐方式。 

- stretch

- - 默认值，flex子项拉伸。
  - ![image-20240607003643252](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003643252-1d7354.png)

- flex-start

- - 表现为容器顶部对齐。
  - ![image-20240607003635442](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003635442-a6b2f4.png)

- flex-end

- - 表现为容器底部对齐。
  - ![image-20240607003628758](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003628758-2a6efc.png)

- center

- - 表现为垂直居中对齐。
  - ![image-20240607003618274](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003618274-2fa19c.png)

![幻灯片9](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%879-1582d3.png)

**align-content**

align-content可以看成和justify-content是相似且对立的属性，如果所有flex子项只有一行，则align-content属性是没有任何效果的。

- stretch

- - 默认值。每一行flex子元素都等比例拉伸。例如，如果共两行flex子元素，则每一行拉伸高度是50%。
  - ![image-20240607003940994](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003940994-bfd8ca.png)

- flex-start

- - 表现为起始位置对齐。
  - ![image-20240607003924490](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003924490-826297.png)

- flex-end

- - 表现为结束位置对齐。
  - ![image-20240607003915935](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003915935-d2a37e.png)

- center

- - 表现为居中对齐。
  - ![image-20240607003906306](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003906306-811d11.png)

- space-between

- - 表现为两端对齐。
  - ![image-20240607003859175](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003859175-4a7792.png)

- space-around

- - 每一行元素上下都享有独立不重叠的空白空间。
  - ![image-20240607003845445](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607003845445-0421b0.png)

![幻灯片10](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8710-fd9515.png)

**弹性盒模型加在子元素上的属性**

**作用在flex子项上的CSS属性**

- **order**

- - 可以通过设置order改变某一个flex子项的排序位置。所有flex子项的默认order属性值是0。
  - ![image-20240607002737391](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002737391-1bcab7.png)

-  **flex-grow**

- - 属性中的grow是扩展的意思，扩展的就是flex子项所占据的宽度，扩展所侵占的空间就是除去元素外的剩余的空白间隙。默认值为0。
  - ![image-20240607002745276](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002745276-dd1ec5.png)
  - ![image-20240607002752091](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002752091-63fbe6.png)
  - ![image-20240607002759534](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002759534-0b923d.png)

- **flex-shrink**

- - 属性中的shrink是“收缩”的意思，flex-shrink主要处理当flex容器空间不足时候，单个元素的收缩比例。默认值是1。
  - ![image-20240607002813374](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002813374-08474e.png)
  - ![image-20240607002820991](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002820991-2784c4.png)
  - ![image-20240607002829755](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002829755-99b39b.png)

- **flex-basis**

- - flex-basis定义了在分配剩余空间之前元素的默认大小。
  - flex-basis的优先级要高于width
  - ![image-20240607002855121](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002855121-1f284a.png)

- **flex**

- - flex属性是flex-grow，flex-shrink和flex-basis的缩写。
  - flex:0 1 auto;

- **align-self**

- - align-self指控制单独某一个flex子项的垂直对齐方式。
  - ![image-20240607002905116](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002905116-794c00.png)

![幻灯片11](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8711-86793c.png)

![幻灯片12](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8712-f5b06d.png)

**grid** **网格布局**

Grid布局是一个二维的布局方法，纵横两个方向总是同时存在。

**网格布局模型加在父容器上的属性**

- **grid-template-columns**

- **grid-template-rows**

- - 对网格进行横纵划分，形成二维布局。单位可以是像素，百分比，自适应以及fr单位（网格剩余空间比例单位fr）。

  - - 0.几不会填满，会有空余
    - fr是比例单位，表示占据这个表格的多少的比例
    - ![image-20240607004200194](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607004200194-7f9f2c.png)

- - grid-template-rows: 100px auto 30%;grid-template-columns: 100px 100px 200px 100px;

  - ![image-20240607004210837](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607004210837-839c62.png)

  - 可以使用 repeat(4,1fr);简化写法

  - - 有时候，我们网格的划分是很规律的，如果需要添加多个横纵网格时，可以利用repeat()语法进行简化操作。

    - 等价

    - - display: grid;grid-template-rows: 1fr 1fr 1fr;grid-template-columns: 1fr 1fr 1fr 1fr;
      - display: grid;grid-template-rows: repeat(3,1fr);grid-template-columns: repeat(4,1fr);

![幻灯片13](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8713-6f70a5.png)

![幻灯片14](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8714-52d66d.png)

- **grid-template-areas**

- **grid-template**

- - area是区域的意思，grid-template-areas就是给我们的网格划分区域的。此时grid子项只要使用grid-area属性指定其隶属于那个区。

  - grid-template是grid-template-rows，grid-template-columns和grid-template-areas属性的缩写。

  - - 在区域划分中不允许出现特殊图形。
    - ![image-20240607005449463](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607005449463-c400f6.png)

- - **分开复合写法**

- ```css
  /* grid-template的分开写的方式 */
  /* .box{width: 400px;height: 300px;border: 1px dotted #000;display: grid;grid-template-rows: repeat(3,1fr);grid-template-columns: repeat(4,1fr);
  grid-template-areas: 
  "a1 a1 a1 a1"
  "a2 a2 a2 a3"
  "a2 a2 a2 a3";
  } */
  
  /* grid-template的复合写法 */
  .box{width: 400px;height: 300px;border: 1px dotted #000;display: grid;grid-template:
  "a1 a1 a1 a1" 1fr
  "a2 a2 a2 a3" 1fr
  "a2 a2 a2 a3" 1fr
  /1fr 1fr 1fr 1fr;
  }
  ```

![幻灯片15](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8715-e2dd43.png)

- **grid-column-gap**

- **grid-row-gap**

- **grid-gap**

- - grid-column-gap和grid-row-gap属性用来定义网格中网格间隙的尺寸。
  - CSS      grid-gap属性是grid-column-gap和grid-row-gap属性的缩写
  - ![image-20240607005341746](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607005341746-20f570.png)

![幻灯片16](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8716-f9b0bb.png)

- **justify-items**

- **align-items**

- **place-items**

- - justify-items指定了网格元素的水平呈现方式，是水平拉伸显示，还是左中右对齐。align-items指定了网格元素的垂直呈现方式，是垂直拉伸显示，还是上中下对齐。

  - **place-items可以让align-items和justify-items属性写在单个声明中。**

  - - place-items的第一个参数是纵向的，第二个参数是水平的

  - justify    

  - - stretch

    - - **默认值，拉伸**。表现为水平或垂直填充。
      - ![image-20240607005002859](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607005002859-2bab35.png)

  - - Start

    - - 表现为容器左侧或顶部对齐。
      - ![image-20240607004955232](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607004955232-329423.png)

  - - end

    - - 表现为容器右侧或底部对齐。
      - ![image-20240607004946958](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607004946958-c388e9.png)

  - - center

    - - 表现为水平或垂直居中对齐。
      - ![image-20240607004940620](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607004940620-0d80e6.png)

- - **align**

  - - stretch

    - - **默认值，拉伸**。表现为水平或垂直填充。
      - ![image-20240607004931064](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607004931064-d1e6b0.png)

  - - Start

    - - 表现为容器左侧或顶部对齐。
      - ![image-20240607004922660](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607004922660-97778e.png)

  - - end

    - - 表现为容器右侧或底部对齐。
      - ![image-20240607004915437](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607004915437-62ac49.png)

  - - center

    - - 表现为水平或垂直居中对齐。
      - ![image-20240607004908369](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607004908369-28ac2d.png)

![幻灯片17](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8717-e88f9d.png)

- **justify-content**

- **align-content**

- **place-content**

- - justify-content指定了网格元素的水平分布方式。align-content指定了网格元素的垂直分布方式。place-content可以让align-content和justify-content属性写在一个CSS声明中。

  - 垂直的和水平的一样，不展示了

  - stretch

  - - 默认值，拉伸。表现为水平或垂直填充。
      - ![image-20240607005306694](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607005306694-881163.png)

- - start

  - - 表现为容器左侧或顶部对齐。
      - ![image-20240607005259328](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607005259328-a080aa.png)

- - end

  - - 表现为容器右侧或底部对齐。
      - ![image-20240607005252550](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607005252550-d52ac3.png)

- - center

  - - 表现为水平或垂直居中对齐。
      - ![image-20240607005243891](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607005243891-f8f6ef.png)

- - space-between

  - - 表现为两端对齐。
      - ![image-20240607005228241](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607005228241-9ee6fb.png)

- - space-around

  - - 享有独立不重叠的空白空间。
      - ![image-20240607005219551](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607005219551-32e1ba.png)

- - space-evenly

  - - 平均分配空白空间
      - ![image-20240607005209054](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607005209054-d2722f.png)

![幻灯片18](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8718-414136.png)

**grid** **网格布局**

**网格布局模型加在子元素上的属性**

![image-20240607004520778](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607004520778-0229b7.png)

- grid-column-start

- - 水平方向上占据的起始位置。

- grid-column-end

- - 水平方向上占据的结束位置。（span属性）

- grid-row-start

- - 垂直方向上占据的起始位置。

- grid-row-end

- - 垂直方向上占据的结束位置。（span属性）

```css
.box div{border: 2px #000 solid;background-color: red; 
    grid-column-end: 3;
    grid-column-start: 2;
    grid-row-end: span 2;
    grid-row-start: 2;
}
```

![image-20240607004603114](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607004603114-c4ed25.png)

- grid-column

- - grid-column-start + grid-column-end的缩写。

- - 合写的的时候第一个表示起始/第二个表示终止

- grid-row

- - grid-row-start + grid-row-end的缩写。

- grid-area

- - 表示当前网格所占用的区域，名字和位置两种表示方法。

- justify-self

- - 单个网格元素的水平对齐方式。

- align-self

- - 单个网格元素的垂直对齐方式。

- place-self

- - align-self和justify-self的缩写。

![幻灯片19](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8719-f88796.png)

![幻灯片20](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8720-4b7083.png)

![幻灯片21](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8721-8895d7.png)

访问一些网站的PC端和移动端

大一点的网站都是分开开发的，pc端一套代码，移动端一套代码

访问淘宝网-->后端检测当前的设备--->如果是PC端--->www.taobao.com

---> 后端检测当前的设备--->如果是移动端--->www.taobao.com--域名重定向--h5.m.taobao.com

**view****port**

在移动端viewport视口就是浏览器显示页面内容的屏幕区域。

在viewport中有两种视口，分别表示为， **visual viewport**（可视视口）和**layout viewport**（布局视口）。

visual viewport 固定大小跟屏幕大小相同，在上面，而layout viewport 可改变大小，在下面。Layout viewport默认大小为980像素，可通过document.documentElement.clientWidth获取。

现代网页需要将layout viewport设置成跟visual viewport等同大小，方便进行网页制作。

在我们的程序中有一句这样的代码：

<meta name="viewport" content="width=device-width, initial-scale=1.0">

width=device-width viewport这就是在规定视口的大小和设备的宽度相同

**设置：**

- 通过<meta>标签进行设置，name属性指定viewport值，content属性进行视口配置。

- - width          

  - - 设置layout       viewport的宽度特定值，device-width表示设备宽。

  -  height    

  - - 设置layout viewport的高度特定值，**一般不进行设置**。

  - initial-scale     

  - - 设置页面的初始缩放。

  - minimum-scale    

  - - 设置页面的最小缩放。

  - maximum-scale    

  - - 设置页面的最大缩放。

  - user-scalable    

  - - 设置页面能否进行缩放，一般设置成no。

- 百度/阿里的da'chang

- - 百度

  - - `<meta name="viewport" content="width=device-width,minimum-scale=1.0,maximum-scale=1.0,user-scalable=no"/>`

  - 阿里

  - - `<meta name=viewport content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no,viewport-fit=cover">`

- 设置之后的展示效果

- - 不设置width=device-width效果
    - ![image-20240607002440979](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002440979-63f37a.png)
  - 设置width=device-width的效果展示
    - ![image-20240607002433749](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002433749-b1094f.png)

**流式布局**

**流式布局和rem布局的不同**

- **流式布局**

- - **通过调整两个元素之间的间隔完成布局调整**

- **rem布局****(****等比缩放布局****)**

- - **通过放大或者缩小两个元素完成布局调整，间隔基本不变**

  - **单位**

    - ![image-20240607002420633](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002420633-c03af3.png)
    - em :     是一个相对单位，1em等于当前元素或父元素的font-size值。
    - rem :     是一个相对单位，1rem等于根元素的font-size值。
    - vw / vh : 把屏幕分为100份，1vw等于屏幕宽的1%。     
    - ![image-20240607002413339](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002413339-f277d2.png)

  - 动态的设置fontsize的大小，可以实现元素缩放适应

    - ![image-20240607002357480](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002357480-a02f14.png)
    - ![image-20240607002347901](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002347901-7efdaa.png)

  - 插件的使用

  - - 搜索扩展px to rem 安装

    - 安装完进行设置

      - ![image-20240607002330449](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002330449-8f9306.png)

    - 设置完，实战

      - ![image-20240607002321264](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002321264-08f193.png)

      - 快速转化多个px到rem

      - - 在想转化的部分直接部分选中，快捷键alt+z即可

- vw的使用

- - vw / vh :      把屏幕分为100份，1vw等于屏幕宽的1%。

![幻灯片22](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8722-bbea51.png)

![幻灯片23](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8723-17c359.png)

![幻灯片24](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8724-aa9347.png)

![幻灯片25](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8725-404198.png)

**模拟移动端**

![image-20240607001840103](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607001840103-0dd4f0.png)

![image-20240607001910013](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607001910013-ab3fdc.png)

![image-20240607001945631](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607001945631-69e13e.png)

![image-20240607002002759](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002002759-5c0e33.png)

![image-20240607002012393](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002012393-f7540c.png)

![image-20240607002019631](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607002019631-927d43.png)