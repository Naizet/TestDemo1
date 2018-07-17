# vuebase

> test

## Build Setup

```bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

<template>：
      组件只能有一个根点
<script>：
<style>:
        scoped样式只在当前组件内生效
子父级组件交互通信
         父->子： props
         子->父：emit Event
         数据传递限制

基本指令：
v-html：渲染文本
v-text:渲染文本
v-bind:绑定

vue 是什么

简介型的 javascript 框架 个人开发 (刘雨溪)

     特点：mvvm       m=mvc   module 模型   v=view 视图    c=controller  控制器
          mvvm       m=mvc   module 模型   v=view 视图     vm (视图与数据之间的传递)
          vue1 双向数据绑定   vue2 单向数据流
           单页面应用

v-model 数据绑定
data 返回对象用 return
v-for 循环 格式 v-for="字段名 in(of) 数组 json"
v-show 显示 隐藏 传递的值为布尔值 true false 默认为 false
v-if 显示与隐藏 和 v-show 对比的区别 就是是否删除 dom 节点 默认值为 false
v-else-if 必须和 v-if 连用
v-else 必须和 v-if 连用 不能单独使用 否则报错 模板编译错误
v-bind 动态绑定 作用： 及时对页面的数据进行更改 ':'代替
v-on 绑定事件 函数必须写在 methods 里面
@click 快捷方法
v-text 解析文本
v-html 解析 html 标签
v-bind:class 三种绑定方法 1、对象型 '{red:isred}' 2、三目型 'isred?"red":"blue"' 3、数组型 '[{red:"isred"},{blue:"isblue"}]'
v-once 进入页面时 只渲染一次 不在进行渲染
v-cloak 防止闪烁
v-pre 把标签内部的元素原位输出

条件渲染：
v-if
v-else
v-else-if
v-show

列表渲染：
v-for:
<div class="list">
<ul>
<li v-for="name in names">{{name }}</li>
</ul>

   </div>
    names:['iwen','wen','en'],
     <ul>
      <li v-for="item in user">
      <span>{{item.name}}</span>
      <span>{{item.age}}</span>
      </li>
      </ul>
user:[
        {
          name:guolu,
          age:20
        },
        {
          name:xioahei,
          age:20
        },
      ]

事件监听：
v-on：可以用@代替
methods:{

}
修饰符：
.stop
.prevent
.capture
.self
.once

数组更新检测：
变异方法：引起视图更新
替换数组：不引起视图更新

显示过滤/排序结果：filter

计算属性与观察者：computed:{}
表单输入绑定：
v-model 双向数据绑定（可读可写）
watch:{}监听数据的绑定
修饰符：
.lazy 失去焦点之后才响应
.trim


插槽slot
//keep-alive 缓存，不更新页面