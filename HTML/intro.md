# 什么是HTML

HTML（HyperText Markup Language，超文本标记语言）是一种用来告知浏览器如何组织页面的标记语言。

## an example

```html
<!doctype html> <!--声明文档类型-->
<html lang="zh-CN"> <!--<html>元素。包括了页面中的所有内容-->
  <head>          <!--<head>元素，这个元素是一个容器，包含了所有想在html页面中包含但不在html页面中显示的内容。-->
    <meta charset="utf-8" />   <!--<meta>元素。这个元素代表了不能由其他html元相关元素表示的元数据。-->
    <title>我的测试站点</title> <!--标题-->
  </head>
  <body> <!--<body>包含了你访问页面时所有显示在页面上的内容，包含文本、图片、视频、游戏、可播放音频轨道等等。-->
    <p>这是我的页面</p>
  </body>
</html>
```

## 特殊字符

| 原义字符 | 等价字符引用 |
| -------- | ------------ |
| <        | `&lt;`         |
| >        | `&gt;`       |
| "        | `&quot;`       |
| '        | `&apos;`       |
| &        | `&amp;`        |

## 框架

框架标签是一种与网页布局密切相关的标签，通过使用框架，可以在同一个浏览器窗口显示多个页面。

### \<frameset>

* cols 属性 定义框架集中的列数目和尺寸
* rows 属性 定义框架集中的行数目和尺寸
* border 属性 设置框架边框的宽度
* bordercolor 属性 设定框架边框的颜色

两者的取值单位可以是像素（绝对大小），可以是百分比（相对大小），也可以是*（表示除了以划分部分的尺寸后剩余的尺寸）。

注意：使用 frameset 标签时不能写在 body 标签内，否则容易无效。

### \<noframes>

为那些不支持框架的浏览器显示替代文本。即当浏览器不能处理框架时，就会显示该元素中的文本，这些文本包含在\< body \>元素中。

```html
<frameset>
  <noframes>
      <body>
      </body>
  </noframes>
<frameset>
```

### \< frame >  框架标签

`<frame name="f1" src="a.html"scrolling="auto noresize="noresize"/>
`

* src 属性 设置框架中要显示的网页的URL地址
* name 属性 设置框架名称、来唯一标识框架
* scrolling 属性 设置框架是否显示滚动条，属性值可为：yes、no、auto
* noresize 属性 设置是否可以调整窗口大小，属性值只可取：noresize

使用超链接中的target属性来控制框架跳转显示.

超链接< a >元素中的target属性可以设置在何处打开链接页面，有五个取值：

* _blank：在新窗口中打开目标文=文档
* _self：在当前框架或窗口打开目标文档，默认值
* _parent：在父框架集中显示被打开的目标文档
* _top：跳出所有框架集，在整个窗口中打开目标文档
* 框架名称：在指定框架中打开目标文档

### \<iframe>

< iframe >是一种可以嵌在网页中任意部分的框架形式，也称为浮动框架。

`<iframe src="aa.html" id="iframe1" width="100" height="100" frameborder="1" scrolling="auto"></iframe>
`

* src 设置框架中要显示的网页的URL地址
* id 用于唯一标识 iframe 框架
* width 设置浮动框架的宽度
* height 设置浮动框架的高度
* frameborder 设置是否显示边框，0 为不显示，1 为显示
* scrolling 设置是否显示滚动条，属性值可为：yes、no、auto

注意：< iframe >标签一般写在 body 标签内，而不是写在框架集标签中.