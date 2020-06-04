# 数组的原生方法有哪些？

### 改变自身的方法

?> `copyWithin()` 方法浅复制数组的一部分到同一数组中的另一个位置，并返回它，而不修改其大小

?> `Array.prototype.fill()` 用一个固定值填充一个数组中从起始索引到终止索引内的全部元素

?> `Array.prototype.pop()` 删除数组的最后一个元素，并返回这个元素

?> `Array.prototype.push()` 在数组的末尾增加一个或多个元素，并返回数组的新长度

?> `Array.prototype.reverse()` 颠倒数组中元素的排列顺序，即原先的第一个变为最后一个，原先的最后一个变为第一个

?> `Array.prototype.shift()` 删除数组的第一个元素，并返回这个元素

?> `Array.prototype.sort()` 对数组元素进行排序，并返回当前数组

?> `Array.prototype.splice()` 在任意的位置给数组添加或删除任意个元素

?> `Array.prototype.unshift()` 将一个或多个元素添加到数组的开头，并返回新数组的长度

### 不改变自身的方法

?> `Array.prototype.concat()`方法用于合并两个或多个数组。此方法不会更改现有数组，而是返回一个新数组

?> `Array.prototype.includes()` 判断当前数组是否包含某指定的值，如果是返回 true，否则返回 false

?> `Array.prototype.join()` 连接所有数组元素组成一个字符串

?> `Array.prototype.slice()` 抽取当前数组中的一段元素组合成一个新数组

?> `Array.prototype.toSource()` 返回一个表示当前数组字面量的字符串。遮蔽了原型链上的 Object.prototype.toSource() 方法

?> `Array.prototype.toString()` 返回一个由所有数组元素组合而成的字符串。遮蔽了原型链上的 Object.prototype.toString() 方法

?> `Array.prototype.toLocaleString()` 返回一个由所有数组元素组合而成的本地化后的字符串。遮蔽了原型链上的 Object.prototype.toLocaleString() 方法

?> `Array.prototype.indexOf()` 返回数组中第一个与指定值相等的元素的索引，如果找不到这样的元素，则返回 -1

?> `Array.prototype.lastIndexOf()` 返回数组中最后一个（从右边数第一个）与指定值相等的元素的索引，如果找不到这样的元素，则返回 -1

### 遍历方法

?> `Array.prototype.forEach()` 为数组中的每个元素执行一次回调函数

?> `Array.prototype.entries()` 返回一个数组迭代器对象，该迭代器会包含所有数组元素的键值对

?> `Array.prototype.every()` 如果数组中的每个元素都满足测试函数，则返回 true，否则返回 false

?> `Array.prototype.some()` 如果数组中至少有一个元素满足测试函数，则返回 true，否则返回 false

?> `Array.prototype.filter()` 将所有在过滤函数中返回 true 的数组元素放进一个新数组中并返回

?> `Array.prototype.find()` 找到第一个满足测试函数的元素并返回那个元素的值，如果找不到，则返回 undefined

?> `Array.prototype.findIndex()` 找到第一个满足测试函数的元素并返回那个元素的索引，如果找不到，则返回 -1

?> `Array.prototype.keys()` 返回一个数组迭代器对象，该迭代器会包含所有数组元素的键

?> `Array.prototype.map()` 返回一个由回调函数的返回值组成的新数组

?> `Array.prototype.reduce()` 从左到右为每个数组元素执行一次回调函数，并把上次回调函数的返回值放在一个暂存器中传给下次回调函数，并返回最后一次回调函数的返回值

?> `Array.prototype.reduceRight()` 从右到左为每个数组元素执行一次回调函数，并把上次回调函数的返回值放在一个暂存器中传给下次回调函数，并返回最后一次回调函数的返回值

?> `Array.prototype.values()` 返回一个数组迭代器对象，该迭代器会包含所有数组元素的值

?> `Array.prototype[@@iterator]()` 数组的 iterator 方法，默认情况下与 values() 返回值相同



**参考资料：**

[Array: MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/isArray)

[题目来源](https://zhuanlan.zhihu.com/p/29514159)