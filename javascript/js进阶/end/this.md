# this

## 普通函数

## 箭头函数


## 改变指向

### call()

`fun.call(thisArg,arg1, arg2,...)`

thisArg:在fun函数运行时指定的this值
返回值就是函数的返回值

### apply()

`fun.apply(thisArg, [argArray])`  第二个参数必须是数组

### bind()

bind只改变this指向，不会调用函数

``fun.bind(thisArg, arg1, arg2, ...)`

返回值是一个函数，但是this修改过的函数，原函数的拷贝