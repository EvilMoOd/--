+ meta常用于定义页面的说明，关键字，最后修改日期，和其它的元数据。这些元数据将服务于浏览器（如何布局或重载页面），搜索引擎和其它网络服务。

+ 表单校验元素将可以通过 CSS 伪类 [`:valid`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:valid) 进行特殊的样式化；

+ form表单required属性表示不能为空，pattern=“ ” 属性则规定指定内容，minlength / maxlength规定text长度,max min规定number

+ 当用户选择该label标签时，浏览器就会自动将焦点转到和标签相关的表单不过是面向来临时的方向，小编渡过时光的荒芜搁浅。

+ 垂直居中效果要在标签的父级写，你个笨蛋

![image-20220128111634582](C:\Users\1\AppData\Roaming\Typora\typora-user-images\image-20220128111634582.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style type="text/css">
        header{

        }
    </style>
</head>
<body>
    <!-- 头部 -->
    <header>
        <!-- 头部标题 -->
        <h1>HTML5时代</h1>
        <!-- 头部标题end -->

        <!-- 导航 -->
        <nav>
            <ul>
                <li>
                    <a href="#">首页</a>
                </li>
                <li>
                    <a href="#">活动</a>
                </li>
                <li>
                    <a href="#">话题</a>
                </li>
                <li>
                    <a href="#">社区·</a>
                </li>
            </ul>
        </nav>
        <!-- 导航end -->

    </header>
    <!-- 头部end -->

    <!-- 部分片段section -->
    <!-- 介绍 -->
    <section id="idea">
        <div>
            <h2>HTML5时代</h2>
            <p>通过我们的 HTML 编辑器，您能够编辑 HTML，然后点击按钮来查看结果。</p>
        </div>
    </section>
    <!-- 介绍end -->
    <!-- 活动幻灯片 -->
    <section id="activity">
        <!-- 活动上部 -->
        <div class="up">
            <!-- 活动区域日历控件 class命名为左侧 -->
            <div id="calendar" class="left_part"></div>
            <!-- 活动区域日历控件end class命名为左侧 -->
            <!-- 右侧 信息info -->
            <div id="info" class="right_part">
                <!-- 公告bulletin -->
                <div id="bulletin">
                    <!-- 公告标题 -->
                    <h3>公告栏</h3>
                    <!-- 公告标题 end -->
                    <p>输入替换内容后，替换所有匹配关键字。(NOTE: 注意此时如果鼠标焦点在编辑窗口中</p>
                </div>
                <!-- 公告bulletin end -->
            </div>
            <!-- 右侧 信息info end -->
        </div>
        <!-- 活动上部end -->

        <!-- 活动下部 -->
        <div class="dowm">
            <h3>发现活动</h3>
            <!-- 活动区域轮播图控件 -->
            <div id="act_slides"></div>
            <!-- 活动区域轮播图控件end -->
        </div>
        <!-- 活动下部end -->
    </section>
    <!-- 活动幻灯片end -->

    <!-- 正文部分 -->
    <section id="post">
        <h3>社区文章</h3>
        <!-- 左侧 -->
        <article id="posts">
            <applet class="item">
                <figure>![](http://upload-images.jianshu.io/upload_images/3877962-9b88174b25a2a31c.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)</figure>
                <div class="header">
                    <h4>
                        <a href="#" title="常用表达式">常用表达式</a>
                        <span>作者:黄继鹏<time>2017-10-12 19:05</time></span>
                    </h4>
                </div>
                <div class="body"></div>
                <div class="footer"></div>
            </applet>
        </article>
        <!-- 左侧end -->

        <!-- 右侧 -->
        <article id="others"></article>
        <!-- 右侧end -->
    </section>
    <!-- 正文部分end -->

    <!-- 部分片段section end -->

    <!-- 页脚 -->
        <footer>
            <ul></ul>
            <address></address>
        </footer>
    <!-- 页脚end -->
</body>
</html>
```
