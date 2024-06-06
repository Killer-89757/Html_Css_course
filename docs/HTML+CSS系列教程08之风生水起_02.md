# HTML+CSS系列教程08之风生水起_02

![幻灯片2](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%872-4e045b.png)

![幻灯片3](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%873-f76c87.png)

![幻灯片4](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%874-2e8aed.png)

![幻灯片5](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%875-98e282.png)

media

- 当屏幕的大小小于500的时候，展示默认的样式；当屏幕的大小大于500的时候，展示media中设置的样式

  - ```css
    @media all and (min-width: 500px){
        #box1{background-color:hotpink;}
    }
    ```

  - ![image-20240607001548175](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607001548175-3532d1.png)

  - ![image-20240607001556049](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607001556049-bcc80c.png)

- 横屏和竖屏

- - orientation:portrait

  - - 横屏

  - orientation:landscape

  - - 竖屏

- link的形式

- - `<link rel="stylesheet" href="base.css" media=" all and (min-width:400px) ">`

  - - 当屏幕的最小width是400px的时候加载的是base.css

  - `<link rel="stylesheet" href="base2.css" media=" all and (min-width:600px) ">`

  - - 当屏幕的最小width是600px的时候加载的是base2.css

- 注：响应式代码写到要适配的CSS后面。

- ![image-20240607001527542](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2Fimage-20240607001527542-2e4839.png)

![幻灯片6](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%876-ee0e0b.png)

![幻灯片7](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%877-1e78d8.png)

![幻灯片8](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%878-2a3dc7.png)

![幻灯片9](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%879-639ecf.png)

![幻灯片10](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8710-610f22.png)

![幻灯片11](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F06%2F%E5%B9%BB%E7%81%AF%E7%89%8711-ebbf25.png)