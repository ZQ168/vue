# VUE手册
星河滚烫，你说人间理想。不辜负生活，不迷失方向  

VUE定的简化写法sync
更新数据
```
jumpDecision: {
  get() {
    return this.jumpDecisionData;
  },
  set(val) {
    this.$emit('update:jumpDecisionData', val);
  },
}
```

### vue中的filter方法如何定义，如何写的，作用是什么？？


组件嵌套思维：
table中需要form表单校验：
方向主要为table和form的嵌套：


table表格和表单的嵌套原则是什么：
因为table中始终有输入框需要进行校验，大面积校验用form表单更高效，所以出来了table嵌套form的一种范式的出现
form表单，双向数据绑定的原理？


### 为什么vue中的data是函数，而不是对象  
函数的话，每个组件中的data都有单独的引用，不存在变量污染问题  
源码分析： 
```
function render() {
  with(this) {
    return _c('div', [_c(Counter),_c('Counter')], 1)
  }
}
```
源码解析：  
每一个Counter会被_c调用，也就是createElement，createElement会直接拿着Counter上的data去创建一个组件。所有的Counter组件实例上的data都会指向同一个引用。

### VUE中的数据传递

vue组件间通信的几种方式：
props  
$emit/$on  
vuex  
$parent / $children  
$attrs/$listeners  
provide/inject  

vue中nextTick表示的是异步更新队列  
### 手动强制更新 $forceUpdate
vm.$forceUpdate()  
强制VUE实例更新，只影响实例本身和插入插槽内容的子组件，不能更新所有子组件  

### v-if 、 v-show
v-if 是真正的条件渲染，在条件切换的过程中条件块的事件监听器和子组件会被销毁和重建
是惰性渲染，在值不变的时候不会渲染  
v-if 有更高的切换开销，而 v-show 有更高的初始渲染开销。
因此，如果需要非常频繁地切换，则使用 v-show 较好；如果在运行时条件很少改变，则使用 v-if 较好。

组件创建：基于新实例的创建

组件的data必须是一个函数，因为每一个实例可以维护一份被返回对象的独立的拷贝

组件构建逻辑：
单独的props传递：


vue还有异步加载组件的功能

this.$root获取根组件
this.$parent获取父级

### VUE3实现动态组件
vue中的createElement，告诉Vue需要渲染怎么样的节点，包含子节点的描述

### vue中的observervable
原生构造的类型：
String，Number，Boolean, Date，Array，Object，Function，Symbol

destroy
beforeDestory，destroyed钩子

### slot  
$slot  
default  property包括了所有没有被包含在具名插槽中的节点   

### 内部异步队列
Promise.then、 mutationObserver、setImmediate  

mutationObserver,创建并返回MutationObserver，它会在指定的dom发生变化时被调用  
disconnect 阻止MutationObserver实例继续接收通知，直到再次调用Observer()方法，该观察者对象包含的回调函数都不会被再调用
observe()在DOM更改匹配给定选项，通过回调函数开始接收通知
