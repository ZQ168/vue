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
