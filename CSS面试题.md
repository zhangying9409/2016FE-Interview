# CSS面试题

1. [介绍一下CSS的盒子模型？](#1)

2. [CSS3有哪些新特性？](#2)

3. [如何居中div？如何居中一个浮动元素？](#3)

4.[如何清除浮动？](#4)

<a name="1"></a>
**1.介绍一下CSS的盒子模型？**

（1）有两种， IE 盒子模型、标准 W3C 盒子模型；IE的content部分包含了 border 和 pading;
（2）盒模型： 内容(content)、填充(padding)、边界(margin)、 边框(border).

<a name="2"></a>
**2.CSS3有哪些新特性？**

   CSS3实现圆角（border-radius:8px），阴影（box-shadow:10px），
   对文字加特效（text-shadow、），线性渐变（gradient），旋转（transform）
   transform:rotate(9deg) scale(0.85,0.90) translate(0px,-30px) skew(-9deg,0deg);//旋转,缩放,定位,倾斜
   增加了更多的CSS选择器  多背景 rgba

<a name="3"></a>
**3.如何居中div？如何居中一个浮动元素？**

给div设置一个宽度，然后添加margin:0 auto属性
```css
 div{
     width:200px;
     margin:0 auto;
  }
```
居中一个浮动元素，确定容器的宽高 宽500 高 300 的层，设置层的外边距
```css
  .div {
   width:500px ; height:300px;//高度可以不设
   margin: -150px 0 0 -250px;
   position:relative;相对定位
   background-color:pink;//方便看效果
   left:50%;
   top:50%;
 }
```
<a name="4"></a>
**4.如何清除浮动？**
(1).clear:both;
```
div{
    float:left;
    clear:both;
}
```
(2).after 方法
```
.outer {
    zoom:1; /*zoom: 1;for IE6/7 Maxthon2*/
}
.outer :after {
    clear:both;
    content:".";
    display:block; /*for FF/chrome/opera/IE8*/
    width: 0;
    height: 0;
    visibility:hidden;
    }
```
(3).设置父级div定义 overflow: auto;
