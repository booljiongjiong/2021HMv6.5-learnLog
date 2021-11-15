1. display
    - `display: block;` 设置这个属性有时候可能不仅仅是为了转换成块元素， 同时也可能是为了显示元素用的
    - `display: none;` 设置这个属性后 元素不可见， `且不再占有原先的位置`
2. visibility
    - `visibility: visible;` 设置元素可见
    - `visibility: hidden;` 设置元素不可见， `且还是会占有原先的位置`
3. overflow
    - `overflow: visible;` 不管内容超不超出盒子范围 都显示
    - `overflow: hidden;` 超出盒子范围的内容被隐藏
    - `overflow: auto;` 只有超出盒子范围了才会在超出范围的方向上添加滚动条
    - `overflow: scroll;` 不管内容超不超出盒子范围 都显示滚动条
    - 3.1 `如果是使用了定位的盒子 要慎重使用overflow: hidden, 因为有可能会把特地设置边偏移超出盒子范围的部分隐藏掉`