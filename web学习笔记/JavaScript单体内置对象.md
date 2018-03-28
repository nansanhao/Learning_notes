## JavaScript除Object，String，Array之外还有两个单体内置对象

- Global对象：不属于任何其他对象的方法，都是属于它的方法。终极兜底对象。
  - 方法：
    - isNaN( )
    - isFinite( ）
    - parseInt( )
    - parseFloat( )
    - URI编码方法
      - encodeURI( )
      - encodeURIComponet( )
    - eval( )
      - 像是一个完整的ECMASctript解析器
    - Window对象：在全局作用域声名的所有变量和函数，都成为Window对象的属性。是用来访问Global对象而存在的。
- Math对象