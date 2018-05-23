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
* box-shadow: 5px 5px 5px 20px #000 inset|outset (水平阴影，垂直阴影，模糊距离，阴影大小，颜色，内外阴影)
* text-shadow: 1px 1px 1px #000 (水平阴影，垂直阴影，模糊距离，颜色)

#### 4.浏览器的内核
IE(IE内核) 火狐(Gecko) 谷歌(Webkit) Opear(presto)

#### 5.css选择符有哪些？哪些可以继承？
* 1. ID选择器（#）
* 2. 类选择器（.）
* 3. 标签选择器（div,p）
* 4. 相邻选择器（div+p）
* 5. 子选择器（div>p）
* 6. 后代选择器 (li a)
* 7. 伪类选择器（a:hover,li:after）
* 8. 属性选择器（div[color="red"]）

可继承样式：font-family，font-size,color
不可继承样式：margin,padding,width,height,border

#### 6.水平垂直居中的方法有哪些

* 1.确定宽高，设置位置，设置层的外边距。
```
  div{
    position: absolute|relative;
    height: 300px;
    width: 400px;
    top:50%;
    left:50%;
    margin: -150px 0 0 -200px;
  }
```
* 2. 绝对定位，transform属性
```
  div{
    position: absolute;
    height:100px;
    width:100px;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%)
  }
```
* 3. flex布局
```
  .content{
    display:flex;
    align-items: center;     /* 垂直 */
    justify-content: center;      /* 水平 */
   }
   .content div{
    ...
   }
```
#### 7. 文字超出部分省略号
* 单行
```
overflow:hidden;
text-overflow:ellipsis;
white-space: nowrap;
```
* 多行
```
display:-webkit-box;
-webkit-box-orient:vertical;
-webkit-line-clamp:2;
overflow:hidden;
```
持续更新中...
