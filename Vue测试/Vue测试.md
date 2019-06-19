## 什么是vue

- vue是现在最流行的前端框架
- 它和angular.js, react.js 并称前端三大主流框架
- vue能方便的和前端页面进行数据交互，轻松渲染数据到页面中

## 为什么要学习vue

- vue 非常简单，极易上手
- 性能非常高
- 开发人员不用再去关心dom的操作，只需要关注业务层

## 什么是dom操作

- 前端动画效果
- 前端数据的验证

## 前端操作dom的技术发展演变

- javascript
  - 缺点
    - 代码书写复杂
    - 浏览器版本不兼容
    - 大量的dom操作，损耗性能
- jquery
  - 改进后兼容各种浏览器，代码书写简化许多
  - 缺点
    - 大量的操作dom，损耗性能
- vue
  - 代码简洁
  - 兼容各种浏览器
  - 去掉了大量的dom操作，性能很高

## vue的基本使用

- 引入vue的包:undefinedundefined<script src="vue-2.5.16.js"></script>
- 嵌入vue的基本结构

```
 window.onload = function () {  
 //window.onload 等待页面全部加载完成之后再执行代码
        var vm = new Vue({
            //el代表和文档的哪一块内容是交互
            el: '#main',
            // data里面是定义要渲染的变量的值
            data: {
            content: 'Vue的基本使用'
        },
        methods:{
            func: function(){
                console.log('Vue的基本使用')
            }  
        }
    });
```

- 参数说明
  - el：指向一个DOM成员，在这个成员中的所有元素都可以被vue识别到
  - data：存放数据成员，可以把成员绑定在某个元素上
  - methods：存放操作方法，为某个元素绑定一个操作方法

## vue的基本语法

- 绑定元素内容
  - {{ content }}
- 绑定元素属性
  - \<a v-bind:href="url"\>\</a\>
  - \<a :href="url"\>\</a\>
  - :是v-bind简写形式
- 绑定元素方法
  - <button v-on:click='fnAddClick'>计数器:{{count}}</button>
  - <button @click='fnAddClick'>计数器:{{count}}</button>
  - @是v-on的简写

## 条件渲染

- v-if
- v-else-if
- v-else
- v-show  （true时内容显示,为false时内容隐藏）
- v-if和v-show的区别
  - v-if控制元素生成和销毁
  - v-show控制元素的显示和隐藏（元素是存在的）

## 列表渲染(for循环)

- 普通列表
  - item: ['a', 'b', 'c', 'd']
  - for v in item
- 列表下标
  - item: ['a', 'b', 'c', 'd']
  - for v,k in item
- 只有一个对象
  - item: {name:'小明', age:19}
  - for v,k in item
- 对象列表
  - item: [{name:'小明', age:19}, {name:'小新', age:20}]
  - for obj in item
  - obj.name

## Vue的使用情况

- 一般情况下Vue模板语法：{ { } }

  当Vue写成[ [ ] ] 时:

  是为了避免django模板语法冲突,修改Vue变量的读取语法  # 写在js模板里面 
  delimiters:['[ [' , '] ]'],

   ——>  Vue模板语法：[ [ ] ]

  当后端返回的是render(...,context={}),那么前端使用jinja2模板语法    jinja2模板语法：{ { } }

  当后端返回的是http.JsonResponse({context:xx}),那么前端使用Vue的语法









