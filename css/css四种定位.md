1. 定位: 将盒子定在某一位置,   `定位 = 定位模式 + 边偏移`
    - 定位模式指定一个元素再文档中的定位方式, 边偏移则决定了元素最终的位置
    - 定位模式
        - `position: static | relative | absolute | fixed`
    - 边偏移 : 
        - `top: xxpx`
        - `bottom: xxpx`
        - `left: xxpx`
        - `right: xxpx`
2. 静态定位 static
    - 静态定位是元素的默认定位方式, 无定位的意思
    - 静态定位按照标准流特性摆放位置, 没有边偏移
3. 相对定位 relative
    - 相对定位是元素在移动位置的时候, `**相对他自己原来的位置移动的**`
    - 移动后元素原来在标准流里面的位置继续占有, 后面的盒子仍然以标准流的方式对待他 ------------> **不脱标**
    - 总结: **不脱标, 继续占有原来位置**
4. 绝对定位 absolute
    - 绝对定位是元素在移动的时候 相对于他的祖先元素位置的
    - 如果绝对定位元素没有祖先元素或者祖先元素没有定位, 则以浏览器为参考定位(Document文档)
    - `如果祖先元素有定位(相对定位 绝对定位 固定定位), 则以最近一级的有这三种定位之一的祖先元素为参考进行移动`
    - 绝对定位的元素不再占有他原来的位置,  脱离标准流 ---------------------------------------------------> **脱标**

    - `子绝父相`:
        - 子级绝对定位, 不会占有位置, 可以自由的放在父级盒子的任何地方, 不会影响其他的兄弟盒子
        - 父盒子需要加定位来限制子盒子在父盒子自己的范围进行边偏移
        - 父盒子布局时, 需要占有位置, 因此父盒子只能是相对定位
        - 以上: 就是'子绝父相'的原因. 因此相对定位经常用来作为绝对定位的父级
5. 固定定位 fixed
    - 固定定位是元素固定于浏览器可视区的固定位置, 不会随着滚动条滚动
    - 1. `以浏览器的可视窗口为参照点移动元素`
    - 2. 固定定位不占有自己原来的位置 ----------------------------------------------------------------> **脱标**
    - 小技巧: 以版心盒子右侧为参考进行固定定位
        - 让固定定位的盒子`left: 50%`,  这样走到浏览器可视区的一半位置
        - 再让固定定位的盒子`margin-left:版心宽度一半距离`
        -这样 就可以让固定定位的盒子贴着版心右侧对齐了
6. 粘性定位 sticky
    
