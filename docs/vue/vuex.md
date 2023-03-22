---
sidebar_position: 1
---

### 官方资料
- 文档：<https://vuex.vuejs.org/zh/>
- 视屏(英文)：<https://scrimba.com/learn/vuex>

### 学习视屏

### 学习记录
- 最新版本是`Vuex@4.1.0`
- 解决组件之间的传值、数据共享，就是管理数据，数据都是响应式的，能保持组件内容同步
- mutations中更改state的值 



- vuex 使用  
###### 1. 下载到本地或直接CDN引用

```javascript
<script src="https://unpkg.com/vuex"></script>  // 指向最新版
<script src="https://unpkg.com/vuex@2.0.0"></script> // 指定版本
```

###### 2. npm/yarn安装 

```bash
npm install vuex --save

yarn add vuex
```

###### 3. 使用

1. (简单版)，新建`store/index.js`文件
  
```javascript
import Vue from 'vue'
import Vuex from 'vuex'

Vue.use(Vuex)

const store = new Vuex.Store({
    state: {
        count:0,
        user:{
            name:'',
            age:18
        }
    },
    getters: {
        getCount(state){
            return state.count;
        },
        getUser(state){
            return state.user;
        }
    },
    mutations: {
        mUpdateCount(state,count){
            state.count = count;
        },
        mUpdateUser(state,user){
            state.user = user;
        }
    },
    actions: {
        updateCount(context,count){
            context.commit("mUpdateCount",count)
        },
        updateUser(context,user){
            context.commit("mUpdateUser",user)
        }
    }
});
export default store;

/*
    state 数据都是响应式的，
    getters 类似计算属性，对state数据进行包装
    mutations 可以修改state值的方法，是同步的 commit，可以追逐每次修改的数据
    actions 异步,也可以直接修改state的值，但是追踪不到数据的改变
*/

// 注意：组件多数据多，这种方式会造成数据复杂，应该使用模块化，改进如下
// user.js
const user = {
    state: () => ({ ... }),
    getters:{},
    mutations:{},
    actions；{}
}
export default user

// product.js
export default {
    product:{  
        namespaced:true,
        state: () => ({
            list:['1','2']

        }),
        getters:{},
        mutations:{
            add(state,value){
                state.list.push(value)
            }
        },
        actions；{
            addAsync(context,value){
                context.commit('add',value)
            }
        }
    }
}

// 在store/index.js 引入
import Vue from 'vue'
import Vuex from 'vuex'
import user from 'user.js'
import product from 'product.js'

Vue.use(Vuex)

const store = new Vuex.Store({
    modules:{
        user,
        product,
    }
});
export default store;
```

2.在`main.js`引入*.js

```javascript
import store from './store'
// Vue.prototype.$store = store  //这句话不写也能用$store

const app = new Vue({
    ...App,
    store
})
app.$mount()

```

3. 在组件中使用
   
```javascript
import {mapState,mapMutations,mapActions,mapGetters} from 'vuex'

computed：{
        
    // 第一种
    // ...mapState(['count'])  

    // 第二种，可以起个名字  
    ...mapState({
        c:'count'
    }),
    ...mapState('product',['list'])
    ...mapGetters([''])
},
// 注意：同一个state 不能同时 mapSate getters
methods:{
        ...mapMutations('product',['add']),
        ...mapActions('product',['addAsyns'])

}


// 方式一
this.$store.state.count; // 获取值
this.$store.getters.getCount  // 获取值
this.$store.getters.getUser.name // 获取值
this.$store.dispatch('updateCount'.3); // 改变值 dispatch 是请求actions 
this.$store.commit('addAsyns')  // commit 是请求mutations的

```

### 遇到问题

- 数据持久化

    localStorage

### 注意事项