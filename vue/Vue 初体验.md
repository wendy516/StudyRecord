### Vue 初体验

#### 语法

1. Mustache语法：	{{}}

2. v-for :将一个数组渲染成一个列表 

   ~~~vue
   <li v-for="item in items">{{item.message}}</li>
   ~~~

3. 

#### 缩写

v- 前缀作为一种视觉提示，用来识别模板中Vue特定的attribute。

由于使用比较频繁，Vue为**v-bind**和**v-on**这两个最常用的指令，提供了特定简写：

* **v-bind缩写**

  ~~~vue
  <!--完整语法-->
  <a v-bind:href="url"></a>
  
  <!--缩写-->
  <a :href="url"></a>
  
  <!-- 动态参数的缩写 (2.6.0+) -->
  <a :[key]="url"> ... </a>
  ~~~

* **v-on缩写**

~~~vue
<!-- 完整语法 -->
<a v-on:onclick="doSomething"></a>

<!-- 缩写 -->
<a @click="doSomething"></a>

<!-- 动态参数的缩写 (2.6.0+) -->
<a @[event]="doSomething"></a>
~~~

#### Vue对象

* **el :**

  类型：string|htmlElement

   作用：挂载到哪个dom对象,决定vue实例会管理哪个DOM。

* **data**

  类型：Object|Function(组件当中data必须是一个函数)

  作用：Vue实例对应的数据对象

* **methods**

  类型：{[key:string]:Funtion}

  作用：该属性用于在Vue对象中定义方法。 可以在其他地方调用，也可以在指令中使用。
  
* **computed**

  类型：{[key:string]:Function | {get:Function, set:Function}

  作用：计算属性的结果会被缓存，除非依赖的响应式property变化才会重新计算。

```vue
var vm = new Vue({
  el: '#example',
  data: {//Vue实例对应的数据对象。
    message: 'Hello'
  },
  methods: {//该属性用于在Vue对象中定义方法。 可以在其他地方调用，也可以在指令中使用。
    plus: function () {

	}
  }
  computed: {//计算属性。
    // 计算属性的 getter
    reversedMessage: function () {
      // `this` 指向 vm 实例
      return this.message.split('').reverse().join('')
    }
  }
})
```

