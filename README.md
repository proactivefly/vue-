# 双向数据绑定 - 前置技术点

## 1. 数组的 reduce() 方法

> 应用场景：下次操作的初始值，依赖于上次操作的返回值。

1. 数值的累加计算

2. 链式获取对象属性的值

## 2. 发布订阅模式

1. Dep 类

   - 负责进行**依赖收集**
   - 首先，有个数组，专门来存放所有的订阅信息
   - 其次，还要提供一个向数组中追加订阅信息的方法
   - 然后，还要提供一个循环，循环触发数组中的每个订阅信息

2. Watcher 类

   - 负责**订阅一些事件**

## 3. 使用 Object.defineProperty() 进行数据劫持

1. 通过 `get()` 劫持**取值操作**

2. 通过 `set()` 劫持**赋值操作**