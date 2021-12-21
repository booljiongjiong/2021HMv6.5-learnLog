1.  
    ```
    img {
        border: 0;                  //照顾低版本浏览器, 如果图片外面包含了连接会有边框的问题
        vertical-align: middle;     //取消图片底测有空白缝隙的问题
    }
    ```

2.
    ```
        .clearfix:after {
            visibility: hidden;
            clear: both;
            diaplay: block;
            content: ".";
            height: 0;
        }
        .clearfix {
            *zoom: 1;
        }
    ```
