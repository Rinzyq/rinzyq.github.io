---
title: vue-detail
date: 2021-05-13 09:33:19
tags:
---

# Vue 细节

## vue 中的$options 作用

众所周知在 data 外面定义的属性是无法进行响应式刷新的，如果我们需要获取 data 外面的数据，就需要使用$options,并且$options 的数据是页面初始化的数据

```
<script>
export default {
  name: "Test",
  data() {
    return {

    };
  },
  //在data外面定义的属性和方法通过$options可以获取和调用
  name: "zs",
  age: 12,
  haha() {
    console.log("haha");
  },
  created() {
    console.log(this.$options.name);  // zs
    console.log(this.$options.age);  //12
    this.$options.haha();  // haha

  },
</script>
```

## vue 的样式穿透

一般在我们用第三方组件库的时候会需要在父组件穿透到子组件来修改子组件的 css
利用 vue 的样式穿透可以做到

例如在父组件更改 el-tag 的样式

```
::v-deep .el-tag{
    //更改样式
}
```

## vue 的$attrs和$listeners

在我们使用第三方组件进行二次封装的时候，可以使用这两个属性来向子组件传所有的值

例如在 el-select 中传递属性和事件

> v-bind="$attrs"
> v-on="$listeners"

```
<el-select v-bind="$attrs" v-on="$listeners>
    //代码
</el-select>
```
