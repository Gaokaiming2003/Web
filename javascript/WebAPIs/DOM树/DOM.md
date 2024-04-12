# DOM

## DOM对象

浏览器根据html标签生成的js对象。

## 获取DOM对象

```javascript
// 选择匹配的第一个元素
document.querySelector('div')
```

### 根据css选择器来获取DOM对象

```javascript
document.querySelector('div') // 选择第一个div元素  可以直接修改
document.querySelectorAll('div') // 选择所有div元素 只能遍历修改
// 得到的是一个伪数组，没有push和pop方法
```

```javascript
// id选择器
document.querySelector('#id')
// 类选择器
document.querySelector('.box')
```

## 修改DOM对象

```javascript
// 先获取DOM对象
const box = document.querySelector('.box')

box.innerText = 'new text' // 修改文本内容, 不解析内部标签
box.innerHTML = '<p>new html</p>' // 修改innerHTML, 会解析内部标签
```

### 操作常用元素属性

```javascript
对象.属性 = 值

const img = document.querySelector('img')
img.src = 'https://example.com/image.jpg' // 修改图片src属性
img.alt = 'image description' // 修改图片alt属性
```

### 操作元素样式属性

```javascript
对象.style.属性 = 值
```

### 通过类名修改样式

```javascript

对象.className = 'box' // box是类名
```

### 操作表单元素

## 自定义属性

```javascript
/* 以data-开头的属性为自定义属性 */
<div data-name="John"></div>

const div = document.querySelector('div')
div.dataset.name // "John"
```

## 定时器

```javascript
**<!-- 倒计时 -->
<!-- 开启定时器 -->
<!-- setInterval(函数, 间隔时间) -->
<!-- 每隔一段时间执行一次函数 -->
<!-- 间隔时间单位为毫秒 -->
<!-- 返回一个定时器的ID, ID会改变所以用let定义 -->
<!-- 关闭定时器 -->
<!-- clearInterval(定时器ID) -->
<body>
    <script>
        let timer_id = setInterval(function() {document.write("123")}, 1000)
        console.log(timer_id)
        clearInterval(timer_id)
    </script>
</body>
```

## 事件

### 事件监听

```javascript
对象.addEventListener('事件类型', 回调函数)

事件源：哪个DOM对象触发的事件
事件类型：鼠标点击、鼠标移动、键盘按下、页面加载完成等
回调函数：当事件发生时执行的函数
```

### 事件类型

* 鼠标事件: 鼠标触发
  * click
  * mouseenter
  * mouseleave
* 焦点事件：表单获得光标
  * focus
  * blur
* 键盘事件:键盘触发
  * keydown
  * keyup
* 文本事件：表单输入触发
  * input

## 事件对象

有事件触发时的相关信息

* 可以判断用户按下哪个键
* 可以判断鼠标点击了哪个元素

### 获取事件对象

```javascript
元素.addEventListener('click', function(e){})
```

### 常用属性

* type
* clientX/clientY
* offsetX/offsetY
* key

```javascript
trim方法：去除字符串两侧的空格
```

## 环境对象

指的是函数内部特殊的变量this,它代表着当前函数运行时所处的环境
每个函数内部都有一个this

## 回调函数

如果将函数A作为参数传递给函数B时，我们称函数A为回调函数

```javasript
function fn() {
  console.log('  w')
}
setInterval(fn, 1000)
```

## 事件流

事件流指的是事件完整执行过程中的流动路径

* 捕获阶段
* 冒泡阶段

### 事件捕获

从DOM的根元素开始去执行对应的事件(从外到里)(从大到小)

`DOM.addEventListener(事件类型,事件处理函数, 是否使用捕获机制)`
第三个参数：false代表冒泡阶段触发，默认是false

son -> father -> grandfa

### 事件冒泡

当一个元素触发事件后，会依次向上调用所有父级元素的同名事件

grandfa -> father -> son

### 阻止冒泡

`事件对象.stopPropagation()` 阻止传播

### 事件解绑

`addEventListener方式使用removeEventListener(事件类型，事件处理函数，[获取捕获或者冒泡])`

## 鼠标经过事件

* mouseover和mouseout会有冒泡效果
* mouseenter和mouseleave没有冒泡效果(推荐)

## 事件委托