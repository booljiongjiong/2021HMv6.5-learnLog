1. 鼠标样式 cursor
    - `cursor: default|pointer|move|text|not-allowed;
2. 取消表单边框
    - `outline: 0|none;` 可以取消表单元素比如输入框,文本域等的蓝色边框线
3. 取消文本域的拖拽
    - `resize: none;` 取消文本域的拖拽功能
    - 一般文本域`<textarea name='' id='' cols='30' rows='20'></textarea>`这样写没有问题 但是如果首尾标签之间用换行了就会造成文本域内容跟边缘有一定的距离 所以为了避免这种情况出现 一般`<textarea>`和`</textarea>`写在一行上,不要写成换行模式
4. 使用vertical-align把行内元素|行内块元素和文字垂直对齐
    - `vertical-align: base-line|top|middle|bottom`
    - 使用场景1: 用在把图片|表单元素和文字垂直居中对齐 `img{ vertical-align: middle;}`
    - 使用场景2:
        - 图片(行内块元素)因为默认是基线对齐, 所以图片(行内块元素)一般底部都会有一个空白缝隙
            - 解决方案1: 给图片添加`vertical-align: bottom|middle|top;`三者中的一个恰当选取使用即可 ----- `推荐使用`
            - 解决方案2: 给图片转成块级元素`display: block;` -------- 不太推荐使用, 因为把图片转成块元素 可能会影响后面的元素布局 比如原来图片后面还有其他行内块元素的话 别的行内块元素就会被挤掉到下一行去, 但是如果这个图片的父元素只有图片自己一个子元素,这个方法倒是没什么顾虑了
5. 一行文本溢出显示省略号
    - ```
        .txt {
            white-space: nowrap;        //不允许换行, 只能在一行显示
            overflow: hidden;           //溢出的部分隐藏
            text-overflow: ellipsis;    // 文字溢出的时候用省略号显示
            }
      ```
6. 多行文本溢出显示省略号
    - ```
        overflow: hidden;
        text-overflow: ellipsis;
        display: -webkit-box;        //弹性伸缩盒子模型显示
        -webkit-line-clamp: 2;       //限制在一个块元素显示的文本的行数, 一般都会控制好这个多行文本的父块元素的宽高,所以这个2一般也代表着在第几行显示省略号
        -webkit-box-orient:vertical; //设置或检索伸缩盒子的子元素的排列方式
      ```
      - 这个方法有兼容性问题, 一般适应webkit浏览器或者移动端(因为移动端浏览器大部分是webkit内核)
