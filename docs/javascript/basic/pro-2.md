# 什么是原型链，原型链有什么特点?

?> `原型链`是利用原型让一个引用类型继承另一个引用类型的属性和方法

**`null` 没有原型，并作为这个原型链中的最后一个环节**

**几乎所有 JavaScript 中的对象都是位于原型链顶端的Object的实例**

> 由于`__proto__`是任何对象都有的属性，而js里万物皆对象，所以会形成一条`__proto__`必须最终到头，并且值是`null`

> 当js引擎查找对象的属性时，先查找对象本身是否存在该属性，如果不存在，会在原型链上查找，但是不会查找自身的`prototype`

**参考资料：**

[MDN: 继承与原型链](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)

[三张图搞懂JavaScript的原型对象与原型链](https://www.cnblogs.com/shuiyi/p/5305435.html)

[题目来源](https://www.nowcoder.com/questionTerminal/dafdf862d4614009a9eab014a157dd83)
