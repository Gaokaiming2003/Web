# CSS

## What is css?

CSS(Cascading Style Sheets, 层叠样式表),为 web 内容添加样式的代码.

## An example

```css
p {
    color: red;
}

```

`p`: Selector\
`color`: property\
`red`: property value\
`color: red`: Declaration

整个结构称为**规则集**

### 选择器(Selector)

    html元素的名称位于规则集开始。它选择了一个或多个需要添加样式的元素。

### 声明(Declaration)

    一个单独的规则，用来指定添加样式元素的属性。

### 属性(Properties)

    改变HTML元素样式的途径。

### 属性的值

    在属性的右边，冒号后面即属性的值。

### tips

#### 每一个声明后必须接一个分号

```css
p {
  color: red;
  width: 500px;
  border: 1px solid black;
}
```

#### 可以选择多种类型的元素并为它们添加一组相同的样式。

用逗号分开

```css
p,
li,
h1 {
  color: red;
}
```

### 不同类型的选择器

