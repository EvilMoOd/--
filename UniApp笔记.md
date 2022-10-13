div 改成 view
span、font 改成 text
a 改成 navigator
img 改成 image
input 还在，但type属性改成了confirmtype
form、button、checkbox、radio、label、textarea、canvas、video 这些还在。
select 改成 picker
iframe 改成 web-view
ul、li没有了，都用view替代
audio 不再推荐使用，改成api方式，背景音频api文档
其实老的HTML标签也可以在uni-app里使用，uni-app编译器会在编译时把老标签转为新标签，比如把:div编译成view。但不推荐这种用法，调试H5端时容易混乱。0.

nvue就业场景：

1、更好的区域长列表或瀑布流滚动

2、更好的下拉刷新

3、左右滚动长列表

4、实现区域滚动长列表+左右拖动列表+吸顶的复杂排版效果

5、需要将软键盘右下角按钮文字改为“发送”

6、用到map、video、vive-pusher

7、启动速度优化
