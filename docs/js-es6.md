---
sidebar_position: 4
---





### es6 模块化
```javascript
默认暴露

// 默认暴露可以是任何类型
// 默认暴露在文件里只能一个
export default {} 
import module from ''

```

### document
```javascript
document.querySelector()
document.querySelectorAll()
// 父类
.parentNode
let li = `<li></li>`
document.querySelector('ul').insertAdjacentHTML('beforeend',li)
// 阻止冒泡
e.stopPropagation()
// 双击禁止选定文字
window.getSelection ? window.getSelection().removeAllRanges():document.selection.empty()
```

### JSON

```javascript
let obj = [{a:1,b:2},{c:3,d:4}];
JSON.stringify(obj); // 对象转json字符串，结果：'[{"a":1,"b":2},{"c":3,"d":4}]'  
JSON.parse('[{"a":1,"b":2},{"c":3,"d":4}]'); // json字符串转对象 
```

### async
1. 返回一个 Promise 对象
2. 返回的结果不是一个 Promise 对象，则返回就是一个成功的promise
3. 返回 throw new Error() 则返回就是一个失败的promise
   
```javascript
const res = async function fn(){
    return 'promise' 
}
console.log(res())
Promise {<fulfilled>: 'promise'}
```

### Date

- 学习网址：<https://mp.weixin.qq.com/s?__biz=MjM5MDA2MTI1MA==&mid=2649121025&idx=2&sn=aff0bf6598f07e6b93f20134b1cfac89&chksm=be5846ac892fcfba7a9c382850cf8783d54d4fe8498843b14957d2bba79fdf39f6cd640c66f5&scene=27>
   
```javascript
// 得到时间戳
Date.now()
Date.parse(new Date()) 
Date.parse("2022/1/18 10:05") 
new Date().getTime()


// 格式化
function getLocalTime(n) {   
   return new Date(parseInt(n)).toLocaleString().replace(/:\d{1,2}$/,'');   
}   
getLocalTime(1642471746435)  // '2022/1/18 10:09'

function  getLocalTime(n){
   return new Date(parseInt(n)).toLocaleString().replace(/年|月/g, "-").replace(/日/g, " ");
}
getLocalTime  (1642471746435) // '2022/1/18 10:09:06'

function getData(n){
  n=new Date(n)
  return n.toLocaleDateString().replace(/\//g, "-") + " " + n.toTimeString().substr(0, 8)
}
getData(1642471746435) // '2022-1-18 10:09:06'


```






## 注意
### 深浅拷贝 
```javascript
// 深拷贝
let a = {a:1,b:2}
let b= {a:5,c:6}
let c = {...a,...b}
Object.assign(a, b)

```

### 回调地狱
```javascript

```









```javascript
let person ={
    name:'张三'
}
Object.defineProperty(person,'age',{
    value:18,
    enumerable:true, //默认false,控制是否可枚举
    writable:true,//默认false,控制是否可以修改
    configurable:true,//默认false,控制是否能删除
    get(){

    },
    set(value){}

})

Object.keys(person) //返回对象key值列表数组




```
