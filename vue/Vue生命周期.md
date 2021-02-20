### Vue生命周期

 实例生命周期钩子

>每个Vue实例在被创建时都要经过一系列的初始化过程。

<img src="%E5%9B%BE%E7%89%87/lifecycle.png" alt="lifecycle" style="zoom: 33%;" />

注：

> 不要在选项 property 或回调上使用[箭头函数](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Functions/Arrow_functions)，比如 `created: () => console.log(this.a)` 或 `vm.$watch('a', newValue => this.myMethod())`。因为箭头函数并没有 `this`，`this` 会作为变量一直向上级词法作用域查找，直至找到为止，经常导致 `Uncaught TypeError: Cannot read property of undefined` 或 `Uncaught TypeError: this.myMethod is not a function` 之类的错误。