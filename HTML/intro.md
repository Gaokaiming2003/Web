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

