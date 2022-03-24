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
