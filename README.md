# VueStudy
----
**Vue.js 处理过程**  
+ app.js  
  项目的入口模块，一切的请求，都要先进这里处理  
  （注意：app.js没有路由分发的功能，需要调用router.js模块进行路由分发）
+ router.js  
  路由分发处理模块，为了保证职能单一，他只负责路由，不负责业务逻辑  
  （涉及业务逻辑只能调用**controller模块处理**）
+ controller  
  业务逻辑处理层，封装了一些逻辑代码，不负责数据的**CRUD**（C：create  R：read  U： updata  D： delete）
  （数据的CRUD需要调用model层）  
+ model层  
  职能单一，只负责操作数据库，执行对应sql语句  
+ view视图层  
  每当用户操作了界面，如有业务处理，都会通过网络请求后端服务器，这个请求会被app.js监听到  
  M(保存页面单独数据)  =>  VM(调度者，分割了V,M)  =>  V(每个页面的HTML结构)
+ MVVM  前端视图层分层开发思想，主要把每个页面分成M,V,VM ，VM 是思想核心，前端中使用他，主要是为了开发方面，因为MVVM提供了数据的双向绑定（双向绑定有VM提供）


### [vue学习](https://www.bilibili.com/video/av50680998/?p=3)
---
**1.v-cloak**  
它能够解决  插值表达式的闪烁问题  

---
**2.v-text**
+ 等价于插值表达式 但是没有闪烁问题  
+ **v-text**会覆盖元素中原本的问题，但是插值表达式  只会替换自己 的这个占位符， 不会把 整个元素清空  
---
**3.v-html**  
+ **v-cloak**和**v-text**会当成文本渲染，覆盖内容，把内容当成html  
---

**v-bind**
vue中提供的绑定属性的指令

```
<input type="button" value="按钮" v-bind:title="mytitle + '123'">

<input type="button" value="按钮" :title="mytitle + '123'">

注意：v-bind中，可以写合法的JS表达式
     v-bind可以简写为： :要绑定的属性
```


