1. 精灵图sprite
    - 目的：有效减少服务器接收和发送请求的次数，提高页面的加载速度
    - 原理： 将页面上小的背景图片正和岛一张大图上， 这样服务器只需要一次请求就行了
    - 使用`background-position`属性精确移动背景位置到需要显示的小图那里即可, 一般精灵图都是向左或者向上移动, 所以这个数值一般是负值
    - 缺点: 精灵图一旦做好要是替换比较麻烦,图片本身还是比较大的, 图片本身放大和缩小会失真
2. 字体图标 iconfront
    - 一个图标要比一系列的图片要小, 一旦字体加载了,图片马上就会渲染出来,减少了服务器请求
    - 字体图标本质是文字, 可以随意的改变颜色,产生阴影,透明效果,旋转等
    - 但是 字体图标不能替代精灵图,只是对工作中图标部分的优化和提升
        - 如果是结构和样式简单的小图标就用字体图标
        - 如果是结构和样式比较复杂的小图标,就用精灵图
    - 2.1 字体图标的下载
        - iconmoon字库
        - 阿里iconfront字库
    - 2.2 字体图标的引入
        - 把2.1中下载下来的字体文件解压后里面的font文件夹放到项目的目录下
        - 使用`@font-face{font-family: 'iconmoon'; src: url('fonts/iconmoon.eot').....}`声明字体图标,  一定要注意字体图标的路径问题, 引入字体声明的语句可以在2.1中下载的文件style.css中拷贝
        - 使用: 打开2.1中下载的文件中的demo.html文档, 选中想用的图标的最右边的矩形框,复制到要使用这个字体图标的标签中, 然后再给这个标签的样式里面增加字体声明`font-family: icomoon;`即可, 后面可以修改这个标签的大小眼色对齐方式等等,跟字体是一样的
    - 2.3 字体图标的追加
        - 把2.1中下载的文件中的selection.json文件上传到icomoon网站中 选择想要追加的图标 点击下载压缩包 替换原来的文件即可
        


