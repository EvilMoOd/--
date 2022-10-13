letter-spacing字与字间距。

**`white-space`** CSS 属性是用来设置如何处理元素中的 [空白 (en-US)](https://developer.mozilla.org/en-US/docs/Glossary/Whitespace)。

writing-mode 属性定义了文本在水平或垂直方向上如何排布。

```
writing-mode: horizontal-tb | vertical-rl | vertical-lr | sideways-rl | sideways-lr
```

- horizontal-tb：水平方向自上而下的书写方式。即 left-right-top-bottom
- vertical-rl：垂直方向自右而左的书写方式。即 top-bottom-right-left
- vertical-lr：垂直方向内内容从上到下，水平方向从左到右
- sideways-rl：内容垂直方向从上到下排列
- sideways-lr：内容垂直方向从下到上排列

### 伪类

（1）a:link（未访问过的链接）

（2） a:hover（鼠标经过，也就是鼠标指针放在该元素上时）

 （3）a:active（当前激活链接,也就是点击鼠标左键时）  

（4）a:visited（已访问过）

### 各种自适应

自适应屏幕最小宽度600px值时

```css
@media screen and (min-width: 600px) 
```

当块的宽度固定设置为width时，屏幕尺寸小于width会出现滚动条

当设置为max-width时将不会有滚动条，块级元素会自适应调整大小

图片剪切适应：如果我们使用 object-fit: cover;，它会剪切图像的侧面，保留长宽比，并填充空间，如下所示

object-fit 属性可接受如下值：

- fill - 默认值。调整替换后的内容大小，以填充元素的内容框。如有必要，将拉伸或挤压物体以适应该对象。
- contain - 缩放替换后的内容以保持其纵横比，同时将其放入元素的内容框。
- cover - 调整替换内容的大小，以在填充元素的整个内容框时保持其长宽比。该对象将被裁剪以适应。
- none - 不对替换的内容调整大小。
- scale-down - 调整内容大小就像没有指定内容或包含内容一样（将导致较小的具体对象尺寸）

### 垂直居中

1、可以给父级使用相对定位，子级使用绝对定位并margin:auto;，将top、left、right、bottom为0

2、给父级和子级都加绝对定位，再给子级添加top：calc（50% - 子级元素高度一半）left：calc（50% - 子级元素宽度一半）

3、 给父级相对定位,子级绝对定位：left：50%；top：50%；
margin-left：-子级元素宽度一半；
margin-top：-子级元素高度一半

4、 给父级一个display：flex； align-items：center；
再给子级添加：margin：0 auto；

### Flex

https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-align-content

#### 父级设置

- `row`（默认）：从左到右`ltr`；从右到左`rtl`
- `row-reverse`：从右到左`ltr`；从左到右`rtl`
- `column`: 相同，`row`但从上到下
- `column-reverse`: 相同，`row-reverse`但从下到上

```css
.container {
  flex-direction: row | row-reverse | column | column-reverse;
}
```

- `nowrap` （默认）：所有弹性项目都将在一行
- `wrap`: flex 项目将从上到下包裹到多行。
- `wrap-reverse`: flex 项目将从下到上换行成多行。

```css
.container {
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```

上面两个可以简写成    flex-flow：row norap；

##### justify-content

![image-20220128185231347](C:\Users\1\AppData\Roaming\Typora\typora-user-images\image-20220128185231347.png)

- `flex-start` （默认）：项目被打包朝向 flex-direction 的开始。
- `flex-end`: 项目被打包到 flex-direction 的末尾。
- `start`: 物品被包装在方向的开始处`writing-mode`。
- `end`: 物品被包装到方向的尽头`writing-mode`。
- `left`: 物品被包装在容器的左边缘，除非这对 . 没有意义，否则`flex-direction`它的行为就像`start`.
- `right`: 物品被包装在容器的右边缘，除非这对 . 没有意义，否则`flex-direction`它的行为就像`end`.
- `center`：项目沿线居中
- `space-between`：物品均匀分布在行中；第一项在起始行，最后一项在结束行
- `space-around`：项目均匀分布在行中，周围空间相等。请注意，视觉上的空间是不相等的，因为所有项目的两边都有相等的空间。第一个项目将在容器边缘有一个空间单位，但下一个项目之间有两个空间单位，因为下一个项目有自己的适用间距。
- `space-evenly`：项目分布使得任何两个项目之间的间距（以及边缘的空间）相等。

```css
.container {
  justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly | start | end | left | right ... + safe | unsafe;
}
```

##### align-items

![image-20220128185607182](C:\Users\1\AppData\Roaming\Typora\typora-user-images\image-20220128185607182.png)

- `flex-start` （默认）：项目被打包朝向 flex-direction 的开始。
- `flex-end`: 项目被打包到 flex-direction 的末尾。
- `start`: 物品被包装在方向的开始处`writing-mode`。
- `end`: 物品被包装到方向的尽头`writing-mode`。
- `left`: 物品被包装在容器的左边缘，除非这对 . 没有意义，否则`flex-direction`它的行为就像`start`.
- `right`: 物品被包装在容器的右边缘，除非这对 . 没有意义，否则`flex-direction`它的行为就像`end`.
- `center`：项目沿线居中
- `space-between`：物品均匀分布在行中；第一项在起始行，最后一项在结束行
- `space-around`：项目均匀分布在行中，周围空间相等。请注意，视觉上的空间是不相等的，因为所有项目的两边都有相等的空间。第一个项目将在容器边缘有一个空间单位，但下一个项目之间有两个空间单位，因为下一个项目有自己的适用间距。
- `space-evenly`：项目分布使得任何两个项目之间的间距（以及边缘的空间）相等。

```CSS
.container {
  align-items: stretch | flex-start | flex-end | center | baseline | first baseline | last baseline | start | end | self-start | self-end + ... safe | unsafe;
}
```

##### align-content

![image-20220128185918749](C:\Users\1\AppData\Roaming\Typora\typora-user-images\image-20220128185918749.png)

- `normal`（默认）：项目被打包在它们的默认位置，就好像没有设置值一样。
- `flex-start`/ `start`：包装到容器开头的物品。（更受支持的）`flex-start`尊重，`flex-direction`而`start`尊重`writing-mode`方向。
- `flex-end`/ `end`：包装到容器末端的物品。（更多支持）`flex-end`尊重，`flex-direction`而端尊重`writing-mode`方向。
- `center`：在容器中居中的项目
- `space-between`：项目均匀分布；第一行在容器的开头，最后一行在结尾
- `space-around`：项目在每行周围均匀分布
- `space-evenly`：项目均匀分布，周围空间相等
- `stretch`: 线条伸展以占用剩余空间

```css
.container {
  align-content: flex-start | flex-end | center | space-between | space-around | space-evenly | stretch | start | end | baseline | first baseline | last baseline + ... safe | unsafe;
}
```

##### gap

![image-20220128190138045](C:\Users\1\AppData\Roaming\Typora\typora-user-images\image-20220128190138045.png)

#### 子级设置

order控制顺序

flex-grow控制块比例

flex-shrink与上面相反

```CSS
.item {
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}//设置单个子块
```

#### 用浮动来写三栏布局记得代码顺序要是先浮动

#### bfc

1、position：absolute

2、display：inline-block

3、float

4、overflow：hidden

#### 子元素浮动，父元素要清除浮动

1、clear：both

2、bfc

3、伪元素

```css
span::after{
    content:"";
    clear:both;
    display:block;
}
```

#### 设置position：absolute，float会在内部把元素转换成inline-block

#### float解决容器包裹字体

#### 溢出容器解决

```CSS
while-space:nowrap;
overflow:hidden;
text-overflow:ellipsics;
```
