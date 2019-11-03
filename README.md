# VueStudy
----
### [vue学习](https://www.bilibili.com/video/av50680998/?p=3)
---
**1.v-cloak**
它能够解决  插值表达式的闪烁问题
**2.v-text**
+ 等价于插值表达式 但是没有闪烁问题
+ **v-text**会覆盖元素中原本的问题，但是插值表达式  只会替换自己 的这个占位符， 不会把 整个元素清空
**3.v-html**
+ **v-cloak**和**v-text**会当成文本渲染，覆盖内容，把内容当成html

----
**v-bind**
vue中提供的绑定属性的指令
```
<input type="button" value="按钮" v-bind:title="mytitle + '123'">

<input type="button" value="按钮" :title="mytitle + '123'">

注意：v-bind中，可以写合法的JS表达式
     v-bind可以简写为： :要绑定的属性
```


