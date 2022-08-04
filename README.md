# VUE手册
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
