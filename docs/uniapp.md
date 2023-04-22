


官网：https://uniapp.dcloud.net.cn/

开发工具：https://www.dcloud.io/hbuilderx.html

官方教程：https://ke.qq.com/course/3169971#term_id=103296764

微信公众平台：https://mp.weixin.qq.com


[微信小程序开发者工具] [error] 工具的服务端口已关闭。要使用命令行调用工具，请在下方输入 y 以确认开启，或手动打开工具 -> 设置 -> 安全设置，将服务端口开启。
16:15:01.287 [微信小程序开发者工具] - initialize

### 遇到的问题
```css
@import './index.scss'; // 正确引入
@import url('./index.scss'); // 错误引入会报错

```




onInit使用注意

仅百度小程序基础库 3.260 以上支持 onInit 生命周期
其他版本或平台可以同时使用 onLoad 生命周期进行兼容，注意避免重复执行相同逻辑
不依赖页面传参的逻辑可以直接使用 created 生命周期替代


生命周期执行顺序
		
vue 生命周期 	created >  mounted

page 生命周期  onLoad > onReady 
	
created > onLoad >  mounted > onReady