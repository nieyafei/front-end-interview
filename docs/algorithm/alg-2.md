# 素数: 你将如何验证一个素数？

?> 一个素数只能被它自己和1整除。所以，我将运行一个while循环并加1。看代码示例，如果你无法理解，那这不是你的菜。先回去学习javaScript基础知识然后再回来吧。）

?> **`素数（质数）`定义为在大于1的自然数中，除了1和它本身以外不再有其他因数。**

## 验证方法1

```js
function isPrime(n){
  var divisor = 2;
  while (n > divisor){// 必须大于1
    if(n % divisor == 0){// 不等于自己且存在被整除，则不是素数
     return false; 
    }
    else
      divisor++;
  }
  return true;
}
isPrime(137); //   = true
isPrime(237); //   = false
```

> **`问`：你能做的更好吗？**

> **`答`：可以。除数一次增加1个。 在3之后我可以增加2.如果一个数可以被任何偶数整除，它将被2整除。**

**补充：如果你不需要把除数增加到这个数。你可以更早停止。让我在下面的步骤中解释一下（如果需要可以多读几遍）**

> **`第一步`: 任何数字都不能被大于它的一半的数字整除。 例如，13将永远不能被7,8,9整除……它甚至可以是偶数的一半。 例如，16将被8整除，但永远不会被9,10,11,12 ……**

> **结论：一个数字将永远不能被一个大于其一半数值的数字整除。 所以，我们可以少循环`50％`。**

> **`第二步`: 现在，如果一个数字不能被3整除。（如果它可被3整除，那么它就不是质数）。然后，它不可以被大于其值1/3的任何数整除。例如，35不能被3整除。因此，它永远不会被大于35/3的数整除，永远不能被12, 13, 14整除…如果你取一个像36一样的偶数，它将永远不能被13, 14, 15整除。**

> **结论： 一个数字可以被其数值的三分之一整除。**

> **`第三步`: 例如，你有一个数字127。127不能被2整除，因此你最多应该检查63.5。其次，127不能被3整除。因此，您将检查到127/3大约42。它不能被5整除，除数应该小于127/5大约25，而不是7。那么，我们该在哪里停下来？**

> **结论： 除数将小于`math.sqrt(N)`**

## 验证方法2

```js
function isPrime(n){
  var divisor = 3, 
      limit = Math.sqrt(n);// 返回n的平方根
  //check simple cases
  if (n == 2 || n == 3)
     return true;
  if (n % 2 == 0)// 大于2的偶数
     return false;
  while (divisor <= limit)
  {
    if (n % divisor == 0)
      return false;
    else
      divisor += 2;
  }
  return true;
}
isPrime(137); // = true
isPrime(237); // = false
```

**参考资料**

[素数](https://baike.baidu.com/item/%E8%B4%A8%E6%95%B0/263515?fr=aladdin)

[JS: Interview Algorithm](http://thatjsdude.com/interview/js1.html)

[翻译：JS: Interview Algorithm](https://www.liayal.com/article/5ac46c20a6cf4e67bc05c9f4#%E6%96%B9%E6%B3%952)

[MDN: Math.sqrt()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/sqrt)