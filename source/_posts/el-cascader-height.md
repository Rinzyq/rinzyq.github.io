---
title: el-cascader-height
date: 2021-05-13 09:32:57
tags:
---

# el-cascader 的选择框高度问题

问题描述：如果选择框内的选项过多，会直接撑满整个选择框，高度过长

##### 解决问题

在全局样式表中加入

```
.el-cascader-panel{
    height:300px
}
```

就可以设置固定高度了
