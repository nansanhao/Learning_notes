# flex布局

#### 描述：即弹性容器，为盒子模型提供灵活性。

#### 默认的轴：主轴和交叉轴![img](http://www.runoob.com/wp-content/uploads/2015/07/3791e575c48b3698be6a94ae1dbff79d.png)

#### 容器属性：

- flex-direction（主轴方向）

  ```css
  .box {
    flex-direction: row | row-reverse | column | column-reverse;
  }
  ```

- flex-wrap（轴线排不下就换行）

  ```
  .box{
    flex-wrap: nowrap | wrap | wrap-reverse;
  }
  ```

- flex-flow（flex-direction属性和flex-wrap属性的简写形式）

  ```
   .box {
    flex-flow: <flex-direction> || <flex-wrap>;
  }
  ```

- justify-content（主轴上的对齐方式）

  ```
  .box {
    justify-content: flex-start | flex-end | center | space-between | space-around;
    //当只有一个容器成员时，space-between无作用，想居中则使用space-around
  }
  ```

- align-items（交叉轴上的对齐方式）

  ```
  .box {
    align-items: flex-start | flex-end | center | baseline | stretch;
    //center是垂直居中，baseline是项目第一行文字的基线对齐，stretch是默认值
  }
  ```

- align-content（多根轴线的对齐方式）

#### 项目属性：

- order（定义项目的排列顺序。数值越小，排列越靠前，默认为0）

- flex-grow（项目的放大比例）

  ```
  .item {
    flex-grow: <number>; /* default 0 */
    //响应式布局，按照数字比例分配空间
  }
  ```

- flex-shrink（项目的缩小比例）

- flex-basis

- flex（flex-grow, flex-shrink 和 flex-basis的简写）

  ```
  .item {
    flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]
  }
  ```

- align-self（align-self属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch）

