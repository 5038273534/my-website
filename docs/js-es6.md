---
sidebar_position: 4
---

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
