总结一些最近面试的题目
> ### css
#### 1.display 与 visibility 的区别
都可以控制元素显示和隐藏，visibility="visible|hidden|collapse|inherit",visibility设置为隐藏时会占据原来的位置。

#### 2.inline block inline-block的区别
块级元素：独立块，独自占用一行，会单独换行。如：div,form,table,section,ul,p
内联元素：不换行直到一行排满再换行.如：span,a,em,strong,img,lable

* display: block
单独占行，相邻的会自动换行，不管宽高是多少，可以设置margin和padding
* display: inline
不单独占行，相邻元素会排在一行内直到排满，不可以设置宽高，垂直方向上的margin和padding设置无效，水平可以。
* display: inline-block
结合block和inline的同行特性，可以设置宽高和margin，padding，相邻元素会排在一行。

#### 3.box-shadow 和 text-shadow
box-shadow: 5px 5px 5px 20px #000 inset|outset (水平阴影，垂直阴影，模糊距离，阴影大小，颜色，内外阴影)
text-shadow: 1px 1px 1px #000 (水平阴影，垂直阴影，模糊距离，颜色)

