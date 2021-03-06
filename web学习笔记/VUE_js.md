# VUE_js

- v-bind属性绑定

  用法：<span v-bind:title = 'message'>

- input的`v-model`属性绑定(等价于value)

- 双向绑定

- vue组件的重要选项

  - date：代表了vue对象的数据
  - methods：代表了vue对象的方法
  - watch：设置了对象监听的方法
  - components：组件化  
  - props：组件之间的通讯

- 模板指令——html和vue对象的粘合剂

  - v-text：渲染数据

    - `v-text`和`{{}}`用法等价
    - 大胡子`{{}}`里边支持表达式，但是只支持单个语句。如：

      ```html
       <h1>{{ message.concat('!!!') }}</h1>
        <h1>{{ message? 'has message' : 'no message' }}</h1>
      ```
    - `v-text`会将元素当成纯文本输出，`v-html`会将元素当成HTML标签解析后输出。`v-html`可以将某些标签加入某个标签中（date中某个属性为一段html）

  - v-if：控制显示。条件渲染指令，根据其后表达式的bool值进行判断是否渲染该元素

  - v-show：与`v-if`不同的是带有 `v-show` 的元素始终会被渲染并保留在 DOM 中。`v-show` 只是简单地切换元素的 CSS 属性 `display`。

    **注意：**`v-show` 不支持 `<template>` 元素，也不支持 `v-else`

  - v-for：渲染循环列表（提供元素+索引(索引是可选第二参数)）

    - 一个对象的 `v-for`

      ```html
      <li v-for="value in object">
      <!--以第二个参数为键值,第三个参数为索引-->
      <li v-for="(key,value,index) in object">
      ```

    - 一段取值范围的 `v-for`

      ```html
      <div>
        <span v-for="n in 10">{{ n }} </span>
      </div>
      ```

      ​

    **注意：**当 `v-if` 与 `v-for` 一起使用时，`v-for` 具有比 `v-if` 更高的优先级

  - v-on：事件绑定

    - `:click`   点击事件绑定 等价于` @click`
    - `:dbclick `  双击事件绑定
    - `:mousemove`   鼠标移动事件
    - 事件修饰符：`.once`，`.prevent`，`.stop`
    - 键值修饰符：`:keyup.enter`

  - v-bind：属性绑定
    - `:class` class属性绑定，等价于` :class`
     - `:src`  src属性  

- 计算属性：computed

  因为methods中的全部方法都会被执行一遍，而计算属性computed是基于依赖进行缓存的，相关依赖发生改变的时候才执行。(且使用时不加括号)

  **注意：**当有大量数据时或者复杂逻辑使用进行优化，平时还是用methods中的方法


- 指令的语法：

  v-指令名 = “表达式判断或者是业务模型中属性名或者事件名”

- 数组操作

  - 以下操作造成的变动将无法被vue检测，从而引起变化

    - 使用索引设置一个项

      ```javascript
      vm.items[indexOfItem] = newValue;
      //用以下方法实现
      Vue.set(example1.items, indexOfItem, newValue);
      //或者
      example1.items.splice(indexOfItem, 1, newValue);
      ```

    - 修改数组长度

      ```javascript
      vm.items.length = newLength;
      //用下面的方法实现
      example1.items.splice(newLength)
      ```

    - 对象添加一个属性

  - 想要显示一个数组的过滤或排序副本，而不实际改变或重置原始数据。在这种情况下，可以创建返回过滤或排序数组的计算属性(computed)或者方法(methods)。

- 样式CSS作用域

  - 子组件的css优先级高于父组件（后加载，覆盖之前的）
  - 添加scoped，使得样式在该组件内作用

- 组件之间的通讯：props

   