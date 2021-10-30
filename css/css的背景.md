1. 背景颜色:
    - background-color:颜色值
2. 背景图片:
    - 实际开发中常见于logo || 装饰性的小图片 || 超大的背景图片
    - 优点是非常便于控制位置(精灵图也是一种运用场景)
    - `background-image: none | url(url);`
3. 背景平铺:
    - `background-repeat : repeat | no-repeat | repeat-x | repeat-y;`
4. 背景图片位置:
    - `background-position : x y;`
    - 如果 x 和 y是两个值都有 且都是方位名词(top|left|right|bottom|center) 那么这两个顺序无所谓
    - 如果 x 和 y只有一个值, 且是方位名词, 那么根据这个方位名词决定是x还是y 剩下的省略的那个值就是center
    - 如果 x 和 y只有一个值, 且是具体的数值, 那么这个值是x,  y就是center
    - 如果 x 和 y都有值, 但是是混合范单位, 那么第一个是x 第二个是y
5. 背景附着:
    - `background-attachment : scroll | fixed`属性设置背景图像是否固定或者随着页面的其余部分滚动
6. 背景复合写法: 
    - `background: 背景颜色 背景图片 背景平铺 背景图像滚动 背景图片位置`
    - 举个栗子:
        ```
        background: transparent url('cssImg/haha.png') repeat-y fixed top
        ```
    - 这种背景符合写法没有固定顺序 一般约定按照上面的顺序写
7. 背景颜色半透明
    - 举个栗子:
        ```
        background: rgba(120,120,120,.3);//这是一个背景颜色透明度为0.3的盒子 不影响盒子里面的内容
        ```
