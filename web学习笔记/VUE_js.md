# VUE_js

- v-bind属性绑定

  用法：<span v-bind:title = 'message'>

- input的v-model属性绑定(等价于value)

- 双向绑定

- vue组件的重要选项

  - date：代表了vue对象的数据
  - methods：代表了vue对象的方法
  - watch：设置了对象监听的方法
  - components：组件化  
  - props：组件之间的通讯

- 模板指令——html和vue对象的粘合剂

  - v-text：渲染数据

    - v-text和{{}}用法等价


    - 大胡子{{}}里边支持表达式，但是只支持单个语句。如：

      ```html
       <h1>{{ message.concat('!!!') }}</h1>
        <h1>{{ message? 'has message' : 'no message' }}</h1>
      ```


    - v-text会将元素当成纯文本输出，v-html会将元素当成HTML标签解析后输出。

  - v-if：控制显示。条件渲染指令，根据其后表达式的bool值进行判断是否渲染该元素；

  - v-for：渲染循环列表

  - v-on：事件绑定

    - :click   点击事件绑定 等价于 @click

  - v-bind：属性绑定

    - :src  src属性    
    - :class属性常用 故有简写形式:   :class


- 指令的语法：

  v-指令名 = “表达式判断或者是业务模型中属性名或者事件名”

