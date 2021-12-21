1. html5 新增的一些语义化标签:
    - header  头部标签
    - nav     导航标签
    - article 内容标签
    - section 定义文档某个区域
    - aside   侧边栏标签
    - footer 尾部标签
    - 注意事项:
        - 这些语义化标签主要是针对搜索引擎的
        - 在IE9中 需要把这些标签转换为块级元素

2. 视频标签 video
   - video标签支持 MP4 WebM  Ogg三种视频格式, 照顾兼容性, 尽量使用mp4格式的
   - `<video src='文件地址' autoplay='autoplay' muted='muted' controls='controls' loop='loop' poster='等待视频加载的时候的图片' width='xxpx' height='xxpx'></video>`
   - 谷歌浏览器默认禁止自动播放 可以添加muted属性解决不能自动播放的问题

3. 音频标签 audio
    - audio支持三种音频格式mp3 wav ogg 照顾兼容性 使用MP3
    - `<audio src='音频地址' autoplay='autoplay' controls='controls' loop='loop'></audio>`
4. h5新增inpu表单
    - `type='email | url | date | time | month | week | number | tel | search | color'`
5. h5新增表单属性
    - `required = 'required'` 表示必填不能为空
    - `placeholder = 'xxxxxx'` 表单的提示信息, 存在默认值将不显示(鼠标点击后修改就显示修改的文本, 删掉修改的文本后默认值又会显示出来)
        - 修改placeholder文本的默认样式, 可以使用
            ```
            input::placeholder {
                color:pink;
            }
            ```
    - `autofocus = 'autofocus'` 自动聚焦属性,  表示页面加载完成后 鼠标焦点自动定在这个属性所在的标签上
    - `autocomplete = 'off | on'`  当用户开始键入时, 浏览器基于之前键入过的值, 显示出之前在这里件如果的值.
        - 含有这个属性的标签需要放在表单内, 且这个标签要加上name属性, 且表单提交成功
        - 默认是打开的on,  一般我们都会选择off关闭, 防止隐私泄露
    - `multiple = 'multiple'` 用在type=file的表单元素内, 表示选择文件的时候可以多选 
