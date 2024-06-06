# HTML+CSS系列教程09之巧夺天工_01

![幻灯片3](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%873-eab120.png)

![幻灯片4](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%874-5dcaf0.png)

![幻灯片5](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%875-85b809.png)

在vs code中进行less和sass的编写

- 下载插件并使用

  - ![image-20240607001047192](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607001047192-8192ee.png)
  - ![image-20240607001003053](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607001003053-a3864f.png)
  - ![image-20240607000953709](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000953709-bf972a.png)
  - ![image-20240607000945381](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000945381-1ea13a.png)

- 使用

- - 注释

  - - 多行注释就是我们的css的多行注释的方式，会被编译出来
    - 单行的注释是不会被编译出来的

  - 变量

  - - less

    - - 定义

      - - @number:123px;

      - 使用

      - - .box1{width: @number;height:         @number;}

    - sass

    - - 定义

      - - $num:123px;

      - 使用

      - - .box1{width: $num;height:         $num;}

  - 插值

  - - less

    - - 定义

      - - @key:margin;

      - 使用

      - - .box2{@{key}:auto;}

    - sass

    - - 定义

      - - $key:margin;

      - 使用

      - - .box2{#{$key}:auto;}

- - 作用域

    - ![image-20240606235015102](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606235015102-9c8fb3.png)

    - less

      - ```html
        //作用域
        .box2{
            @number:456px;
            width: $num;
        }
        ```

    - sass

    - - 注意这个地方有个差别，这个是看顺序的，不是单纯的作用域

      - ```html
        //作用域
        .box2{
            $num:456px;
            width: $num;
        }
        ```

      - ![image-20240607000927840](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000927840-821553.png)

  - 选择器嵌套

  - - less
      - ![image-20240607000917272](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000917272-654359.png)
    - sass
      - 和less是一样的

- - 伪类嵌套

  - - less
      - ![image-20240607000905333](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000905333-e6b85b.png)
      - 解决空格问题
        - ![image-20240607000856339](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000856339-b849fe.png)
    - sass
      - 和less的一样

- - 属性的嵌套

  - - 只有sass有,less没有
      - ![image-20240607000844476](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000844476-b1cb70.png)

- - 运算

  - 单位

  - - less
      - ![image-20240607000835047](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000835047-10da99.png)
    - sass
      - 不支持不同单位之间进行运算

- - 转义

  - - less

      - ![image-20240607000823908](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000823908-c881e7.png)

    - sass

      - ![image-20240607000812325](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000812325-ec59d9.png)

      - ![image-20240607000804283](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000804283-2905ce.png)

- - 颜色

  - - less
      - ![image-20240607000754722](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000754722-4ef413.png)
    - sass
      - 和less一样

- - 函数

  - - less
      - ![image-20240607000745843](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000745843-50ba73.png)
    - sass
      - round函数和less使用的一样
      - 具体函数具体分析
      - random() sass有 less没有
      - sqrt() sass没有 less有
      - sass的自定义函数
        - ![image-20240607000736047](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000736047-108a79.png)

- - 混入

  - - 把不同的css组合到一起，实现组合的方式
    - less
      - ![image-20240607000653364](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000653364-d9bdc0.png)
      - ![image-20240607000646646](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000646646-2bee59.png)
      - ![image-20240607000640849](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000640849-80b21a.png)
    - sass
      - ![image-20240607000633494](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000633494-b9d79a.png)
      - ![image-20240607000621881](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000621881-1e9918.png)

- - 命名空间

  - - less

    - - 只有less有，sass没有
      - ![image-20240607000614803](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000614803-7dc75d.png)

- - 继承

  - - less
      - ![image-20240607000606925](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000606925-5dc70a.png)
    - sass
      - ![image-20240607000551926](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000551926-80b789.png)
      - ![image-20240607000544812](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000544812-12d325.png)

- - 合并

  - - less
      - ![image-20240607000536729](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000536729-6c8c48.png)
      - ![image-20240607000528178](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000528178-ed4a87.png)
    - sass
      - ![image-20240607000516890](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000516890-58f4a1.png)
      - ![image-20240607000506502](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000506502-f66795.png)

- - 媒体查询

  - - less

      - ![image-20240607000456017](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000456017-0c13fb.png)

    - sass

    - - 和less是一样的

  - 条件

  - - less
      - ![image-20240607000446797](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000446797-49a1c6.png)
    - sass
      - ![image-20240607000437650](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000437650-bca23f.png)

- - 循环

  - - less
      - ![image-20240607000417958](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000417958-969ecc.png)
    - sass
      - ![image-20240607000403624](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000403624-97fee5.png)

  - 导入

  - - less
      - ![image-20240607000353022](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000353022-b6cf74.png)
    - sass
      - ![image-20240607000333271](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607000333271-20c36d.png)

![幻灯片6](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%876-91d47d.png)

![幻灯片7](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%877-100004.png)

**postCSS**

官网地址：https://postcss.org/

主要使用的就是这个网站的插件：

![image-20240606234653343](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606234653343-2a6d61.png)

![幻灯片8](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%878-292e8f.png)

**css架构文件分配**

![image-20240606234451909](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606234451909-0b1125.png)

![幻灯片9](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%879-ae5a8c.png)

![幻灯片10](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8710-bdcadc.png)

![幻灯片11](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8711-716b48.png)

**shapes**

- shape-outside: margin-box;
  - ![image-20240606234535781](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606234535781-a2589f.png)
- shape-outside: border-box;
  - ![image-20240606234550596](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606234550596-52c5ee.png)
- shape-outside: content-box;
  - ![image-20240606234600067](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606234600067-968392.png)
- padding-box:内边距环绕
  - ![image-20240606234612461](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606234612461-11ebd3.png)

![幻灯片12](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8712-5401a3.png)

**自定义滚动条**

- 默认的样式
  - ![image-20240606234342372](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606234342372-80558f.png)
- 滑动块
  - ![image-20240606234357625](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606234357625-01fe7f.png)
- 滑道
  - ![image-20240606234409275](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240606234409275-cd02df.png)

![幻灯片13](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8713-a3d7c7.png)

![幻灯片14](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8714-a0092e.png)