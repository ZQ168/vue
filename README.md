# vue的面试官手册
VUE定的简化写法sync
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


vue中的filter方法如何定义，如何写的，作用是什么？？


组件嵌套思维：
table中需要form表单校验：
方向主要为table和form的嵌套：
